🌦️ WRF Domain Wizard

Interactive WRF/WPS Domain Configuration Tool








WRF Domain Wizard is a browser-based tool for interactively designing Weather Research and Forecasting (WRF) model domains and configuring the Weather Research and Forecasting Preprocessing System (WPS).

Draw, move, and resize nested domains directly on an interactive map. Configure projections, grid settings, simulation dates, and directory paths, then generate, preview, copy, and download your namelist.wps and namelist.input files.

No server-side processing is required. The application runs in your browser from a single index.html file. Map tiles and libraries require an internet connection.

🚀 Open the Live Application

Launch WRF Domain Wizard →

Feature

Description

🗺️ Interactive mapping

Draw and edit domains directly on the map

🌐 Multiple projections

Lambert Conformal, Mercator, Polar Stereographic, and Latitude–Longitude

🧩 Nested domains

Configure up to 9 domains

📋 Copy to clipboard

Copy generated namelists or important configuration values

📥 Download files

Save generated WRF/WPS configuration files

💾 Project management

Save and reopen projects as JSON

↩️ Undo and redo

Reverse or restore domain edits

🔒 Client-side operation

Domain settings are processed in your browser

✨ Key Features

🗺️ 1. Interactive Domain Drawing

Draw domain rectangles by clicking and dragging the mouse.

Move domains using their centre handles.

Resize domains using corner handles.

Automatically pan the map when drawing near its edges.

Enable Keep inside parent to help constrain nested domains.

Edit domain extents using the configuration table.

Add, remove, and manage multiple nested domains.

🌍 2. Map Layers

Switch between different basemaps to identify suitable WRF model domains:

Carto Voyager

Esri World Topographic Map

Esri World Imagery

🧭 3. Projection Configuration

Choose from four supported map projections:

Lambert Conformal

Mercator

Polar Stereographic

Latitude–Longitude

⚙️ 4. WRF/WPS Configuration

Configure the main simulation and preprocessing settings:

Start and end dates and times

Meteorological input interval

WRF integration timestep

History output interval

Vertical model levels

Domain grid dimensions and nesting parameters

Geographic data directory

Geogrid output directory

Ungrib input directory and file prefix

Metgrid output directory

📄 5. Generate and Copy Namelists

Generate editable previews of:

namelist.wps

namelist.input

Quick actions:

📋 Copy — Copy the generated configuration to your clipboard.

📥 Download — Save the configuration as a file.

✏️ Edit — Modify the generated text before saving.

🔄 Regenerate — Update the output after changing settings.

GitHub automatically provides a copy button on fenced code blocks below, allowing you to copy commands and configuration examples quickly.

💾 6. Save and Reopen Projects

Save domain configurations as JSON project files and reopen them later to continue editing your setup.

🧪 7. Built-in Example

Load the built-in three-domain example:

Domain

Approximate grid spacing

d01

15 km

d02

5 km

d03

1.667 km

These are example nominal grid spacings. Actual grid geometry depends on the configured projection, dimensions, and nesting ratios.

🖥️ How to Use the Wizard

Open the live application.

Draw the outer domain, d01, by dragging a rectangle on the map.

Add d02, d03, and additional nested domains as needed.

Select a domain to move or resize it using the available handles.

Configure the projection, grid settings, simulation period, and file paths.

Click Generate namelists.

Review and edit the generated namelist.wps and namelist.input.

Use Copy or Download to save the configuration.

Run WPS and inspect the generated domain grids before running WRF.

📘 Documentation: Read the step-by-step User Guide.

📋 Copy-Friendly Installation and Launch Commands

1. Clone the repository

Copy the command below using GitHub's code-block copy button.

git clone https://github.com/goikelem/WRF-domain-Wizard.git

2. Enter the project directory

cd WRF-domain-Wizard

3. Check that the application exists

ls -lh index.html

4. Open in your default Linux browser

xdg-open index.html

5. Open from WSL on Windows

explorer.exe index.html

Alternatively, open the file directly in Microsoft Edge:

explorer.exe "$(wslpath -w "$PWD/index.html")"

6. Run a local HTTP server if needed

If the application uses JavaScript modules or local resources that do not work when opening index.html directly, start a local server:

python3 -m http.server 8000

Then open:

http://localhost:8000

Keep the terminal running while using the application. Press Ctrl+C to stop the server.

📁 Project Structure

WRF-domain-Wizard/
├── index.html           # Main browser-based application
├── README.md            # Project documentation
├── LICENSE              # License, if included
└── docs/
    └── USER_GUIDE.md    # Step-by-step documentation

The LICENSE and docs/USER_GUIDE.md entries should exist in the repository for these links and paths to work.
