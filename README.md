# Nanoscopy Analysis Toolkit

An open‑source Python toolkit for analyzing single‑molecule localization microscopy (SMLM) data. The toolkit provides scripts and functions for common SMLM analysis tasks: localization precision estimation, drift correction, cluster analysis, and visualization.

## Features

- **Localization precision calculation** using the Thompson formula
- **Drift correction** via cross‑correlation or fiducial‑based methods
- **Clustering algorithms** (DBSCAN, Ripley’s K, etc.) for quantifying molecular organization
- **Visualization** of localization maps, precision maps, and cluster properties
- **Modular design** – each script can be used independently or as part of a pipeline
- **Extensive documentation** and examples

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### From Source
1. Clone the repository:
   ```bash
   git clone https://github.com/cuines/Nanoscopy-Analysis-Toolkit.git
   cd Nanoscopy-Analysis-Toolkit
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   (If `requirements.txt` does not yet exist, install the following packages manually: `numpy`, `pandas`, `matplotlib`, `scipy`, `scikit‑learn`.)

3. Test the installation by running a simple example (see below).

## Quick Start

1. Prepare your localization data as a CSV file with at least the columns `x`, `y`, `frame`, `photons`, `background`.
2. Calculate localization precision:
   ```bash
   python scripts/calculate_precision.py --input your_data.csv --pixel‑size 100 --psf‑sigma 1.5
   ```
   This will output a new CSV file with an added `precision` column.

3. For drift correction:
   ```bash
   python scripts/drift_correction.py --input your_data.csv --method cross‑correlation
   ```

4. For cluster analysis:
   ```bash
   python scripts/cluster_analysis.py --input your_data.csv --algorithm dbscan --eps 20 --min‑samples 5
   ```

## Project Structure

```
Nanoscopy‑Analysis‑Toolkit/
├── scripts/               # Main analysis scripts
│   ├── calculate_precision.py
│   ├── drift_correction.py
│   └── cluster_analysis.py
├── docs/                  # Detailed documentation
├── tests/                 # Unit tests
├── examples/              # Example datasets and notebooks
├── LICENSE
├── .gitignore
└── README.md              (this file)
```

## Contributing

We welcome contributions from the community! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to submit new scripts, report bugs, or suggest enhancements.

## Citation

If you use this toolkit in your research, please cite it as:

> **Nanoscopy Analysis Toolkit** (2025). https://github.com/cuines/Nanoscopy‑Analysis‑Toolkit.

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please open an issue on the [GitHub issue tracker](https://github.com/cuines/Nanoscopy‑Analysis‑Toolkit/issues).