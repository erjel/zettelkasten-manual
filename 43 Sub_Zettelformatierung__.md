# Sub Zettelformatierung()

Sub Zettelformatierung()


**--------------------msel, 20.09.2005--------------------**
Dieses Makro ist inzwischen durch ein anderes Makro ersetzt,
was zusätzlich die Anhänge direkt in das Zettelkasten Export
Verzeichnis exportiert!
**--------------------msel, 20.09.2005--------------------**
 


`'Dieses Programm formatiert exportierte Zettelkästen Einträge (fortlaufend
'in einer Datei) und ist für Word gedacht.
'Voraussetzung: Formatierung im Zettelkasten ist eingestellt auf: Leerzeilen: 2 1 2 3
'Folgende Struktur der Anhänge zum Zettelkasten wird zugrundegelegt:
'...zkn\Anhang\Anhang...
'             \Anhang...
'Die exportierte Datei soll dann im gleichen Verzeichnis wie die Zettelkastendatei gespeichert
'werden (in diesem Fall funktionieren die erzeugten relativen Anhänge
'...zkn
'...rtf
'Das Zettelkastenprogramm befindet sich unter Z:\Zettelkasten, die einzelnen Zettelkästen
'in Unterordnern davon, z. B. Z:\Zettelkasten\zettelkasten.exe
'                             Z:\Zettelkasten\Informatik\Informatik.zkn

Dim oRange As Range
Dim rngFormat As Range
Dim adresse, adresse2 As String
Dim Suchtext, Suchtext2
Dim Position
    
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
        ' Eintrag = Überschrift 1
        para.Style = ActiveDocument.Styles(wdStyleHeading1)
        para.Range.InsertParagraphBefore
        Set para = para.Previous
        'Seitenumbruch vor jedem neuen Eintrag einfügen
        para.Range.InsertBreak
        Set para = para.Next
    End If
    If para.Range.Words(1).Text = "Anmerkung" And para.Range.Words(1).Font.Underline Then
       ' Anmerkung = Überschrift 2
       para.Style = ActiveDocument.Styles(wdStyleHeading2)
       Set para = para.Next
       ' Titel = Überschrift 3
       para.Style = ActiveDocument.Styles(wdStyleHeading3)
    End If
    If para.Range.Words(1).Text = "Autor" And para.Range.Words(1).Font.Underline Then
        ' Autor = Überschrift 2
        para.Style = ActiveDocument.Styles(wdStyleHeading2)
    End If
    If para.Range.Words(1).Text = "Stichworte" And para.Range.Words(1).Font.Underline Then
        ' Stichwörter = Überschrift 2
        para.Style = ActiveDocument.Styles(wdStyleHeading2)
        Set para = para.Next
    End If
    If para.Range.Words(1).Text = "Verweise" And para.Range.Words(1).Font.Underline Then
        ' Verweise = Überschrift 2
        para.Style = ActiveDocument.Styles(wdStyleHeading2)
    End If
    If para.Range.Words(1).Text = "Verknüpfungen " And para.Range.Words(1).Font.Underline Then
        ' Verknüpfungen (Web) bzw. Verknüpfungen (Datenträger) = Überschrift 2
        para.Style = ActiveDocument.Styles(wdStyleHeading2)
    End If
        ' Verknüpfungen (Datenträger) werden in relative Hyperlinks umgewandelt
        ' Voraussetzung siehe oben
    If para.Range.Words(1).Text = "Verknüpfungen " Then
        Position = 1 'eigentlich unnötig, die Position zu setzen, hilft aber Struktur zu erkennen
                     'wenn man mal eine zweite Zeile eines Absatzes markieren will
        Set oRange = para.Range
        oRange.Start = oRange.Start + Position - 1
        oRange.End = oRange.End - 1
        Suchtext = "Verknüpfungen (Datenträger):"
        Suchtext2 = oRange
        'MsgBox Suchtext
        'MsgBox Suchtext2
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
                  If Len(adresse) ] Len(adresse2) Then
                        adresse2 = Right(adresse2, Len(adresse2) - 16) 'hier zehn, da Speicherort
                                                                       'grundsätzlich Z:\Zettelkasten\
                        adresse = Right(adresse, Len(adresse) - Len(adresse2) - 1)
                        'MsgBox adresse
                        
                        ActiveDocument.Hyperlinks.Add Anchor:=oRange, Address:= _
                        adresse, TextToDisplay:=adresse
                  End If
                  
                        
            Wend
        End If
    End If
    If para.Range.Words(1).Text = "sonstige " And para.Range.Words(1).Font.Underline Then
        para.Style = ActiveDocument.Styles(wdStyleHeading2)
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
Set myrange = ActiveDocument.Paragraphs(6).Range
ActiveDocument.TablesOfContents.Add Range:=myrange, _
   UseFields:=False, UseHeadingStyles:=True, _
   LowerHeadingLevel:=3, _
   UpperHeadingLevel:=3
   
'Und jetzt noch die Kommata richtig stellen
'Erst überall ein Leerzeichen hinten anfügen
Set myrange = ActiveDocument.Content
myrange.Find.Execute FindText:=",", ReplaceWith:=", ", _
    Replace:=wdReplaceAll

'Die Strichpunkte in den Verweisen richtig stellen
'Erst überall ein Leerzeichen hinten anfügen
Set myrange = ActiveDocument.Content
myrange.Find.Execute FindText:=";", ReplaceWith:="; ", _
    Replace:=wdReplaceAll

'dann alle Leerzeichen, die hintereinanderauftreten löschen (bitte dreimal!)
'For index = 1 To 3
Set myrange = ActiveDocument.Content
myrange.Find.Execute FindText:="  ", ReplaceWith:=" ", _
    Replace:=wdReplaceAll
'Next index
    
' Und jetzt noch ein AutoFormat, damit alle Hyperlinks, die mit http beginnen, richtig gestellt
' werden
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

End Sub`



