# isard-data

Data files for [isard](https://github.com/IGNF/isard)'s examples and tests, served by GitHub Pages at
`https://graffkevin.github.io/isard-data/`, with CORS open to every origin.

| Folder | What | Made by | Source and licence |
|---|---|---|---|
| `splats/martyrs/` | A square of Paris captured as 9.98 million Gaussian splats, cut into 3D Tiles 1.1 with levels of detail (770 tiles, `KHR_gaussian_splatting`, SPZ), placed by hand | `bun run splats:tiles splatmartyrs.sog out/ --position 2.3488,48.8534,30 --scale 20 --up -y` | © its authors, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| `van/van.glb` | A delivery van with its wheels turning in a clip of a second (one turn about their axle), 5 m long, its front glTF's +Z | Kenney's `van.glb` (Car Kit 3.1), its colormap embedded, scaled, the clip added | [Kenney](https://kenney.nl/assets/car-kit), [CC0](https://creativecommons.org/publicdomain/zero/1.0/) |
| `closed-network/` | PLAN IGN's style, its sprite and its fonts (Source Sans Pro, Latin and punctuation), the style taking them from here: the files of the *Closed network* example | `npx isard-assets closed-network --base https://cdn.jsdelivr.net/gh/graffkevin/isard-data@v7/closed-network/ --only fonts,styles`, the other styles and ranges left out | © IGN, [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/); Source Sans Pro, Adobe, [SIL OFL 1.1](https://openfontlicense.org) |
| `dted/n45e006.dt1` | The degree of the Mont Blanc (6° to 7° E, 45° to 46° N) as a DTED level 1 cell: 1201 × 1201 posts 3″ apart, heights in metres | Copernicus DEM GLO-30 tile `Copernicus_DSM_10_N45_00_E006_00_DEM` sampled at the posts (bilinear), written as DTED (UHL, DSI, ACC, a record per meridian) | Produced using Copernicus WorldDEM-30 © DLR e.V. 2010-2014 and © Airbus Defence and Space GmbH 2014-2018 provided under COPERNICUS by the European Union and ESA; all rights reserved ([GLO-30 licence](https://spacedata.copernicus.eu/documents/20123/121286/CSCDA_ESA_Mission-specific+Annex_31_Oct_22.pdf)) |
| `mbtiles/briancon-plan-ign.mbtiles` | PLAN IGN's tiles of Briançon's area (6.58° to 6.70° E, 44.86° to 44.94° N), levels 10 to 14, as an MBTiles file (PNG images, rows from the south, an index on their position) | the Géoplateforme's WMTS (`GEOGRAPHICALGRIDSYSTEMS.PLANIGNV2`, `PM`) written into SQLite by a script | © IGN, [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/) |
| `mbtiles/briancon-openfreemap.mbtiles` | OpenFreeMap's vector tiles of the same area and levels, gzipped (`format` `pbf`, its layers in `json`) | OpenFreeMap's planet tiles of 2026-11-01 written into SQLite by the same script | © OpenMapTiles, © OpenStreetMap contributors, [ODbL](https://opendatacommons.org/licenses/odbl/) |
| `gpkg/briancon.gpkg` | A GeoPackage of Briançon: PLAN IGN in the Géoplateforme's Lambert-93 tile matrix set (`2154_10cm_6_20`, levels 13 to 16, JPEG; a `plan_ign` tile table), and the forts as features in Lambert-93 (`forts`: five points and the Cité Vauban's outline, their positions approximate) | the WMTS's tiles and the features written into SQLite by a script, as GeoPackage 1.3 lays them out | PLAN IGN © IGN, [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/); the forts, CC BY 4.0 |

Load one in isard: `map.addTiles3d({ url: 'https://graffkevin.github.io/isard-data/splats/martyrs/tileset.json' })`.

## Licence

The data here, the van (CC0, public domain), `closed-network/`, `dted/`, `mbtiles/` and the PLAN IGN tiles of `gpkg/` (their own licences, above) excepted, is under the [Creative Commons Attribution 4.0 International licence](https://creativecommons.org/licenses/by/4.0/)
(`LICENSE`): free to share and adapt, with credit to its authors as the table above gives it. The 3D Tiles are a
conversion of the authors' capture by isard's `splat-tiles` (cut into tiles, its coarse levels merged).
