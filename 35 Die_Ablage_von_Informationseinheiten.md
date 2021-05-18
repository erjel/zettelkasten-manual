# Die Ablage von Informationseinheiten

**Die Ablage von Informationseinheiten**

“ich bin schon seit einiger Zeit auf der Suche nach Software mit der man einigermassen anschaulich/uebersichtlich und "intelligent" Notizen, Webnotizen, Textschnippsel, Ideen (der uebliche Kram also) verwalten kann.”
From: Michael Schillo; Newsgroups: de.sci.informatik.ki; Subject: KI fuer den Hausgebrauch des Wissenschaftlers?; Date: 18 Apr 2002 08:08:09 -0700; Message-ID: [e9ccf96a.0204180708.49705bea@posting.google.com].

Diese Seite enthält einige Notizen zur Ablage von Informationen.
Prinzipien
KISS
Das Prinzip KISS  (“keep it simple, stupid ”) empfiehlt, Systeme möglichst einfach zu konstruieren.
Ein Ablagesystem muß einfach zu verstehen sein. Kompliziert erdachte Details wird man früher oder später vergessen. Ein Ablagesystem muß lebenslang verständlich sein. Auch wenn man sich nach einer Weltreise ein ganzes Jahr nicht mehr damit beschäftigt hat, sollte es möglich sein, daß man sofort wieder weiß, wo man eine Information abzulegen hat oder wie man eine bestimmte Information wiederfinden kann. Die beste Gewähr dafür ist es, wenn die Grundstrukturen des Systems absolut naheliegend und trivial sind.
ROCT
Das Prinzip ROCT  (“rely on common technology ”) empfiehlt es, nur weitverbreitete Standards einzusetzen.
Ein Ablagesystem muß auch nach mehreren Dekaden noch zugänglich bleiben, wenn das ursprünglich eingesetzte Betriebssystem vielleicht schon längst nicht mehr verfügbar ist. Der Aufwand, um Informationen aus einem ganz speziellen Programm zu extrahieren und ein spezielles Format in das spezielle Format eines anderen speziellen Programms zu wandeln, ist unter Umständen so groß, daß die mit einem speziellen System abgelegten Daten möglicherweise ganz oder teilweise mit diesem untergehen könnten.
Ein Beispiel zur Anwendung von ROCT  ist der Einsatz von Verzeichnissen und Textdateien zur Informationsablage. Alle zukünftigen Computer werden es voraussichtlich erlauben, Dateien und Verzeichnisse zu verwalten und diese zu durchsuchen. Wenn man Informationen in dieser Form ablegt, dann wird es voraussichtlich immer möglich sein, sie auf eine neues System übertragen zu können.
Ebenfalls portabel ist der Einsatz relationaler Datenbanktechnik, solange nur die gebräuchlichsten Operationen und Funktionen einer relationalen Datenbank verwendet werden. Da Datenbanken, die Daten relational verwalten können, vermutlich ebenfalls auf lange Sicht verfügbar sein werden, kann eine solche Datenbank ebenfalls noch als portabel angesehen werden.
Spezielle „Zettelkasten-Programme“ oder „Dokumenten-Verwaltungssysteme“ und ihre Hersteller haben nur eine endliche Lebenszeit. Ein großer Schaden entstünde, wenn solche Programme ausfielen und die Daten dann nicht mehr zugänglich wären. Daher sollten solche System vermieden werden, wenn sie ihre Verwaltungsdaten in einem speziellen nur mit dieser Software zugänglichen Format speichern. Akzeptabel wären solche Programme, die Informationen in einem gut dokumentierten und einfachen Verfahren so ablegen, so daß auf die Informationen auch noch mit Hilfe anderer Programmen zugegriffen werden kann oder die Informationen leicht in eine portable Struktur (Verzeichnisse mit Dateien [mit Standard-Dateitypen] oder relationale Datenbank) exportiert werden können.
Zentralisierung
Es führt zu erheblichen Aufwand, zur Verwaltung spezieller Ressourcetypen unterschiedliche Software einsetzen zu müssen. Werden beispielsweise jeweils spezielle Programme zur Ablage von Büchern, DVDs, Notizen, Unterlagen, Dateien und von Web-Lesezeichen (“bookmarks ”) eingesetzt, so kann es sein, daß in den Programmen Begriffshierarchien parallel gepflegt und abgeglichen werden müssen. Dies führt entweder zu erheblichen Mehraufwand oder zu einem Auseinanderlaufen der verschiedenen Ablagesysteme. Um eine Information zu einem Thema zu finden, wären dann die verschiedenen Systeme hintereinander zu befragen. Wird wegen des Aufwandes darauf verzichtet, so werden Informationen einer bestimmten Form übersehen.
Daher sollte es angestrebt werden, nur ein einziges  System zur Ablage jeglicher Art von Information zu verwenden.
Werden Informationen zu einem bestimmten Themen gesucht, dann ist dem Rechercheur das Medium, über das die Informationen zu ihm kommen, meist egal. Ein Ablagesystem, das alle möglichen Medien enthält, kann bei einer Suchanfrage beispielsweise Webseiten, lokale Dateien und erfaßte Bücher anzeigen und dem Rechercheur dann die weitere Auswahl erlauben. Mehrere Ablagesysteme für verschiedene Medientypen getrennt hintereinander befragen zu müssen ist viel mühevoller und kann auch dazu führen, daß aus Zeitmangel nur in einigen Systemen recherchiert wird und so einige Medien übersehen werden. 
Kategoriebildung und -ordnung
Es ist möglich, mehrere Informationseinheiten mit einer bestimmten Gemeinsamkeit in einer Kategorie  zusammenzufassen. Werden Informationseinheiten in Kategorien abgelegt, so wird jede Informationseinheit mindestens einer Kategorie zugeordnet. Zur Ablage von Informationseinheiten müssen Kategorien aber nicht unbedingt verwendet werden, da benötigte Informationseinheiten auch über Stichwörter wiedergefunden werden können, wenn sie nicht in Kategorien enthalten sind.
Kategorien
Falls Kategorien verwendet werden, sollten sie möglichst eindeutig sein, so daß bei der Ablage oder der Suche einer Information möglichst wenig Zweifel darüber aufkommen, wo eine Information abzulegen oder zu suchen ist. Da in der Regel mehrere Informationsstücke in einer Kategorie gesammelt werden, vermindert sich durch die Kategorisierung die Zahl der auf einer gewissen Abstraktionsstufe zu verwaltenden Einheiten, von der Zahl der Informationsstücke auf die Zahl der Kategorien. Diese quantitative Minderung der durch einfaches Zählen der Einheiten gemessenen Komplexität ist der wesentliche Beitrag von Kategorien gegenüber einem System, das alles Informationsstücke ungeordnet in ein Verzeichnis legt.
 AblageverfahrenSuche die Kategorie, unter der die Einheit vermutlich am häufigsten wieder gesucht wird und ordne sie dieser Kategorie zu. Falls die passende Kategorie noch nicht existiert, lege sie neu an. Falls es verschiedene andere ebenfalls naheliegende Kategorien gibt, lege dort einen Verweis auf die Einheit oder notfalls eine Kopie der Einheit ab.
 SuchverfahrenSuche die Kategorie, die das Gesuchte am besten beschreibt und sichte die in dieser Kategorie vorkommenden Einträge. Falls die gesuchte Information nicht gefunden wurde oder noch mehr Information gewünscht wird, untersuche auch andere, ebenfalls in Frage kommende, Kategorien.
Es zeigt sich, daß es wünschenswert wäre, daß es zu jeder Einheit genau eine zutreffende Kategorie gäbe. Da eine Informationseinheit aber immer in verschiedener Weise interpretiert werden kann, ist das nicht möglich. Dennoch wird man versuchen, wenigstens die Zahl der in Frage kommenden Kategorien möglichst klein zu halten.
Relation-Begriff-Kategorien
Wie kann man Kategorien bilden?
Stefan Ram  benutzt zur Ablage von Informationen Relation-Begriff-Kategorien, also Kategorien, die aus einer Relation und einem Begriff gebildet werden. Dabei wird also festgeschrieben, in welcher Relation die enthaltenen Informationseinheiten zu einem bestimmten Begriff stehen. Dies kann man auch als Aussage interpretieren, wonach die Einordnung der Einheit E in die Kategorie R_B bedeutet, daß die Einheit E in der Relation R zum Begriff B steht.
Dieses System ist feiner als die weiter verbreiteten Begriff-Kategorien. Ein Beispiel soll die Unterscheidung verdeutlichen. Einzuordnen sei ein von Edsgar Djikstra  verfaßter Text und ein Text über Edsgar Djikstra. In einem Begriff-Kategorie-System erfolgte die Einordnung in beiden Fällen unter der Kategorie "Djikstra". Stefan Ram  empfindet aber einen so großen Unterschied zwischen einem Text von  Edsgar Djikstra  und einem Text über  Edsgar Djikstra, daß er es für wünschenswert hält, den ersten in eine Kategorie "von_Djikstra" und den zweiten in eine Kategorie "ueber_Djikstra" einzuordnen. So entstehen also Relation-Begriff-Kategorien, die jeweils eine Relation (hier die Relation "von" und die Relation "ueber") und einen Begriff (hier den Begriff "Djikstra") miteinander verbinden.
Ein System sollte nicht zu fein sein, also zu viele Details der verwalteten Informationseinheiten codieren, weil es dann zu kompliziert wird und sich die Zahl der Abhängigkeiten erhöht. Die Verwendung von Relation-Begriff-Kategorien wird aber als guter Kompromiß zwischen den zu groben Begriff-Kategorien und denkbaren weiteren Verfeinerungen empfunden.
Es zeigt sich, daß Informationseinheiten gemäß ihrer Relation zu einem Begriff anhand weniger Standard-Relation erfaßt werden können. Die Standard-Relation hängen aber letztendlich doch von der Anwendung und den persönlichen Bedürfnissen eines Benutzers ab. Ein Beispiel zu Standard-Relationen findet sich weiter unten bei der Schilderung des Relation-Begriff-Verzeichnissystems.
Ontologische Kategorie-Graphen
Oft besteht das Bedürfnis, die verwendeten Kategorien im Rahmen eines Kategorie-Graphen (einer sogenannten „Ontologie“) weiter zu ordnen, der die Beziehungen der verschiedenen Kategorien untereinander klarstellt. Die Dezimalklassifikation ordnet Begriffe beispielsweise in einem thematischen Baum an.
Solche Kategorie-Graphen wirken zunächst als notwendig und naheliegend, enthalten aber bei näherer Betrachtung viele Komplikationen. Sie müssen zeitabhängig  sein, um an neue Themen angepaßt zu werden, was aber ständige Wartungsarbeiten bedeutet. Die Verwendung eines fertigen  Begriffssystems macht den Benutzer von nicht immer als passend empfundenen Einordnungen Dritter abhängig. Die Herstellung eines eigenen  Begriffssystems ist aufwendig.
Ein Problem ist es dabei, daß die Einordnung eines Begriffs oft nicht eindeutig möglich ist, so daß immer eine gewisse Unsicherheit darüber besteht, wo ein Begriff denn nun einzuordnen oder zu finden ist. Die Pflege und Verwendung eines Kategorie-Graphen bereitet oft viel Arbeit und Kopfzerbrechen.
Es zeigt sich aber, daß es möglich ist, Kategorien ohne  Kategorie-Graphen zu verwenden. Dabei stehen alle Kategorien einfach gleichberechtigt nebeneinander. Die Verwendung solch eines „Nicht-Systems“, d.h. der Verzicht auf einen festen Kategorie-Graphen entkoppelt die Verwaltung der Kategorien von einem Kategorie-Graphen und erlaubt es damit auch ganz ohne Kategorie-Graphen zu arbeiten, womit natürlich auch der damit verbundene Aufwand entfällt. Ein jedem bekanntes Beispiel eines solchen Ablagesystem ist ein Lexikon: Dort stehen alle Einträge gleichberechtigt nebeneinander, sie sind nur alphabetisch geordnet, aber nicht beispielsweise hierarchisch angeordnet. Dadurch sind alle Begriffe unabhängig von speziellen Auffassungen über ihre hierarchische Einordnung auffindbar.
Wer ontologische Begriffsgraphen schätzt, kann zu solch einem entkoppelten Kategoriesystem dann immer noch später ein oder mehrere Kategorie-Graphen hinzufügen. (Das nennt man heute auch manchmal eine “topic map ”.) Das ist vergleichbar mit einem Kategorie-Graphen, dessen Begriffe dann im Lexikon nachgeschlagen werden können: Beides ist auch getrennt voneinander benutzbar. Wichtig ist es aber, die Funktionalität der Kategorien nicht von einem speziellen Kategorie-Graphen abhängig zu machen, weil dadurch viel Komplexität, Abhängigkeit und Wartungsaufwand importiert wird.
Denotative Begriffsgraphen
Denotative Begriffsgraphen versuchen nicht eine ontologische Relation zwischen verschiedenen Begriffen zu etablieren, sondern beschränken sich auf die Aufgabe Namensräume  zu verwalten. Das ist vergleichsweise einfacher und eindeutiger. Ein naheliegender Typ eines denotativen Begriffsgraphens ist eine einfache Mengen von Namensräumen mit Namen.
So ist es beispielsweise wünschenswert, in einem Ablagesystem zwischen der Insel „Java “ und der Programmiersprache „Java “ zu unterscheiden. Dies kann dadurch geschehen, daß in dem Ablagesystem zwei verschiedenen Namensräume geschaffen werden. So gäbe es dann beispielsweise den Namensraum "Insel" und den Namensraum "Programmiersprache". Die beiden Begriffe könnte dann beispielsweise als Kategorie "Java_Insel" und als Kategorie "Java_Programmiersprache" abgelegt werden.
Mehrfach belegte Namen können in automatischen Systemen durch Numerierung unterschieden werden. Gibt es beispielsweise noch eine weitere Insel „Java “ neben der berühmten indonesischen Insel, so wird diese durch den Namen "Java_Insel_1" bezeichnet, die nächste Insel mit demselben Namen durch den Namen "Java_Insel_2", u.s.w.. Es kann aber auch sinnvoll sein, hinter dem Namen weiterer Java-Inseln einen erklärenden Text (weiteren Namensraum) anzufügen, wie etwa bei der hypothetischen Insel "Java_Insel_Ostsee".
Kategorienormale
Wenn Kategorien nicht in einer Systematik oder in einem semantischen Netz gefunden werden können, weil sie wie in einem Lexikon alle gleichberechtigt nebeneinander stehen, dann spielt der Name der Kategorien aber eine große Rolle bei der Identifikation eines Kategorie.
Um Kategorien leicht und eindeutig über ihren Namen finden und identifizieren zu können, ist es sinnvoll, eine Normalform  zu verwenden. Beispielsweise sollte es geklärt werden, ob grundsätzlich Deutsch oder Englisch  verwendet wird, damit klar ist, ob eine Information zum Thema „Fernsehen“ unter der Kategorie "about_television" oder unter der Kategorie "ueber_fernsehen" abgelegt wird. Genauso kann festgelegt werden, daß grundsätzlich keine Abkürzungen verwendet werden, um nicht eine Kategorie "about_tv" und später noch versehentlich eine weitere Kategorie "about_television" für denselben Zweck anzulegen. Außerdem könnte beispielsweise festgelegt werden, daß nur Substantive  für Kategorien stehen und grundsätzlich der Singular des Nominativs  zu verwenden ist (Andererseits kann es auch sinnvoll sein, den Plural als bedeutungstragendes Element einzusetzen, weil Informationen über die Freiheitsstatue  etwas anderes sind als Informationen über Freiheitsstatuen.) Bei der Verwendung von Namensräumen muß die Reihenfolge zwischen Namensraum und Element  festgelegt werden, so kann beispielsweise "Insel_Java" und "Programmiersprache_Java" oder "Java_Insel" bzw. "Java_Programmiersprache" verwendet werden.
Schließlich bleibt noch das Problem der Synonymie, das durch Verweise gemildert aber schwer vollständig durch Normalisierung gelöst werden kann.
Beispiele konkreter Systeme
Das Relationen-Begriff-Verzeichnissystem
Als Beispiel eines Ablagesystems, das einige der bisher beschriebenen Ideen verwendet, sei das von Stefan Ram  verwendete Relationen-Begriff-Verzeichnissystem vorgestellt: Informationen werden dabei in Verzeichnisse abgelegt, die Relationen-Begriffs-Kategorien entsprechen.
Zunächst einmal gibt es einige wenige grundlegende Relationen, die durch Kurzbezeichner (Buchstaben) benannt sind und von denen einige im folgenden beispielhaft aufgelistet werden. In der folgenden Liste wird der Begriff, nach dem die Kategorien innerhalb einer Relation gebildet werden, durch „X “ bezeichnet. (Das folgende Kategoriesystem wurde gegenüber dem tatsächlich verwendeten leicht vereinfacht.)
 aabout —Information über  den Begriff X. Damit enthält beispielsweise das Verzeichnis "a/Deutsch" Informationen über  das Thema Deutsch (in diese Fall also über die Sprache  Deutsch).
 bby —Information von  dem Autor X. Damit enthält beispielsweise das Verzeichnis "b/Deutsch" Texte vom  Autor Deutsch.
 fForm —Inhalte der Form X  (das kann auch eine natürliche oder formale Sprache sein). So enthält das Verzeichnis "f/Deutsch" beispielsweise Texte in der Sprache  Deutsch.
 jproject —Unterlagen zum Projekt X. Damit enthält beispielsweise das Verzeichnis "j/Deutsch" Dateien zum  Projekt Deutsch. (Projektwissen, Prozeßwissen, Strukturwissen, Steuerungswissen)
 pperson —Informationen über die Person X. Damit enthält beispielsweise das Verzeichnis "p/Deutsch" Texte über  die Person Deutsch. Die Abgrenzung zum Modul „a“ ist hier nicht immer ganz einfach und so kann auch auf das Modul „p“ verzichtet werden, so daß Informationen über Personen auch unter dem Modul „a“ abgelegt werden. (Personenwissen)
Für Projekte gibt es noch vereinheitlichte Unterverzeichnisnamen:
 j/Deutsch/inincoming —Eingang zum Projekt „Deutsch“. Dateien, die im Rahmen des Projekts weiter zu verarbeiten sind.
 rrelation —Unterlagen zur Beziehung mit der Person X. Damit enthält beispielsweise das Verzeichnis "r/Deutsch" Dateien zur  Beziehung mit der Person Deutsch. Während der Bereich p Informationen über Personen aufnimmt, auch wenn keine Beziehung zu ihnen besteht, nimmt der Bereich r Informationen zu Personen auf, zu denen eine Beziehung besteht.
Für Beziehungen gibt es noch vereinheitlichte Unterverzeichnisnamen:
 r/Deutsch/inincoming —Eingang von der Person Deutsch.
 r/Deutsch/outoutbound —Ausgang an die Person Deutsch.
 r/Deutsch/loglog —Aufzeichnungen zum Kontakt mit der Person Deutsch.
Darüber hinaus reserviert das System alle Namen aus einzelnen Buchstaben für seine Zwecke und definiert noch die Bedeutung folgender Buchstaben.
 wDie Bedeutung dieses Buchstabens wird nie durch das System festgelegt werden, so daß ein Anwender sie selber definieren kann, um das System zu erweitern oder anzupassen. 
 zEinige  (nicht weiter bestimmte) mögliche Kategorien treffen zu. Ein Lexikon  behandelt beispielsweise viele verschiedene Themen und könnte daher in das Verzeichnis "a/z" („über Verschiedenes“) abgelegt werden. 
 xEntspricht einer widersprüchlichen Aussage über die Kategorie einer Einheit. Damit ist die Ablage einer Einheit in das Verzeichnis "a/x" per definitionem  fehlerhaft bzw. nicht mehr im Rahmen der durch das Bezeichnungssystem definierten Semantik interpretierbar. Diese Möglichkeit wird eher aus theoretischen Gründen vorgesehen und ähnelt dem Bottom-Element eines Verbandes oder dem Wert NULL einer Datenbank oder der Gleitkommazahl NaN.
 yEntspricht keiner Aussage über die Kategorie einer Einheit. Damit macht die Ablage einer Einheit in das Verzeichnis "a/y" keinerlei Aussage über das Thema. Diese Möglichkeit wird eher aus theoretischen Gründen vorgesehen und ähnelt dem Top-Element eines Verbandes. (Allerdings könnten in der Praxis diese Kategorie durchaus verwendet werden, um Einheiten zu sammeln, die noch feiner zu kategorisieren sind, wenn bisher die Zeit dazu fehlte.)
Jede Informationseinheit kann unter mehreren Kategorien abgelegt werden. Diese Mehrdeutigkeit ist leider kaum zu vermeiden. Die Richtlinie für die Ablage lautet dann, daß eine Informationseinheit vor allem unter der Kategorie abzulegen ist, unter der sie vermutlich am häufigsten wieder gesucht wird. In den Fällen, in denen hier mehrere Kategorien in Frage kommen, wird die Datei in mehreren Kategorien gelegt (dies kann technisch mit Verweisen realisiert werden).
Eine weitere Richtlinie ist es, eine Informationseinheit unter der speziellsten möglichen Kategorie  abzulegen, da diese am meisten Informationen enthält. Ein Lexikon von Goethe könnte bei Verwendung der Relation "a" („über …“) nur in die Kategorie "a/z" (oder die Kategorie "a/y") gelegt werden, weil ein Lexikon nicht ein spezielleres Thema behandelt. Die Einordnung unter der Kategorie "f/Lexikon" oder Kategorie "b/Goethe" kann daher mehr brauchbar Informationen kodieren und ist daher vorzuziehen.
Ein Text von Goethe  über Lavendel könnte sowohl unter der Kategorie "b/Goethe" als auch unter der Kategorie "a/Lavendel" abgelegt werden. Hier sollte man sich dann fragen, warum man diesen Text überhaupt archivieren will. Wenn man den Text deswegen interessant findet, weil er von Goethe  ist, dann sollte man ihn unter die Kategorie "b/Goethe" ablegen, weil man ihn dort vermutlich auch wieder suchen wird. Ist der Text hingegen deshalb für den Benutzer des Ablagesystems interessant, weil er sich mit Lavendel beschäftigt, dann sollte er in die Kategorie "a/Lavendel" gelegt werden. 
Soll das System aber universell nutzbar sein, dann müßte die Informationseinheit unter allen in Frage kommenden Kategorien abgelegt werden, um unnötige Kopien zu vermeiden, wären dann aber Verweise nötig, die zwar einzelne Dateisysteme in der einen oder anderen Form bieten, welche aber nicht portabel sind. (Allerdings kann man Verweise portabel durch Dateien implementieren, was aber nicht von jedem Betriebssystem unterstützt wird.) Damit stößt man an die Grenzen der portablen Fähigkeiten eines Dateisystems zur Ablage von Informationen.
Beispiel eines Relationen-Begriff-Verzeichnissystems
Das folgende Beispiel eines Relationen-Begriff-Verzeichnissystems soll der Veranschaulichung dienen. Es handelt sich um eine hypothetische Sammlung von Dateien und Verzeichnissen. Namen von Verzeichnissen enden mit einem Schrägstrich "/", alles andere sind Dateinamen. Kommentare zu den einzelnen Verzeichnissen sind mit der Zeichenfolge " -- " eingeleitet. Diese Kommentare sind kein Teil des Namens des Verzeichnisses, sondern nur hier zur Erläuterung hinzugefügt.
Relationen-Begriff-Verzeichnissystem 
r/

  a/ -- about: ueber ein bestimmtes Thema

    1978 - Jahr/ -- ueber das Jahr "1978"
      26_ Oktober 1978 Schnalle am Breitscheidplatz.htm

    and - englisches Wort/ -- ueber das englische Wort "and"
      Herkunft.htm

    and - deutsche Wortendung/ -- ueber die deutsche Wortendung "-and"
      Bedeutung.htm

    and - Suchmaschinenoperator/ -- ueber den Suchmaschinenoperator "and"
      Einsatzgebiete.htm

    Bildschirmarbeit - Thema/ -- ueber Bildschirmarbeit
      gesundheitliche_Folgen.htm
      ERGOnomie - FAQ.htm

    de - Domain/ -- ueber den Bereichsnamen "de"
      heise online Zehn Jahre DENIC.htm

    de.etc.sprache.deutsch - Newsgroup/ 
    -- ueber die Newsgroup "de.etc.sprache.deutsch"
      10 Jahre desd.htm

    Dr. Werner Buchholz - Person/ -- ueber Dr. Werner Buchholz
      Werner Buchholz.htm
      werner.jpg

    entry.de - site/ -- uber den Web-Dienst "entry.de"
      Aufbau von Entry.DE.html

    ECMAScript - Notation/ -- ueber ECMAScript
      Ecma-262.pdf

    Ted Nelson - Person/ -- ueber Ted Nelson
      Ted Nelson and Xanadu.htm

    Zahlensysteme - Thema/ -- ueber Zahlensysteme
      Leibniz Binaerzahlen.htm

  b/ -- by: von bestimmtem Autor oder aus einer bestimmten Quelle

    de.etc.sprache.deutsch/ -- Texte aus der Runde "de.etc.sprache.deutsch"
      Adjektivflexion.htm

    Francis Bacon/ -- Texte von Francis Bacon
      Advancement of Learning (1640).htm

    Goethe/ -- Texte von Goethe
      faust1.txt
      faust2.txt

    The Incredible String Band/ -- Texte der Gruppe "The Incredible String Band"
      The Incredible String Band Lyrics.htm

    Tim Berners Lee/ -- Texte von Tim Berners Lee
      The original proposal of the WWW.htm

  d/ -- documents: Nicht einem bestimmten Projekt zugeordnete 
     -- bearbeitete Dokumente, Werkstücke, Texte und Dateien.

  e/ -- entity: ein Werk oder Werkauszug unter seinem Eigennamen abgelegt

    Bibel/
      Bibel.txt -- Text der Bibel

    La Donna é mobile/
      La Donna é mobile -- Text der Arie

  f/ -- form: ein Werk in einer bestimmten Form oder Sprache

    ASCII-Art/
      Muster.txt
      Tiere.txt

    Anagramme/
      Ein-Wort-Anagramme.htm

    Aphorismen/
      Aphorismen.htm

    Aufzeichnungen/

      E-Mail/

        Ausgang_bis_20030407.txt

        Eingang_bis_20030412.txt

        Eingang_bis_20040622.txt

      Musterbank/

        Kontoauszuege/

    C++/ -- Quelltexte in der Sprache "C++"
      Vollkommene_Zahlen.cpp
      Boost/
      Loki/

  g/ -- generator: (ein Archiv für )ein unter einer bestimmten
     --   Plattform ausführbares Werk, abgelegt nach der Plattform
     --   und manchmal noch nach der Werkgattung.
     --   Es handelt sich aber nicht um "installierte" Werke,
     --   sondern um installierbare Werke.

    Windows/
      antivirus
        avg6607fu_free.exe
      PDF/
        AcroReader51_ENU.exe
      programming/
        doxygen-1.3.6-setup.exe

    Java/
      JUNIT3.ZIP

  i/ -- incoming: Eingangskorb: Inhalt ist weiter zu verteilen 
     -- oder abzulegen


  j/ -- Projekte: In Bearbeitung befindliche Dateien eines 
     -- Projekts und Materialien zu einem Projekt oder Produkt
     -- Kritiken, Kommentare und Reaktionen zu Produkten

    Textanalyse/
      analyse.c
      analyse.o
      analyse.exe
      Makefile
      todo.txt

  r/ -- Beziehungen: Materialien und Nachrichten

    FU Berlin/
      Email_vom_2003-12-20.txt
      Antwort_2003-12-21.txt

  s/ -- Software: "installierte" Software

    GIMP/

    Tcl/

  v/ -- Variablen: Variablen (Ablage, Dateien) bestimmter Software
Einige wünschenswerte Funktionen
Volltextsuche
Kein Kategoriesystem ist so perfekt, daß jede  Information darüber immer sicher und schnell gefunden werden kann. Daher ist eine gute Möglichkeit zur schnellen Volltextsuche unersetzlich. Es ist schon das meiste gewonnen, wenn schnell alle Informationseinheiten gefunden werden können, in denen eine bestimmte Zeichenfolge vorkommt. Natürlich sind auch komfortablere Suchprogramme mit der Möglichkeit komplizierterer Anfragen zu schätzen, wie sie schon Bestandteil mancher Büroprogramme sind. Perfekt wäre ein System, das Texte auch in komprimierten Dateien und den verschiedensten Formaten findet und auch verschiedene Wortformen oder Synonyme kennt.
Erfreulicherweise erlauben viele Betriebssysteme heute schon Grundformen der Textsuche im Dateisystem. Auch mit relationalen Datenbanken sind solche Suchen möglich. Daher ergibt sich hieraus zunächst keine unbedingte Notwendigkeit, ein spezielles Programm zu erwerben, denn schon eine einfache Suchmöglichkeit erlaubt das Auffinden der meisten relevanten Informationseinheiten, während zusätzliche Spezialfunktionen seltener benötigt werden.
Suchprogramme, die es erlauben, Dateien verschiedener gängiger Dateitypen nach Wörtern zu untersuchen, und dabei Mustersuchen, logische Verknüpfungen, mehrere Suchkriterien, unscharfes oder phonetisches Suchen, Suchen nach Wortvarianten oder Synonymen anbieten, sind allerdings ohne Zweifel eine nützliche Investition. Im Vergleich zu Programmen, die zu verwaltende Daten in ihr eigenes spezielles Format umwandeln, ist es bei Verwendung solche Suchprogramme beruhigend zu wissen, daß die Lesbarkeit der Dateien auch ohne diese Suchprogramme weiterhin gewährt bleibt.
Einzelne Techniken
Behälterbeschriftungen
Das Prinzip der „Behälterbeschriftung“ ist ein technischer Trick, der es erlaubt jedes verpackbare Objekt zu beschriften: Wenn ein Objekt nicht beschriftet werden kann oder beschriftet werden soll, dann wird es in einen Behälter gepackt und der Behälter wird beschriftet. Dieser Trick ist bei der Ablage an verschiedenen Stellen hilfreich: Wenn eine Datei mit einem Kommentar versehen werden soll, aber das Betriebssystem keine Funktion für diesen Zweck bietet (die gegebenenfalls ja auch nicht portabel wäre), dann wird die Datei in ein Verzeichnis (als Behälter) gelegt, dessen Name dann den Kommentar darstellt. Wenn ein wichtiges physikalisches Schriftstück (ein Blatt Papier) beschriftet werden soll, aber es nicht beschriftet werden darf, um es nicht zu beschädigen, dann wird es in einen Umschlag gelegt, der dann beschriftet werden kann. 
Umgekehrt können unbeschriftbare Behälter durch ihre Inhalte beschriftet werden: Wenn der Name eines Verzeichnisses dieses nicht ausreichend beschreiben kann oder nicht verändert werden darf, so kann festgelegt werden, daß in jedem Verzeichnis eine Datei "dirinfo.txt" weitere Informationen zu diesem Verzeichnis enthält. Physikalisch entspricht das der „Beschriftung“ eines Umschlages durch einen hineingelegten Zettel.
(Zu diesem Abschnitt erreichte mich eine Mitteilung, die am Ende dieses Artikels zu finden ist.)
Freie Beschriftungen
Behälter, besonders physikalische Behälter (wie Briefumschläge, Schubfächer oder Kartons), die zur Ablage verwendet werden, werden bei der Beschriftung frei von allen Angaben zu ihrem Inhalt gehalten und nur durch einen künstlichen eindeutigen Primärschlüssel individualisiert, also beispielsweise mit einer laufenden Nummer durchnumeriert. In einer Datei notiert man dann, was in welchem Behälter enthalten ist. 
Dieses Verfahren hat den Vorteil, daß Änderungen der Widmung (des Soll-Inhalts) eines Behälters nur durch die leicht möglichen Änderung an der Datei erfolgen können, während die physikalische Beschriftung immer gleich bleiben kann, da diese den Behälter und nicht seinen Inhalt kennzeichnet. Außerdem kann in einer Datei leicht automatisch nach Stichwörtern gesucht werden, was bei physikalischen Behälterbeschriftungen nicht so einfach ist.
Ein Nachteil dieses Verfahrens ist es, daß ein zusätzlicher Schritt nötig ist, um gezielt auf einen Behälter zuzugreifen. Sind beispielsweise alle Stehordner nur durchnumeriert und deren Inhalt erst in einer Datei beschrieben, dann wird der Zugriff schwierig, wenn das Rechnersystem ausgefallen ist.
Medienbeschriftungen
Bestimmte Medien, wie Bilder oder Klänge, sind einer Volltextsuche nicht direkt zugänglich. Zwar sind Verfahren entwickelt worden, um in Beständen solcher Medien nach Ähnlichkeit zu suchen, doch ist manchmal eine Textsuchmöglichkeit sehr wünschenswert. Auch in diesem Fall kann natürlich das Prinzip der Beschriftung  wieder verwendet werden: Dem Medium soll ein Text zugeordnet werden, unter dem es später wieder gefunden werden kann. 
Ein Nachteil dieser Vorgehensweise, ist der Aufwand, den es bedeutet, wenn ein Mensch einen großen Medienbestand sichtet und zu jedem einzelnen Medium passende Schlagwörter eingeben soll. Damit das Ergebnis wenigstens dauerhaft erhalten bleibt, sollte versucht werden, die Beschriftung möglichst so anzubringen, daß sie bewahrt bleiben kann, wenn das System gewechselt werden muß. Spezielle Programme zur Medienverwaltung sollten daraufhin überprüft werden, ob sie den Benutzer in eine Abhängigkeit von diesem speziellen System bringen oder ob der Zugriff auf die Texte auch ohne diese Programme möglich bleibt.
Ganz ohne spezielle Software ist es möglich, einige wenige Stichwörter im Dateinamen  von Mediendateien unterzubringen. Das ist recht bequem, da der Dateiname aber eigentlich anderen Aufgaben dient, ist diese Vorgehensweise nicht empfehlenswert. Eine bessere Möglichkeit ist es, zu jeder Mediendatei eine beschreibende Textdatei anzulegen. Zur Bilddatei "bar.png" gehört dann beispielsweise die Textdatei "bar.txt", die als erste Zeile den Namen der Bilddatei und dann Informationen über das Bild, wie z.B. Stichwörter enthält. Bei Änderungen des Namens einer Mediendatei muß dann darauf geachtet werden, die Textdatei entsprechend anzupassen. Für die Textdatei können dann mehr oder weniger ausgefeilte Formate definiert werden. Jedenfalls kann die Textdatei dann mit jedem Textsuchprogramm gefunden werden, und damit ist dann über die Gleichheit des Namensteils vor dem Punkte "." auch die zugehörige Mediendatei gefunden. Solche Textdateien sind natürlich wieder recht portabel, das heißt: Sie können bei einem Wechsel des Systems mitgenommen werden und stellen keine Bindung an ein spezielles Softwareprodukt dar.
Detaillierteres Beispiel eines Verzeichnissystems
detaillierteres Relationen-Begriff-Verzeichnissystem 
      r/                            Wurzel

        a/                          about ..., ueber Thema ... (nach Namen)

        b/                          by ..., von Autor ... (nach Namen)

        e/                          entity ..., Objekt ... (nach Namen)

        f/                          form ..., Form

*       f/bookmarks                 - Lesezeichen

* +     f/log                       - Aufzeichnung/Protokoll

* +     f/log/email                 - - Datennachrichten

* +     f/log/email/in              - - - empfangene Nachrichten

* +     f/log/email/out             - - - gesendete Nachrichten

* +     f/log/mail/out              - - - gesendete Briefe

* +     f/log/usenet                - - - gesendete Usenet-Beitraege

* +     f/log/beleg                 - - Belege

* +     f/log/beleg/Bank A          - - - Belege von der Bank A

        i/                          incoming, Eingang (noch abzulegen)

* +     j/                          Projekt

        p/                          Person ... (nach Namen)

* +     r/                          relation ..., Beziehung ... (nach Namen)

* +     s/                          software ..., installierte Software

  +     v/                          variable ..., Programmdaten

  + ?   w/                          word ..., Wort ... (im Klientenbereich)





        f/g                         - generator ..., Archiv/Software

    ?   f/C++                       - C++-Programme

    ?   f/Aufgaben zu C++           - C++-Aufgaben

    ?   f/Woerterbuch               -

    ?   f/Gitarrennoten             - 

    ?   f/jpg                       - 

    ?   f/ico                       - 

    ?   f/Italienisch               - 

    ?   f/Lyrics                    - 

    ?   f/RFC                       - 


Kommentare zu dieser Seite
 Von Maria S. 
Zu Die Ablage von Informationseinheiten, Abschnitt Behälterbeschriftung/ Medienbeschriftung:
Um einfach eine Textdatei zu einer beliebigen Datei zu erzeugen, kann man das Freeware-Programm FileNote (http://www.moonsoftware.com/freeware.asp) benutzen. Im Kontext Menü für eine Datei kann man dann auf FileNote klicken und eine Textdatei gleichen Namens wird erzeugt und kann bearbeitet werden (existierende werden aufgerufen).
Das Programm kann man auch "händisch" auf Ordner erweitern, in dem man in der Windows Registry unter 
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\Folder\shellex\ContextMenuHandlers
einen neuen Schlüssel erzeugt (z. B. FileNote) und als Standardwert denselben Wert eingibt, den das Programm unter
KEY_CLASSES_ROOT\*\shellex\ContextMenuHandlers\FileNote
schreibt, z. B. {9EDB82E0-C19C-11D1-A59F-00609725CF78}
Damit steht das Programm auch unter Ordner zu Verfügung. Für das Programm gibt es eine Hilfe in Form einer Readme.txt, in der man auch nachlesen kann, wie man einen bestimmten Editor für die Notizen einstellen kann (empfehlenswert besonders NoteTab Light (Freeware) oder NoteTab Pro (Shareware): http://www.notetab.com/download.php)).
Zur komfortablen Verwaltung / Erzeugung von Textdateien zu Dateien eignet sich auch das folgende Freeware-Open Source Programm: http://tombo.sourceforge.jp/En/, mit dem man Textdateien erzeugen kann und Suche nach Textinhalten durchführen kann. Sollte der Texteditor von Tombo irgendwann einmal Hyperlinks unterstützen, so könnte man dieses Programm als "Zentrale" nehmen.
Grüße, Maria S?Rest des Nachnamens ?

Quelle: http://userpage.fu-berlin.de/~ram/pub/pub_w33d45lg/informationsverwaltung_ablage_de  (am 14.02.2005 um 10:33 Uhr)





## null

WWW: http://www.purl.org/stefan_ram/pub/informationsverwaltung_ablage_de [ID 7]

