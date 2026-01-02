# Sleep Data Visualization Project

A comprehensive personal data visualization project analyzing sleep patterns using Garmin device data.

## Overview

This project analyzes approximately 700 nights of sleep data from Garmin devices, creating interactive visualizations to understand sleep quality patterns, including relationships between travel, seasonal changes, and various sleep metrics.

## Features

- **Interactive Calendar Visualizations**: Traditional and circular calendar formats
- **Radial Bar Calendars**: With cycle phase color coding and smooth gradients
- **Comprehensive Dashboards**: Interactive elements with dropdown selectors and detailed hover tooltips
- **Sleep Metrics Analysis**: Duration, stages (deep, light, REM), and overall sleep scores
- **Statistical Outlier Handling**: Robust measures for travel days and unusual nights

## Tech Stack

- Python 3.x
- Plotly (for interactive visualizations)
- Jupyter Notebooks
- Pandas (for data processing)
- NumPy (for calculations)

## Project Structure

```
sleep-viz-project/
├── notebooks/          # Jupyter notebooks with visualizations
├── data/              # Sleep data JSON files (gitignored)
├── src/               # Reusable Python modules
├── exports/           # Generated visualizations
├── docs/              # Documentation and notes
└── requirements.txt   # Python dependencies
```

## Getting Started

### Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Garmin sleep data in JSON format

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/sleep-viz-project.git
cd sleep-viz-project
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Launch Jupyter:
```bash
jupyter notebook
```

### Data Setup

Place your Garmin sleep data JSON files in the `data/` directory. The data structure should follow Garmin's export format.

## Visualizations

### Calendar Grid View
Traditional calendar-style visualization showing sleep metrics across months.

### Radial Calendar
Innovative circular calendar format with cycle phase color coding.

### Interactive Dashboard
Comprehensive view with dropdown year selectors and detailed metrics.

## Development Notes

- Code is organized with centralized styling elements for consistent theming
- Statistical measures use IQR and MAD for robust outlier handling
- Timezone corrections applied to sleep data for accurate analysis

## Future Plans

- Transition to JavaScript/D3.js for more complex interactions
- Click-to-highlight functionality for weekday analysis
- Side panels with aggregate statistics and sleep quality breakdowns

## Contributing

This is a personal project, but suggestions and ideas are welcome!

## License

MIT License - feel free to use this code for your own sleep data analysis.

## Acknowledgments

- Garmin for providing detailed sleep tracking data
- Plotly for excellent visualization capabilities
