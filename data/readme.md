## Exercises in OTTR

### Software to be installed
1. Download the latest stable release of [Lutra](https://gitlab.com/ottr/lutra/lutra/-/releases).
2. Download [Fuseki](https://jena.apache.org/download/).

### Getting to know the data
3. Browse `planets.xlsx` and get familiar with the Planets-sheet in tabOTTR syntax.
4. Run `planets.xlsx` together with `planet-tpl.ttl` through Lutra and generate a `.ttl`-file containing information from the spreadsheet.

*Lutra command:* `java -jar lutra.jar -l .\planet-tpl.ttl -L stottr -I tabottr -f .\planets.xlsx -o planet-output.ttl`

5. Upload the output-file into Fuseki and browse through SPARQL.
```
SELECT * WHERE { ?s ?p ?o . }
```

### Graph enrichment
6. Browse the data in `satellite-raw.xlsx`.
7. Create a new page in the spreadsheet where you will make tabOTTR instances of satellites.

| Planet ID      | Satellite ID | Label |
| ----------- | ----------- |---------|

8. Following headers are required, then choose satellite characteristics of choice. E.g. radius.
9. Write a `:SatelliteTemplate` that will serialise the spreadsheet into RDF.
10. Run through Lutra and upload into Fuseki.
