# :sun_behind_rain_cloud: WRF Domain Wizard: Interactive Domain Configuration

![](https://goikelem.github.io/WRF-domain-Wizard/)
![](https://goikelem.github.io/WRF-domain-Wizard/)


**WRF Domain Wizard** is a browser-based, interactive tool designed to simplify the setup of the Weather Research and Forecasting (WRF) model and its Preprocessing System (WPS). 

Instead of manually calculating coordinates and editing text files, users can **draw, move, and resize nested domains directly on an interactive map**. The tool processes all configurations client-side (in your browser) and generates ready-to-use `namelist.wps` and `namelist.input` files.

---

## :sparkles: Key Features

| Icon | Feature | Description |
|:---:|:---|:---|
| :map: | **Interactive Domain Drawing** | Draw domain rectangles by clicking and dragging. Move via center handles, resize via corner handles. |
| :globe_with_meridians: | **Multiple Projections** | Supports Lambert Conformal, Mercator, Polar Stereographic, and Latitude–Longitude projections. |
| :jigsaw: | **Nested Domains** | Configure and manage up to 9 nested domains (d01, d02, etc.) with "Keep inside parent" constraints. |
| :gear: | **Full WRF/WPS Config** | Set simulation dates, timesteps, vertical levels, grid dimensions, and directory paths. |
| :clipboard: | **Copy & Download** | Generate, preview, edit, copy to clipboard, and download your namelists directly from the browser. |
| :floppy_disk: | **Project Management** | Save your domain configurations as JSON files and reopen them later to continue editing. |
| :leftwards_arrow_with_hook: | **Undo & Redo** | Easily reverse or restore domain edits without losing your progress. |
| :earth_africa: | **Map Layers** | Switch between Carto Voyager, Esri World Topographic, and Esri World Imagery basemaps. |
| :lock: | **Client-Side Privacy** | No server-side processing. Your settings are processed entirely in your browser. |

---

## :desktop_computer: How to Use the Wizard

Follow these steps to configure your WRF simulation:

1. **Launch the App:** Open the Live WRF Domain Wizard.
2. **Draw the Outer Domain:** Click and drag on the map to draw your outermost domain (**d01**).
3. **Add Nests:** Add **d02**, **d03**, and additional nested domains as needed for your study.
4. **Edit Domains:** Select a domain to move or resize it using the map handles. You can also fine-tune extents using the configuration table.
5. **Configure Settings:** Set your map projection, grid settings, simulation start/end times, and file paths (geogrid, ungrib, metgrid).
6. **Generate Namelists:** Click the **Generate namelists** button.
7. **Review & Edit:** Preview the generated `namelist.wps` and `namelist.input`. Use the **Edit** feature to make manual tweaks.
8. **Export:** Use the **Copy** or **Download** buttons to save your configuration.
9. **Run WPS/WRF:** Take your downloaded files to your HPC or local system, run `geogrid.exe` to verify grids, and proceed with your WRF simulation.

---

## :clipboard: Copy-Friendly Installation Commands

*Click the "Copy" button on the top right of the code blocks below to quickly clone and run the project locally.*

### 1. Clone the repository
```bash
git clone [https://github.com/goikelem/WRF-domain-Wizard.git](https://github.com/goikelem/WRF-domain-Wizard.git)
