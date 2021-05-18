# Sub Zettelform2

Sub Zettelform2()

'Dieses Programm formatiert exportierte Zettelkästen Einträge (fortlaufend
'in einer Datei) und ist für Word gedacht. Dabei eignet sich das Programm besonders für die Weitergabe.
'Voraussetzung: Formatierung im Zettelkasten ist eingestellt auf: Leerzeilen: 2 1 2 3
'Außerdem gilt: Alle Zettel haben eine Überschrift!
'Folgende Struktur der Anhänge zum Zettelkasten wird zugrundegelegt:
'...zkn\Anhang\Anhang...
'             \Anhang...
'Die exportierte Datei soll dann im gleichen Verzeichnis wie die Zettelkastendatei gespeichert
'werden (in diesem Fall funktionieren die erzeugten relativen Anhänge!)
'...zkn
'...rtf
'Das Zettelkastenprogramm befindet sich unter Z:\Zettelkasten, die einzelnen Zettelkästen
'in Unterordnern davon, z. B. Z:\Zettelkasten\zettelkasten.exe
'                             Z:\Zettelkasten\Informatik\Informatik.zkn
'Das Programm kopiert die Verknüpfungen, die angehängt sind, in das gleiche Verzeichnis,
'wie das der Zettelkastendatei.
'Anschließend braucht man nur noch die RTF-Datei sowie die neu angelegten Dateien aus diesem
'Verzeichnis zusammenzippen (ohne die Zettelkastendatei) und kann diese dann einfach weiterverwenden
'Das funktioniert jedoch nur, wenn eine Datei keine anderen Dateien zum Betrieb benötigt. So haben HTML
'Dateien oft einen Unterordner, in dem die Bilder gespeichert sind oder zusätzliche Dateien mit Bildern.
'In diesem Fall würde nur die HTML-Datei, wenn diese im Zettelkasten verknüpft ist selbst kopiert,
'die Bilder bleiben aber "draußen".
'Als Alternativen zum HTML-Format bieten sich: Konvertierung nach PDF oder Speichern als Webseitenarchiv,
'z. B. MHT-Archiv (Internet Explorer), MAF-Archiv (Firefox (Extension)) oder unter Verknüpfungen neben der
'HTML-Datei auch noch den Ordner mit den untergeordneten Dateien angeben.

    'Variablendeklaration
    Dim oRange As Range
    Dim rngFormat As Range
    Dim adresse, adresse2, alteadresse, dateiname, Suchtext, Suchtext2, ziel As String
    Dim Position
    'Ende Variablendeklaration

    'Inhalt einfügen
    Set rngFormat = ActiveDocument.Range(Start:=0, End:=0)
    With rngFormat
         .InsertAfter Text:=ActiveDocument.Name & " vom " & Date & " " _
         & Time & vbCrLf & vbCrLf & "Inhalt" _
         & vbCrLf & vbCrLf & vbCrLf
         .InsertParagraphAfter
         With .Font
              .Name = "Arial"
              .Size = 14
              .Bold = True
         End With
    End With

    'Überschriften festlegen und formatieren
    For Each para In ActiveDocument.Paragraphs
        If para.Range.Words(1).Text = "Eintrag " And para.Range.Words(1).Font.Bold And _
        para.Range.Words(1).Font.Underline Then
           'Eintrag = Überschrift 1
           para.Style = ActiveDocument.Styles(wdStyleHeading1)
           para.Range.InsertParagraphBefore
           Set para = para.Previous
           'Seitenumbruch vor jedem neuen Eintrag einfügen
           para.Range.InsertBreak
           Set para = para.Next
        End If
        If para.Range.Words(1).Text = "Anmerkung" And para.Range.Words(1).Font.Underline Then
           'Anmerkung = Überschrift 2
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
        End If
        If para.Range.Words(1).Text = "Autor" And para.Range.Words(1).Font.Underline Then
           'Autor = Überschrift 2
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
        End If
        If para.Range.Words(1).Text = "Stichworte" And para.Range.Words(1).Font.Underline Then
           'Stichwörter = Überschrift 2
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
           Set para = para.Next
        End If
        If para.Range.Words(1).Text = "Verweise" And para.Range.Words(1).Font.Underline Then
           'Verweise = Überschrift 2
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
        End If
        If para.Range.Words(1).Text = "Verknüpfungen " And para.Range.Words(1).Font.Underline Then
           'Verknüpfungen (Web) bzw. Verknüpfungen (Datenträger) = Überschrift 2
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
        End If
           'Verknüpfungen (Datenträger):
           '1. Ordner und Dateien werden in das Verzeichnis der Exportdatei kopiert
           '2. Die Hyperlinks werden entsprechend umgesetzt und aktiviert
           'Voraussetzung siehe oben
        If para.Range.Words(1).Text = "Verknüpfungen " Then
           Position = 1 'eigentlich unnötig, die Position zu setzen, hilft aber Struktur zu erkennen
                     'wenn man mal eine zweite Zeile eines Absatzes markieren will
           Set oRange = para.Range
           oRange.Start = oRange.Start + Position - 1
           oRange.End = oRange.End - 1
           Suchtext = "Verknüpfungen (Datenträger):"
           Suchtext2 = oRange
           If Suchtext = Suchtext2 Then
              'nacheinander die folgende Absätze durchgehen und die Hyperlinks umwandeln,
              'bis ein neuer Eintrag erfolgt
              While Not para Is Nothing And Suchtext2 [] ""
                    Set para = para.Next
                    Set oRange = para.Range
                    oRange.Start = oRange.Start + Position - 1
                    oRange.End = oRange.End - 1
                    Suchtext2 = oRange
                    adresse = oRange
                    adresse2 = ActiveDocument.Path
                    adresse = "Z:\Zettelkasten\" & adresse
                    Set fs = CreateObject("Scripting.FileSystemObject")
                    If fs.FolderExists(adresse) Then
                       If Len(adresse) ] Len(adresse2) Then
                          GoSub Namenfinden
                          fs.CopyFolder adresse, ziel
                          ActiveDocument.Hyperlinks.Add Anchor:=oRange, Address:= _
                          dateiname, TextToDisplay:=dateiname
                       End If
                    Else
                       If fs.FileExists(adresse) Then
                          If Len(adresse) ] Len(adresse2) Then
                             GoSub Namenfinden
                             If fs.FileExists(ziel) Then
                                Antwort = MsgBox("Die Datei " & ziel & " existiert bereits. Überschreiben?", vbYesNo)
                                If Antwort = vbYes Then
                                   Set f = fs.GetFile(ziel)
                                   'CopyFile funktioniert nur, wenn die zu überschreibende Datei
                                   'nicht schreibgeschützt ist
                                   If f.Attributes And 1 Then
                                      f.Attributes = f.Attributes - 1
                                      MsgBox ("Der Schreibschutz wurde für die Datei " & ziel & " entfernt!")
                                   End If
                                   fs.CopyFile adresse, ziel
                                End If
                            Else
                                fs.CopyFile adresse, ziel
                             End If
                             ActiveDocument.Hyperlinks.Add Anchor:=oRange, Address:= _
                             dateiname, TextToDisplay:=dateiname
                          End If
                       End If
                    End If
              Wend
           End If
        End If
        If para.Range.Words(1).Text = "sonstige " And para.Range.Words(1).Font.Underline Then
           para.Style = ActiveDocument.Styles(wdStyleHeading2)
        End If
        If para.Range.Words(1).Font.Bold And para.Range.Words(1).Font.Size [] 14 Then
           para.Style = ActiveDocument.Styles(wdStyleHeading3)
        End If
    Next para
    Datei = ActiveDocument.Name
    Datei = Left(Datei, Len(Datei) - 4)
    ActiveDocument.Content.InsertParagraphAfter
    Set para = ActiveDocument.Range.Paragraphs.Last
    para.Style = ActiveDocument.Styles(wdStyleNormal)
    ActiveDocument.Content.InsertAfter (vbCrLf & "Aus dem Zettelkasten: " _
    & Datei _
    & " vom " & Date & " " & Time & vbCrLf & "erstellt mit dem Zettelkasten nach Niklas Luhmann http://zettelkasten.danielluedecke.de/")
    'Inhaltsverzeichnis einfügen
    'Es werden die "Titel" der Dokumente eingefügt
    Set myRange = ActiveDocument.Paragraphs(6).Range
    ActiveDocument.TablesOfContents.Add Range:=myRange, _
    UseFields:=False, UseHeadingStyles:=True, _
    LowerHeadingLevel:=3, _
    UpperHeadingLevel:=1
    'Und jetzt noch die Kommata richtig stellen
    'Erst überall ein Leerzeichen hinten anfügen
    Set myRange = ActiveDocument.Content
    myRange.Find.Execute FindText:=",", ReplaceWith:=", ", _
    Replace:=wdReplaceAll
    'Die Strichpunkte in den Verweisen richtig stellen
    'Erst überall ein Leerzeichen hinten anfügen
    Set myRange = ActiveDocument.Content
    myRange.Find.Execute FindText:=";", ReplaceWith:="; ", _
    Replace:=wdReplaceAll
    'dann alle Leerzeichen, die hintereinanderauftreten löschen (bitte dreimal!)
    For Index = 1 To 3
        Set myRange = ActiveDocument.Content
        myRange.Find.Execute FindText:="  ", ReplaceWith:=" ", _
        Replace:=wdReplaceAll
    Next Index
    'Und jetzt noch ein AutoFormat, damit alle Hyperlinks, die mit http beginnen, richtig gestellt
    'werden
    Options.AutoFormatReplaceHyperlinks = True
    Options.AutoFormatApplyBulletedLists = False
    Options.AutoFormatApplyFirstIndents = False
    Options.AutoFormatApplyHeadings = False
    Options.AutoFormatApplyLists = False
    Options.AutoFormatApplyOtherParas = False
    Options.AutoFormatDeleteAutoSpaces = False
    Options.AutoFormatMatchParentheses = False
    Options.AutoFormatPlainTextWordMail = False
    Options.AutoFormatPreserveStyles = True
    Options.AutoFormatReplaceFarEastDashes = False
    Options.AutoFormatReplaceFractions = False
    Options.AutoFormatReplaceOrdinals = False
    Options.AutoFormatReplacePlainTextEmphasis = False
    Options.AutoFormatReplaceQuotes = False
    Options.AutoFormatReplaceSymbols = False
    Selection.Range.AutoFormat
    Set fs = Nothing
    Set f = Nothing
    
    Exit Sub

'GoSub Routine
Namenfinden:
    If Len(adresse) ] Len(adresse2) Then
       dateiname = Right(adresse, Len(adresse) - Len(adresse2) - 1)
       'solange kürzen bis kein \ mehr kommt
       
       While InStr(1, dateiname, "\")
             dateiname = Right(dateiname, Len(dateiname) - 1)
             ziel = adresse2 & "\" & dateiname
      Wend
    End If
Return

End Sub


