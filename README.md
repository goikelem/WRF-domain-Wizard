Here is the complete Markdown file. You can copy the raw text below and save it as `README.md` (or any other `.md` file) in your repository.

```markdown
# 🌦️ WRF Domain Wizard: Interactive Domain Configuration

[![Live App](https://img.shields.io/badge/🚀_Live_App-Open_Wizard-2ea44f?style=for-the-badge)](https://goikelem.github.io/WRF-domain-Wizard/)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Online-blue?style=flat-square&logo=github)](https://goikelem.github.io/WRF-domain-Wizard/)
[![WRF](https://img.shields.io/badge/WRF-4.x-orange?style=flat-square)](https://github.com/wrf-model/WRF)
[![WPS](https://img.shields.io/badge/WPS-Domain_Setup-purple?style=flat-square)](https://github.com/wrf-model/WPS)
[![Maps](https://img.shields.io/badge/Maps-Leaflet-green?style=flat-square&logo=leaflet)](https://leafletjs.com/)

**WRF Domain Wizard** is a browser-based, interactive tool designed to simplify the setup of the Weather Research and Forecasting (WRF) model and its Preprocessing System (WPS). 

Instead of manually calculating coordinates and editing text files, users can **draw, move, and resize nested domains directly on an interactive map**. The tool processes all configurations client-side (in your browser) and generates ready-to-use `namelist.wps` and `namelist.input` files.

---

## ✨ Key Features

| Icon | Feature | Description |
|:---:|:---|:---|
| 🗺️ | **Interactive Domain Drawing** | Draw domain rectangles by clicking and dragging. Move via center handles, resize via corner handles. |
| 🌐 | **Multiple Projections** | Supports Lambert Conformal, Mercator, Polar Stereographic, and Latitude–Longitude projections. |
| 🧩 | **Nested Domains** | Configure and manage up to 9 nested domains (d01, d02, etc.) with "Keep inside parent" constraints. |
| ⚙️ | **Full WRF/WPS Config** | Set simulation dates, timesteps, vertical levels, grid dimensions, and directory paths. |
| 📋 | **Copy & Download** | Generate, preview, edit, copy to clipboard, and download your namelists directly from the browser. |
| 💾 | **Project Management** | Save your domain configurations as JSON files and reopen them later to continue editing. |
| ↩️ | **Undo & Redo** | Easily reverse or restore domain edits without losing your progress. |
| 🌍 | **Map Layers** | Switch between Carto Voyager, Esri World Topographic, and Esri World Imagery basemaps. |
| 🔒 | **Client-Side Privacy** | No server-side processing. Your settings are processed entirely in your browser. |

---

## 🖥️ How to Use the Wizard

Follow these steps to configure your WRF simulation:

1. **Launch the App:** Open the [Live WRF Domain Wizard](https://goikelem.github.io/WRF-domain-Wizard/).
2. **Draw the Outer Domain:** Click and drag on the map to draw your outermost domain (**d01**).
3. **Add Nests:** Add **d02**, **d03**, and additional nested domains as needed for your study.
4. **Edit Domains:** Select a domain to move or resize it using the map handles. You can also fine-tune extents using the configuration table.
5. **Configure Settings:** Set your map projection, grid settings, simulation start/end times, and file paths (geogrid, ungrib, metgrid).
6. **Generate Namelists:** Click the **Generate namelists** button.
7. **Review & Edit:** Preview the generated `namelist.wps` and `namelist.input`. Use the **Edit** feature to make manual tweaks.
8. **Export:** Use the **Copy** or **Download** buttons to save your configuration.
9. **Run WPS/WRF:** Take your downloaded files to your HPC or local system, run `geogrid.exe` to verify grids, and proceed with your WRF simulation.

---

## 📋 Copy-Friendly Installation Commands

*Click the "Copy" button on the top right of the code blocks below to quickly clone and run the project locally.*

### 1. Clone the repository
```bash
git clone https://github.com/goikelem/WRF-domain-Wizard.git
```

### 2. Enter the project directory
```bash
cd WRF-domain-Wizard
```

### 3. Open the application in your browser
```bash
# For Linux:
xdg-open index.html

# For WSL on Windows:
explorer.exe index.html
```

### 4. (Optional) Run a local HTTP server
If you encounter issues opening the HTML file directly, start a local server:
```bash
python3 -m http.server 8000
```
Then, navigate to **http://localhost:8000** in your browser.

---

## ⚠️ Important Technical Notes

* **Directory paths and browser limitations:** Browsers restrict access to local files. The **Browse** buttons preserve the existing path prefix and replace the final component with the selected folder. Check the resulting path before generating your namelists.
* **Nesting calculations:** The nesting calculations are approximate and based on the drawn lat/lon rectangles. Always check `e_we`, `e_sn`, `parent_grid_ratio`, and `i_parent_start` before running a real simulation.
* **Client-side privacy:** The wizard does not require a backend server. However, map tiles and external libraries may be requested from their respective providers.

---

## 🗺️ Credits

* **Map library:** [Leaflet](https://leafletjs.com/)
* **Map providers:** [CARTO](https://carto.com/), [Esri](https://www.esri.com/), and OpenStreetMap contributors.
* **Modeling systems:** [WRF](https://github.com/wrf-model/WRF) and [WPS](https://github.com/wrf-model/WPS).

---

## 👨‍💻 Author & Support

**Goitom Kelem**

Project: [WRF Domain Wizard](https://github.com/goikelem/WRF-domain-Wizard)

If this tool helps your meteorological research or WRF workflow:
- ⭐ Star the repository on GitHub.
- 🍴 Fork the project and contribute improvements.
- 🐛 Report bugs and suggest new features through GitHub Issues.

**Draw your domains. Configure your grids. Generate your namelists. Prepare for WRF.** 🌦️
```
