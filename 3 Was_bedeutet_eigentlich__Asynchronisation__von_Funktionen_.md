# Was bedeutet eigentlich "Asynchronisation" von Funktionen?

Einige Funktionen nehmen sehr viel Zeit und CPU-Leistung in Anspruch, weil sie den gesamten Datensatz des Zettelkastens bearbeiten oder durchsuchen. Diese Funktionen durchlaufen eine Programmschleife, die erst dann wieder "Rückmeldung" gibt, wenn alles durchgeführt wurde. Dies kann dazu führen, dass der Computer denkt, das Programm sei abgestürzt, weil es sich nicht zurückmeldet. Tatsächlich jedoch arbeitet das Programm immernoch, nur weiß weder der Nutzer noch der Computer, wann das Programm seine Operationen abgeschlossen hat. Mithilfe der Asynchronisation startet das Programm einen zweiten Prozess, der "nebenbei" läuft und den normalen Ablauf des Programms nicht aufhält. Somit gibt das Programm immer Rückmeldung und der Nutzer weiß auch, wie lange er noch zu warten hat.

## null

Programm: Zettelkasten - Homepage, FAQ, http://zettelkasten.danielluedecke.de/ [ID 2]

