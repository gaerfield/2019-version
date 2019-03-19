<!--s-->
## Alternativ-Vorschlag

<!--v-->
### Regeln I

* Unterscheidung zwischen:
  * Auslieferungen (an BMS oder Rechenzentrum)
  * Auslieferungen zu QA-Zwecken (an BMS oder Testinstanzen des RZ)
  * regulären/spontanen Builds (bspw. Nightly)

<!--v-->
### Regeln II - Auslieferungen

* Schema: `[CC-Release].[Update]`
  * Kopplung an das CC-Release, da Auslieferung **immer** zu genau einer CC-Version
  * Update: laufende Nummer zu einem Release
  * Hotfix: sollten wie Update behandelt werden
  * Sonderfall Patches: werden in Echtsystemen nicht angezeigt
    * ließe sich "versteckt" (unsichtbar für Endanwender) hinterlegen

<!--v-->
### Regeln III - Auslieferungen zwecks QA
* Schema: `[CC-Release].[Update]-[Suffix]` zusätzliche Charakterisierung über Suffix
  * **p** - patch: werden in Echtsystemen nicht angezeigt
  * **rc** - release-candidate: Testversion an BMS oder Rechenzentrum
  * **F[ABCD]-[X]**: die Xte Testversion des Features ABCD an BMS
    * alternativ **F[ABCD]-[Featurename]-[X]**
  * **i[X]**: die Xte Testversion eines Integrationszweigs

<!--v-->
### Regeln IV - Builds ohne explizite Version

* können nicht an einem Issue hinterlegt werden
* Nutzung von Metadaten als Versionskennzeichnung
  * statt Tag wird commit-Informationen genutzt
  * Schema des **Nightly**: `[letzter Tag]-[Anzahl Commits seit letztem Tag]-[commit-Hash]-[Branch-Name]`
  * Schema für **Entwickler-Builds**: `[autor]-[commit-Hash]-[Branch-Name]`
* wird aktuell bereits so durchgeführt ([10080](http://tomcat-srv-d8.eudemonia-solutions.de:10080/MinD_banker_wave/wave/version))
