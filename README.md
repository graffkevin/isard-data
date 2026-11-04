# isard-data

Data files for [isard](https://github.com/IGNF/isard)'s examples and tests, served by GitHub Pages at
`https://graffkevin.github.io/isard-data/`, with CORS open to every origin.

| Folder | What | Made by | Source and licence |
|---|---|---|---|
| `splats/martyrs/` | A square of Paris captured as 9.98 million Gaussian splats, cut into 3D Tiles 1.1 with levels of detail (770 tiles, `KHR_gaussian_splatting`, SPZ), placed by hand | `bun run splats:tiles splatmartyrs.sog out/ --position 2.3488,48.8534,30 --scale 20 --up -y` | to be completed |

Load one in isard: `map.addTiles3d({ url: 'https://graffkevin.github.io/isard-data/splats/martyrs/tileset.json' })`.
