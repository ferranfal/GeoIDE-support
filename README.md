# GeoIDE

GeoIDE is a free Visual Studio Code extension for interactive Python data science and geospatial work. It keeps Python variables alive between executions and brings a Variable Explorer, scientific plots, tables and interactive maps into one panel.

This public repository is the official information and support page for GeoIDE. It does **not** contain the proprietary development source code.

## Main features

- Run Python files, selections and `# %%` cells in persistent per-file sessions.
- Use **Run Cell**, **Run Above** and **Run Below** without the VS Code Jupyter extension.
- Inspect NumPy, pandas and xarray variables and delete selected variables from memory.
- Create plots and inspect supported raster, vector and point-cloud data.
- Use worldwide satellite imagery and additional online or network-free map backgrounds.

## Requirements

- Visual Studio Code 1.90 or later.
- A local Python environment containing:

  ```bash
  python -m pip install "ipykernel>=6.29,<8" "jupyter_client>=8.6,<9"
  ```

- The scientific packages needed by your own work, such as NumPy, pandas, xarray, GeoPandas, Rasterio or Matplotlib.

GeoIDE does not install or update Python packages automatically.

## Getting started

1. Install GeoIDE from Visual Studio Marketplace when the public listing is available.
2. Open a trusted workspace and a Python file.
3. Run **GeoIDE: Select Python Environment** from the Command Palette.
4. Add a cell marker and run the cell:

   ```python
   # %%
   import numpy as np
   values = np.arange(100).reshape(10, 10)
   values.mean()
   ```

5. Inspect `values` in the Variable Explorer and open a plot, table or map when supported.

## Support and bug reports

Use [GitHub Issues](https://github.com/ferranfal/GeoIDE-support/issues) for questions and reproducible problems. Before opening an issue, please include:

- GeoIDE version and Visual Studio Code version;
- operating system and whether the workspace is local, SSH, WSL or another remote host;
- Python version and the relevant package versions;
- a small example using synthetic or non-confidential data;
- the exact error message or a screenshot with private information removed.

GeoIDE can export a filtered diagnostic report through **GeoIDE: Export Diagnostics**. Review it before sharing. Do not publish credentials, private paths, proprietary datasets or personal information.

## Data and online services

Python runs in the environment selected by the user. GeoIDE does not include analytics telemetry or a hosted data-upload service. Online map backgrounds contact their providers directly; those providers receive the connection IP address and the tile coordinates required for the visible area. Provider terms, attribution requirements and availability apply separately.

## License

GeoIDE is free to use, including for commercial work, under the [GeoIDE Free-of-Charge Proprietary Software License](LICENSE). It is not open-source software. Third-party components and services retain their own terms and notices.

© 2026 Ferran Fernández Alemany.
