## Exercises in OTTR 

### Software to be installed

1. Download the latest stable release of [Lutra](https://gitlab.com/ottr/lutra/lutra/-/releases).

### Getting to know the data
3. Browse `data.xlsx` and get familiar with the Planets-sheet in tabOTTR syntax.
4. Run `data.xlsx` togeher with `tpl.ttl` through Lutra and generate a `.ttl`-file containing the seralized RDF from the spreadsheet. 

```
java -jar lutra.jar -l tpl.ttl -L stottr -I tabottr -f data.xlsx -o output.ttl
```
5. Open the sheet Satellites OTTR and add tabOTTR flavoured syntax for serialization.
6. Write a `:SatelliteTemplate` in the `tpl.ttl` file for serializing the new data.
7. Run through Lutra.