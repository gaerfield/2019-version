<!--s-->
## Untersuchung der Alternative

<!--v-->
### Eindeutige Ordnung I

* `01.13.00.01` < `01.13.00.02` ?
  * Neu: `19.1-F2583-1` $\neq$ `19.1-F2326-1`
  * zwei unterschiedliche Features, keine Gemeinsamkeiten

<!--v-->
### Eindeutige Ordnung II

* `01.13.00.01` < `01.13.00.08` ?
  * Neu: 19.1-F2583-1 $\neq$ 19.1.0-rc8
  * keine Aussage darüber, ob das Feature bereits im Release enthalten ist: nachschauen ([WAVEX-2583](https://jira.eudemonia-solutions.de/browse/WAVEX-2583))
* `01.13.00.02` < `01.13.00.08` ?
  * Neu: 19.1-F2326-1 $\neq$ 19.1.0-rc8
  * keine Aussage darüber, ob das Feature bereits im Release enthalten ist: nachschauen ([WAVEX-2326](https://jira.eudemonia-solutions.de/browse/WAVEX-2326))

<!--v-->
### Änderungsumfang I

* `01.12.10.07` und `01.12.10.08`
  * 18.2.10-rc7 und 18.2.10-rc8
  * wenige Änderungen, da geringste Versionsnummer erhöht
  * korrekt: zwei direkt aufeinander folgende Testversionen

<!--v-->
### Änderungsumfang II

* `01.13.00.02` und `01.13.00.08`
  * 19.1-F2326-1 und 19.1.0-rc8
  * wenig Aussagen über Änderungsumfang - keine DB-Änderungen

<!--v-->
### Änderungsumfang III

* `01.12.10.09` und `01.12.11.00`
  * 18.2.11-rc9 und 18.2.11
  * keine Änderungen

<!--v-->
### Unterscheidung Release/Test-Version I

* `01.12.10.09` -> 18.2.11-rc9
  * Testversion: Suffix $neq$ '00' bzw. '50'
* `01.12.00.00` -> 18.2.00
  * Auslieferungsversion: 1. Auslieferung für CC 18-2
* `01.12.11.00` -> 18.2.11
  * Auslieferungsversion: 11. Update für CC 18-2

<!--v-->
### Unterscheidung Release/Test-Version II

* `01.12.10.50`: 18.2.10-hf5 (Hotfix)
* `01.12.10.55`: 18.2.10-hf5-patch1 (Patch)
* Sonderfall: Build auf Integrationszweig
  * `01.12.11.24` -> direkt auf 18-2
  * Schema [CC-Release]-[Branch]-[X] (bspw. 19.1-F2326-1) wäre komisch: `18.2-18.2-24`
  * Einführung eines Namenkürzels `I` = Integration [CC-Release]-I-[X]: `18.2-I-24`

<!--v-->
### Zeitpunkt einer Auslieferung

* `01.12.10.00`? CC-Release 18-2
  * 18.2.10
* `01.09.04.00`? BSA-Release 5.9.0
  * 590.4

<!--v-->
### Builds ohne Versionsnummernvergabe

* Nightly-Build:
  * bisher: `01.13.00.15-4-e26ceae10775-Feature-WAVEX-2326`
  * neu: `19.1.0-rc15-4-e26ceae10775-Feature-WAVEX-2326`
  * nightly auf einem Integrationszweig: `19.1.0-rc15-4-e26ceae10775-19.1`
* Builds durch einen Entwickler: `blaschke-d88bbdcbb4f5-WAVEX-3134`
