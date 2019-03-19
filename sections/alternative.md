<!--s-->
## Alternativ-Vorschlag

<!--v-->
### Regeln I

* Unterscheidung zwischen:
  * Auslieferungen (an BMS oder Rechenzentrum)
  * regulären/spontanen Builds (bspw. Nightly)

<!--v-->
### Regeln II - Auslieferungen

* Schema: `[CC-Release].[Update](-[Suffix])`
  * Kopplung an das CC-Release, da Auslieferung **immer** zu genau einer CC-Version
  * Update: laufende Nummer zu einem Release
  * Suffix: zusätzliche Charakterisierung der Auslieferung

<!--v-->
### Regeln II - Auslieferungen

* Suffix: zusätzliche Charakterisierung der Auslieferung
  * **hf**: hotfix
    * werden bei Echtsystemen nicht angezeigt (?)
    * bleiben für Releases in Testsysteme des RZ erhalten
  * **rc** (release-candidate): Testversion an BMS oder Rechenzentrum
  * **F[ABCD]-[X]**: die Xte-Testversion des Features ABCD an BMS
    * alternativ **F[ABCD]-[Featurename]-[X]**

<!--v-->
### Regeln III - Builds ohne explizite Version

* können/sollten nicht an einem Issue hinterlegt als Quellversion hinterlegt werden
* Nutzung von Metadaten als Versionskennzeichnung
  * statt Tag wird commit-Informationen genutzt
  * wird aktuell bereits so durchgeführt ([10080](http://tomcat-srv-d8.eudemonia-solutions.de:10080/MinD_banker_wave/wave/version))
  * Schema des **Nightly**: `[letzter Tag]-[Anzahl Commits seit letztem Tag]-[commit-Hash]-[Branch-Name]`
  * Schema für **Entwickler-Builds**: `[autor]-[commit-Hash]-[Branch-Name]`
