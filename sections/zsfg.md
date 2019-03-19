<!--s-->
## Vorteile

<!--v-->
### Anwender
* Gemeinsamkeit in MinD-Versionsnummer und CC-Release erkennbar

<!--v-->
### Release-Manager
* keine Notwendigkeit der manuellen Pflege der Versionsnummer (Steuerung vollständig über Tag oder Commit)
* Unterscheidung zwischen Testversionen für Feature, Integrationszweig oder Auslieferung
* Unterscheidung zwischen Test- und Produktionsversion (Produktion enthält kein Suffix)

<!--v-->
### QA und Entwickler

* Test- & Zielversion durch `rc`-Suffix konsistent zueinander
* einfache Zuordnung einer Issue-Versionsnummer zu betroffenen Zweigen/Versionen (keine Uminterpretation `01.13` zu `19.1` )
* ob Bug produktiv auftreten kann ist ersichtlich
  * Affects Ver.: `19.1.0-rc5`, Fix Ver.: `19.1.0`
  * Bug wurde in Testversion entdeckt aber vor Auslieferung behoben
* beliebiger Suffix bietet Flexibilität für zukünftige Erweiterungen

<!--v-->
## Motivation: bisher
![](img/vorher.png)

<!--v-->
## Motivation: zukünftig
![](img/nachher.png)
