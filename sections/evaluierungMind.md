<!--s-->
## Evaluierung des bestehenden Versionsschemas

<!--v-->
### Eindeutige Ordnung I

* `01.13.00.01` < `01.13.00.02` ?
  * Nein <!-- .element: class="fragment" data-fragment-index="1" -->
    * `01.13.00.01` ist Feature-WAVEX-2583
    * `01.13.00.02` ist Feature-WAVEX-2326
    * befinden sich parallel in Entwicklung und haben nichts miteinander zu tun

<!--v-->
### Eindeutige Ordnung II

* `01.13.00.01` < `01.13.00.08` ?
  * ja  <!-- .element: class="fragment" data-fragment-index="1" -->
    * `01.13.00.01` ist Feature-WAVEX-2583 ist Vereinbarungen in 19.1.0
    * `01.13.00.08` ist Testversion aus 19-1-pilot-01-13-00-10

<!--v-->
### Eindeutige Ordnung III

* `01.13.00.02` < `01.13.00.08` ?
  * <!-- .element: class="fragment" data-fragment-index="1" --> nein: [WAVEX-2326](https://jira.eudemonia-solutions.de/browse/WAVEX-2326) befindet sich noch in Entwicklung  
  *  <!-- .element: class="fragment" data-fragment-index="1" --> es gilt umgekehrt: `01.13.00.08` < `01.13.00.02`
      * `x.08` enthält nichts aus `x.02`
      * `x.02` enthält Änderungen aus `x.08`

<!--v-->
### Änderungsumfang I

* `01.12.10.07` und `01.12.10.08`
  * Erwartung: wenige Änderungen, da geringste Versionsnummer erhöht
  * korrekt: zwei direkt aufeinander folgende Testversionen  <!-- .element: class="fragment" data-fragment-index="1" -->

<!--v-->
### Änderungsumfang II

* `01.13.00.02` und `01.13.00.08`
  * Erwartung: wenige Änderungen, da geringste Versionsnummer erhöht
  * <!-- .element: class="fragment" data-fragment-index="1" --> inkorrekt: viele Änderungen, `01.13.00.02` = Feature-WAVEX-2326

<!--v-->
### Änderungsumfang III

* `01.12.10.09` und `01.12.11.00`
  * Erwartung: viele Änderungen, da minor-Version von 10 auf 11 wechselt
  * <!-- .element: class="fragment" data-fragment-index="1" --> inkorrekt: gar keine Änderung, `01.12.10.09` war die letzte Testversion vor Auslieferung der finalen Version `01.12.11.00`

<!--v-->
### Unterscheidung Release/Test-Version I

* `01.12.10.09` <span class="fragment" data-fragment-index="1">- Testversion: letzte Ziffer $\neq$ 0 </span>
* `01.12.00.00` <span class="fragment" data-fragment-index="2">- 1. Auslieferung für CC 18-2</span>
* `01.12.11.00` <span class="fragment" data-fragment-index="3">- 11. Update für CC 18-2 (Auslieferung)</span>

<!--v-->
### Unterscheidung Release/Test-Version II

* `01.12.10.09` <span class="fragment" data-fragment-index="1">- Testversion: letzte Ziffer $\neq$ '0'</span>
* `01.12.10.10`
  * <!-- .element: class="fragment" data-fragment-index="2" --> Hotfix, da Suffix = 10 (letzte Ziffer eine '0')
  * <!-- .element: class="fragment" data-fragment-index="3" --> Oder ist es doch die 10. Testversionen für `x.11.00`?
  * <!-- .element: class="fragment" data-fragment-index="4" -->  Kollisionen von Testversionen/Hotfixes durch Doppelbelegung der letzten Ziffern


<!--v-->
### Zeitpunkt einer Auslieferung

* `01.12.10.00`? <span class="fragment" data-fragment-index="1">CC-Release 18-2</span>
* `01.09.04.00`? <span class="fragment" data-fragment-index="2">BSA-Release 590</span>

<!--v-->
### Zusammenfassung

* eindeutige Ordnung <span class="fragment" data-fragment-index="1">**nicht erfüllt**</span>
  * Sonderfälle wegen Feature-Branches <!-- .element: class="fragment" data-fragment-index="1" -->
* Änderungsumfang <span class="fragment" data-fragment-index="2">**nicht erfüllt**</span>
  * durch letzte Version vor einer Auslieferung <!-- .element: class="fragment" data-fragment-index="2" -->
* Version für Produktion oder Test <span class="fragment" data-fragment-index="3">**teilweise erfüllt**</span>
  * letzte Ziffer ist doppelt belegt <!-- .element: class="fragment" data-fragment-index="3" -->
  * Kollisionen bei Hotfixes und Patches <!-- .element: class="fragment" data-fragment-index="3" -->
* Auslieferungszeitpunkt <span class="fragment" data-fragment-index="4">**nicht erfüllt**</span>
  * an Versionsnummern nicht ablesbar <!-- .element: class="fragment" data-fragment-index="4" -->
