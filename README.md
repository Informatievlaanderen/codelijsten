# codelijsten
Deze repository omvat een aantal codelijsten die gepubliceerd worden op <https://data.vlaanderen.be/doc/conceptscheme>.

Per codelijst wordt een subdirectory aangemaakt. Elke codelijst is een of meerdere RDF files in de turtle syntax volgens het SKOS vocabularium.
De master branch staat op data.vlaanderen.be. De test-branch is voor de test-omgeving.

# vormafspraken voor publicatie van codelijsten op data.vlaanderen.be
Om een uniforme gebruikservaring te bekomen, is het nodig om enkele vormafspraken te maken voor het publiceren van een codelijst op data.vlaanderen.be.
De volgende afspraken gelden:

- uri's van concepten en conceptscheme's voldoen aan de URI standaard en het volgende patroon:
  - `https://data.vlaanderen.be/id/conceptscheme/{mijncs}`
  - `https://data.vlaanderen.be/id/concept/{mijncs}/{mijnconcept}`
  
- voor conceptschemes worden de volgende eigenschappen getoond op de html subjectpagina's:

|eigenschap | nota |
|-----------|------|
skos:prefLabel | een unieke naam voor het conceptscheme
skos:definition | een definitie van de codelijst

- voor concepten zijn de volgende eigenschappen getoond op de html subjectpagina's:

|eigenschap | nota |
|-----------|------|
skos:prefLabel | een unieke naam voor het concept
skos:definition | een definitie van het concept
skos:inscheme  | het conceptscheme waartoe dit concept behoort
skos:topConceptOf | het conceptscheme waarvan dit concept een top concept is 
skos:narrower | de concepten die onder dit concept hangen in de conceptscheme boom.

- gebruik language-tagged strings i.p.v. plain literals
Dus `"mijn label@nl` i.p.v. `"mijn label"`

- We verwachten een hierarchie in 1 richting. Het is voldoende om de hierarchie in 1 richting uit te drukken. Het is aan de afnemers om indien voor hen nodig ook de omgekeerde relatie te berekenen. Dat maakt de data ook overzichtelijk. 



