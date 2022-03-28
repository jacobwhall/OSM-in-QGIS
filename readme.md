# OSM styles for QGIS
 
This repository was forked from [yannos/Beautiful_OSM_in_QGIS](https://github.com/yannos/Beautiful_OSM_in_QGIS). It is distributed under the GPLv3 license.

This project is designed to work with osm2pgsql + default.style (more on this later).

## Installation

1. Install PostgreSQL/PostGIS
2. If you haven't already, download OSM data e.g. [virginia-latest.osm.pbf](https://download.geofabrik.de/north-america/us/virginia.html)
3. Load your OSM data into QGIS as Postgres vector layers, using the [osm2pgsql](https://osm2pgsql.org/) with its [default style](https://github.com/openstreetmap/osm2pgsql/blob/master/default.style).
   ```
   osm2pgsql --create --multi-geometry --database gis --username $USER --hstore "data.osm.pbf"
   ```
4. [Import your PostGIS database into QGIS](https://docs.qgis.org/3.4/en/docs/training_manual/spatial_databases/import_export.html#db-manager)
5. Apply stylesheets. There is one stylesheet per layer with the same name, for example planet_osm_roads.qml should be applied to planet_osm_roads

## Further Reference

See the [upstream repo](https://github.com/yannos/Beautiful_OSM_in_QGIS) for more in-depth instructions and tips

## Contributing

Please feel free to contribute. I do hope to merge this repo upstream once I'm happy with it
