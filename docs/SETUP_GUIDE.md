# GitHub Repository Setup Guide

## Quick Start

### 1. Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right → "New repository"
3. Name it something like `sleep-viz-project` or `garmin-sleep-analysis`
4. Choose "Public" or "Private" (Private recommended for personal data project)
5. **Do NOT** initialize with README, .gitignore, or license (we already have these)
6. Click "Create repository"

### 2. Initialize Local Repository

Open your terminal and navigate to your project folder, then run:

```bash
cd /path/to/your/project
git init
git add .
git commit -m "Initial commit: Sleep visualization project setup"
```

### 3. Connect to GitHub

After creating the repository on GitHub, you'll see commands like these:

```bash
git remote add origin https://github.com/yourusername/sleep-viz-project.git
git branch -M main
git push -u origin main
```

## File Organization Tips

### What to Commit
- ✅ Notebooks (`.ipynb` files)
- ✅ Python scripts (`.py` files)
- ✅ Documentation (`.md` files)
- ✅ Configuration files (`requirements.txt`)
- ✅ Example/template files

### What NOT to Commit (Already in .gitignore)
- ❌ Your actual sleep data (`.json`, `.csv` files in `data/`)
- ❌ Large export images/HTML files
- ❌ Virtual environment folders (`venv/`, `env/`)
- ❌ Python cache files (`__pycache__/`)

## Adding Existing Notebooks

If you have existing notebooks, copy them to the `notebooks/` directory:

```bash
cp /path/to/your/notebook.ipynb notebooks/01_calendar_viz.ipynb
```

Then commit:

```bash
git add notebooks/01_calendar_viz.ipynb
git commit -m "Add calendar visualization notebook"
git push
```

## Workflow Recommendations

### Daily Work
1. Make changes to your notebooks/code
2. Save your work
3. Commit regularly:
```bash
git add .
git commit -m "Descriptive message about what you changed"
git push
```

### Creating Versions/Releases
Use tags for major milestones:
```bash
git tag -a v1.0 -m "First complete visualization suite"
git push origin v1.0
```

## Common Git Commands

```bash
# Check status of files
git status

# See what changed
git diff

# View commit history
git log --oneline

# Create a new branch for experiments
git checkout -b experimental-d3-version

# Switch back to main branch
git checkout main

# Pull latest changes (if working from multiple computers)
git pull
```

## Troubleshooting

### Accidentally Committed Data Files
If you accidentally commit private data:
```bash
git rm --cached data/my_sleep_data.json
git commit -m "Remove private data file"
git push
```

### Want to Undo Last Commit (Not Pushed)
```bash
git reset --soft HEAD~1
```

## Next Steps

1. Copy your existing notebooks into the `notebooks/` directory
2. Place your data files in `data/raw/` (they won't be tracked)
3. Commit and push your code to GitHub
4. Consider adding a badge or screenshots to your README
5. As you develop, commit regularly with descriptive messages
