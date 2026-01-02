# Data Directory

Place your Garmin sleep data JSON files here.

## Structure

- `raw/` - Original exported data from Garmin
- `processed/` - Cleaned and processed data files

## Note

Data files are excluded from version control (see `.gitignore`) to protect your personal information.

## Expected Data Format

Your JSON files should contain sleep session data with fields like:
- Sleep start/end times
- Sleep stages (deep, light, REM, awake)
- Sleep scores
- Heart rate data
- Respiration data
