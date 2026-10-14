# WRF Domain Wizard

Browser-based WRF/WPS Domain Wizard. Draw nested domains on an interactive map with your mouse, move and resize them with handles, then generate ready-to-use `namelist.wps` and `namelist.input` files. Everything runs client-side in a single `index.html`; nothing is uploaded to a server.

**Live app:** https://goikelem.github.io/WRF-domain-Wizard/

## Features

- Interactive map (Leaflet) with Carto Voyager, ESRI World Topo and ESRI World Imagery basemaps.
- Draw domains by holding the mouse and dragging. The map auto-pans when you reach its edge, so you can place the far corner outside the current view.
- Select a domain by clicking it. Move it with the centre square and resize it with the corner squares.
- "Keep inside parent" option for nests.
- Up to 9 domains, with undo and redo.
- Projections: Lambert Conformal, Mercator, Polar Stereographic, Latitude-Longitude.
- Settings for start and end time, met interval, timestep, history interval and vertical levels.
- Path boxes for `geog_data_path`, geogrid, ungrib (directory and prefix) and metgrid, each with a Browse button.
- Editable preview of both namelists, with Copy and Download buttons.
- Save and open projects as `.json`.
- Built-in 3-domain example (15 km, 5 km, 1.667 km).

## How to use

1. Open the app. Draw mode is on, so drag a rectangle on the map for d01.
2. Draw d02, d03 and so on, or press **Add domain**. Each nest is sized relative to its parent.
3. Untick **Draw mode** to pan the map and to move or resize the selected domain with the squares. You can also type extents in the table.
4. Set projection, dates and paths.
5. Click **Generate namelists**, then **Copy** or **Download**.

## Notes

- Browsers hide full folder paths. **Browse** keeps the parent path already in the box and replaces the last part with the folder you pick, so check the start of the path afterwards.
- Folder picking works best in Chrome and Edge on the published HTTPS site.
- The ungrib prefix is written as `<ungrib directory>/<prefix>`, and the same value is used for `fg_name` in `&metgrid`.
- The nesting maths (grid size, parent ratio, parent start, fit check) is approximate and based on the drawn lat/lon boxes. Review `e_we`, `e_sn`, `i_parent_start` and `j_parent_start`, and run `geogrid.exe` to confirm the grid before a real run.
- The physics and dynamics sections hold generic defaults. Adjust them for your case.

## Not included yet

Opening an existing `namelist.wps` or `geo_em` files, terrain plots, and projected (curved) box edges. The original desktop version (Python/Tkinter) has these.

## Run locally

Open `index.html` in a browser. An internet connection is needed for the map libraries and tiles.

## Publish on GitHub Pages

1. Upload `index.html` and `README.md` to the `main` branch.
2. Go to Settings > Pages, choose "Deploy from a branch", then `main` and `/ (root)`.
3. The site appears at `https://<user>.github.io/<repo>/` after a minute or two.

## Credits

Map library: [Leaflet](https://leafletjs.com). Tiles: Carto, Esri and OpenStreetMap contributors.
