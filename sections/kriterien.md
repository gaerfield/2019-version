<!--s-->
## Ziel von Versionsnummern

<!--v-->
### Definition einer Ordnung
* Unterscheidung einzelner Versionen einer Software, um deren Weiterentwicklungen nachvollziehbar zu kennzeichnen
* dafür wird eine Ordnung definiert:
  * Version `13` kam nach Version `10`
  * Version `13` kam vor Version `17`
  * zwischen Version `10` und `17` liegen 6 weitere Versionen
* Je nach Gestaltung sind weitere Informationen in der Versionsnummer eingebettet

<!--v-->
### Umfang der Änderungen
* Vergleichbarkeit anhand höher- und niedrigwertiger Vesionsnummern
  * marginale Änderungen zwischen Versionen `1.0` und `1.1`
  * viele Änderungen zwischen Versionen `1.0` und `1.24`
  * grundlegende Änderungen zwischen Versionen `1.24` und `2.17`

<!--v-->
### Unterscheidung zwischen Versionen für Test und Produktion
* Ein Suffix definiert einen "unreifen" Stand
  * `1.2-alpha1`
  * `1.2`
  * `1.3-beta5`

<!--v-->
### Auslieferungszeitpunkt
* für Software mit festen Auslieferungsterminen wird eine Kombination aus Jahr und Monat genutzt:
  * Ubuntu `18.10`: das zweite Release für des Jahres 2018, veröffentlicht im Oktober
  * CC-Release `18.2`: das 2. Release des Jahres 2018

<!--v-->
### Kriterien

* im folgenden Bewertung des bestehenden Versionierungskonzepts und Alternativvorschlags anhand der folgenden Kriterien:
  * eindeutige Ordnung
  * Umfang der Änderungen zwischen zwei Versionen
  * Version für Produktion oder Test
  * Auslieferungszeitpunkt
