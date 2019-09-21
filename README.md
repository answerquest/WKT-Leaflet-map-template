## Intro

A template that others can use, where the following things have been achieved:

- Geo-data file is in CSV WKT format (normal csv, with one column 'WKT' holding the geo-data)
- CSV WKT data is loaded from CSV and rendered on map
- Basic (but difficult to code!) interactions like hover, click are set up
- Any kind of geo data like point, polygon, line, multipolygon etc can be loaded; and multiple kinds can be loaded togther.


### Advantage of WKT:
The data is in a simple table like so:
```
+───────────+─────────+──────────────────────────────────────+
| DISTRICT  | D_CODE  | WKT                                  |
+───────────+─────────+──────────────────────────────────────+
| Gondiya   | 507     | POLYGON ((80.56149 20.82284, ... ))  |
| Bhandara  | 506     | POLYGON ((80.56149 20.82284, ... ))  |
| Jalgaon   | 499     | POLYGON ((80.56149 20.82284, ... ))  |
+───────────+─────────+──────────────────────────────────────+
```
So you can easily bring in more columns, edit your data, make fixes, combine data from different sources, etc. No need of spending time loading up on GIS software etc. Data management becomes a breeze : just change and save your csv.

### Deploying at your end
- Download and unzip this repo
- No worries, nothing to install. But...
- Since there is dynamic csv loading happening, simply double-clicking the html file isn't going to cut it.
- This folder needs to be deployed on a server. Don't worry, you can easily deploy a "simple portable web server". Search for that on the web - there's many quick apps / command line solutions.
- Once your server is launched, open browser and go to `localhost:8000` or whatever port number the server tells you.


### Getting data in WKT form
If you have your data loaded up on QGIS, then follow this guide: https://dominoc925.blogspot.com/2018/01/using-qgis-to-export-csv-files-with.html  
You can also search online for "covert KML to WKT" etc.


### Libraries used
- **[Wicket](https://github.com/arthur-e/Wicket)** for wicket to geojson conversion
- **[Papa.parse]()** for loading the CSV file as a json array
- **[Leaflet](https://leafletjs.com/)** for the map


Proudly Made In India by [Nikhil VJ](https://nikhilvj.co.in)
