# Import Natural Earth into PostGIS [![Docker Automated build](https://img.shields.io/docker/automated/osm2vectortiles/import-natural-earth.svg?maxAge=2592000)]()

This is a Docker image to import a subset of [NaturalEarth](https://img.shields.io/docker/automated/jrottenberg/ffmpeg.svg
) using *ogr2ogr* into a PostGIS database.
The SQLite database containing the tables for the import is already baked
into the container to make distribution and execution easier.

## Usage

Provide the database credentials and run `import-water`.

```bash
docker run --rm \
    -e POSTGRES_USER="osm" \
    -e POSTGRES_PASSWORD="osm" \
    -e POSTGRES_HOST="127.0.0.1" \
    -e POSTGRES_DB="osm" \
    -e POSTGRES_PORT="5432" \
    osm2vectortiles/import-natural-earth
```
