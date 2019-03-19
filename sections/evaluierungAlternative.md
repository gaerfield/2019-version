<!--s-->
## Untersuchung der Alternative

<!--v-->
### Eindeutige Ordnung I

* `01.13.00.01` < `01.13.00.02` ?
  * <!-- .element: class="fragment" data-fragment-index="1" -->  Neu: `19.1-F2583-1` $\neq$ `19.1-F2326-1`
  * <!-- .element: class="fragment" data-fragment-index="1" -->  zwei unterschiedliche Features, keine Gemeinsamkeiten (außer 19.1)

<!--v-->
### Eindeutige Ordnung II

* `01.13.00.01` < `01.13.00.08` ?
  * <!-- .element: class="fragment" data-fragment-index="1" --> Neu: `19.1-F2583-1` $\neq$ `19.1.0-rc8`
  * <!-- .element: class="fragment" data-fragment-index="1" --> keine Aussage darüber, ob das Feature bereits im Release enthalten ist: nachschauen ([WAVEX-2583](https://jira.eudemonia-solutions.de/browse/WAVEX-2583))

<!--v-->
### Eindeutige Ordnung III

* `01.13.00.02` < `01.13.00.08` ?
  * <!-- .element: class="fragment" data-fragment-index="1" --> Neu: `19.1-F2326-1` $\neq$ `19.1.0-rc8`
  * <!-- .element: class="fragment" data-fragment-index="1" --> keine Aussage darüber, ob das Feature bereits im Release enthalten ist: nachschauen ([WAVEX-2326](https://jira.eudemonia-solutions.de/browse/WAVEX-2326))

<!--v-->
### Änderungsumfang I

* `01.12.10.07` und `01.12.10.08`
  * Erwartung: wenige Änderungen, da geringste Versionsnummer erhöht
  * <!-- .element: class="fragment" data-fragment-index="1" --> neu: `18.2.11-rc7` und `18.2.11-rc8`
  * <!-- .element: class="fragment" data-fragment-index="1" --> korrekt: zwei direkt aufeinander folgende Testversionen
  * <!-- .element: class="fragment" data-fragment-index="2" --> die richtige Zielversion ist Teil der Versionsnummer (Testversion für 11. - nicht 10. - Update)

<!--v-->
### Änderungsumfang II

* `01.13.00.02` und `01.13.00.08`
  * Erwartung: wenige Änderungen, da geringste Versionsnummer erhöht
  * <!-- .element: class="fragment" data-fragment-index="1" --> neu: `19.1-F2326-1` und `19.1.0-rc8`
  * <!-- .element: class="fragment" data-fragment-index="2" --> potentiell viele Änderungen (möglicherweise auch gar keine, weil bereits in 19.1.0 enthalten)
  * <!-- .element: class="fragment" data-fragment-index="3" --> definitiv keine DB-Schema-Änderungen (neue Tabellen, etc.)

<!--v-->
### Änderungsumfang III

* `01.12.10.09` und `01.12.11.00`
  * Erwartung: viele Änderungen, da minor-Version von 10 auf 11 wechselt
  * <!-- .element: class="fragment" data-fragment-index="1" --> neu: `18.2.11-rc9` und `18.2.11`
  * <!-- .element: class="fragment" data-fragment-index="1" --> potentiell wenig (möglicherweise keine) Änderungen

<!--v-->
### Unterscheidung Release/Test-Version I

* `01.12.10.09`- Testversion: letzte Ziffer $\neq$ 0
  * <!-- .element: class="fragment" data-fragment-index="1" --> neu: `18.2.11-rc9`
  * <!-- .element: class="fragment" data-fragment-index="1" --> korrekte Ziel-Version als Teil dieser Version
* `01.12.00.00`- 1. Auslieferung für CC 18-2
  * <!-- .element: class="fragment" data-fragment-index="2" --> neu: `18.2.0`
* `01.12.11.00`- 11. Update für CC 18-2 (Auslieferung)
  * <!-- .element: class="fragment" data-fragment-index="3" --> neu: `18.2.11`

<!--v-->
### Unterscheidung Release/Test-Version II

* `01.12.10.09` - Testversion `18.2.11-rc9`
* `01.12.10.10` - Hotfix: `18.2.10-hf1`<!-- .element: class="fragment" data-fragment-index="1" -->
* `???` - Patch: `18.2.10-p1`<!-- .element: class="fragment" data-fragment-index="1" -->
* für Endanwender könnten wir Anzeige des Suffix streichen, so dass dort nur 18.2.10 angezeigt wird (sinnvoll?)

<!--v-->
### Unterscheidung Release/Test-Version III

* Sonderfall: Build auf Integrationszweig
  * `01.12.11.24` wurde direkt auf 18-2 erstellt
  * <!-- .element: class="fragment" data-fragment-index="1" --> `18.2-18.2-24` entsprechend Schema `[CC-Release]-[Branch]-[X]` irgendwie komisch
  * <!-- .element: class="fragment" data-fragment-index="1" --> Nutzung eines Namenkürzels `i` (Integration) `[CC-Release]-i[X]`: `18.2-i24`?

<!--v-->
### Zeitpunkt einer Auslieferung

* `01.12.10.00` CC-Release 18-2:`18.2.10`<!-- .element: class="fragment" data-fragment-index="1" -->
* `01.09.04.00` BSA-Release 5.9.0: `590.4`<!-- .element: class="fragment" data-fragment-index="1" -->

<!--v-->
### Builds ohne Versionsnummernvergabe

* Nightly-Build:
  * bisher: `01.13.00.15-4-e26ceae10775-Feature-WAVEX-2326`
  * neu: `19.1.0-rc15-4-e26ceae10775-Feature-WAVEX-2326`
  * nightly auf einem Integrationszweig: `19.1.0-rc15-4-e26ceae10775-19.1`
* Builds durch einen Entwickler: `blaschke-d88bbdcbb4f5-WAVEX-3134`

<!--v-->
### Zusammenfassung

* eindeutige Ordnung <span class="fragment" data-fragment-index="1">**erfüllt**</span>
  * <!-- .element: class="fragment" data-fragment-index="1" --> `19.1-F2583-1` $\neq$ `19.1.0-rc8`
  * <!-- .element: class="fragment" data-fragment-index="1" --> `19.1.0-rc8` < `19.1.0`
* Änderungsumfang <span class="fragment" data-fragment-index="2">**erfüllt**</span>
  * <!-- .element: class="fragment" data-fragment-index="2" --> `19.1.0-rc8` < `19.1.0`
* Version für Produktion oder Test <span class="fragment" data-fragment-index="3">**erfüllt**</span>
  * <!-- .element: class="fragment" data-fragment-index="3" --> `18.2-F253` < `19.1.0-rc8` < `19.1.0` < `19.1.1`
* Auslieferungszeitpunkt <span class="fragment" data-fragment-index="4">**erfüllt**</span>
  * <!-- .element: class="fragment" data-fragment-index="4" --> `19.1.0` wurde für CC-Release 19.1 ausgeliefert
