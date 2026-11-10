# isard-data

Data files for [isard](https://github.com/IGNF/isard)'s examples and tests, served by GitHub Pages at
`https://graffkevin.github.io/isard-data/`, with CORS open to every origin.

| Folder | What | Made by | Source and licence |
|---|---|---|---|
| `splats/martyrs/` | A square of Paris captured as 9.98 million Gaussian splats, cut into 3D Tiles 1.1 with levels of detail (770 tiles, `KHR_gaussian_splatting`, SPZ), placed by hand | `bun run splats:tiles splatmartyrs.sog out/ --position 2.3488,48.8534,30 --scale 20 --up -y` | © its authors, [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| `van/van.glb` | A delivery van with its wheels turning in a clip of a second (one turn about their axle), 5 m long, its front glTF's +Z | Kenney's `van.glb` (Car Kit 3.1), its colormap embedded, scaled, the clip added | [Kenney](https://kenney.nl/assets/car-kit), [CC0](https://creativecommons.org/publicdomain/zero/1.0/) |
| `closed-network/` | PLAN IGN's style, its sprite and its fonts (Source Sans Pro, Latin and punctuation), the style taking them from here: the files of the *Closed network* example | `npx isard-assets closed-network --base https://cdn.jsdelivr.net/gh/graffkevin/isard-data@v7/closed-network/ --only fonts,styles`, the other styles and ranges left out | © IGN, [Licence Ouverte 2.0](https://www.etalab.gouv.fr/licence-ouverte-open-licence/); Source Sans Pro, Adobe, [SIL OFL 1.1](https://openfontlicense.org) |

Load one in isard: `map.addTiles3d({ url: 'https://graffkevin.github.io/isard-data/splats/martyrs/tileset.json' })`.

## Licence

The data here, the van (CC0, public domain) and `closed-network/` (its own licences, above) excepted, is under the [Creative Commons Attribution 4.0 International licence](https://creativecommons.org/licenses/by/4.0/)
(`LICENSE`): free to share and adapt, with credit to its authors as the table above gives it. The 3D Tiles are a
conversion of the authors' capture by isard's `splat-tiles` (cut into tiles, its coarse levels merged).
