# Wozu das Ganze I

* Technisch haben wir nicht viel gewonnen
  * aa.bb.cc.dd
  * erste Teil der Versionsnummer `aa` wird gestrichen
  * zweite Teil `bb` wird ersetzt durch `CC-Release`
  * dritte Teil `cc` bleibt wie es ist
  * vierte Teil `dd` wird ein Suffix
  * mehr oder weniger ließen sich 90% der Nummern abbilden, also wozu das Ganze?

# Wozu das Ganze II

* Endnutzer: Gemeinsamkeit der Versionsnummer und des CC-Release geben eindeutige Aussage
* Release-Manager: keine Notwendigkeit der manuellen Pflege der Versionsnummer (es kommt alles aus Tags oder der Repository)
* QA und Entwickler:
  * deutlich verbesserte Lesbarkeit der Versionsnummer für auftretende Bugs
  * vereinfachte Kommunikation, da an Version auch Ursprung des Bugs erkennbar
