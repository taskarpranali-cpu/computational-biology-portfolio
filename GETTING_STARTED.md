# Getting Started — Setting Up Your GitHub Portfolio

Follow these steps to get your portfolio live on GitHub.

## Step 1: Create a GitHub Account

If you don't have one yet:
1. Go to [github.com](https://github.com)
2. Click **Sign up**
3. Choose a professional username (e.g., `pranali-taskar` or `ptaskar`)

## Step 2: Install Git

**Mac:**
```bash
# Open Terminal and run:
xcode-select --install
```

**Windows:**
Download from [git-scm.com](https://git-scm.com/download/win)

**Verify it works:**
```bash
git --version
```

## Step 3: Configure Git

```bash
git config --global user.name "Pranali Taskar"
git config --global user.email "taskar.pranali@gmail.com"
```

## Step 4: Create the Repository on GitHub

1. Go to [github.com/new](https://github.com/new)
2. Repository name: `computational-biology-portfolio`
3. Description: `Computational biology & AI projects — genomics, drug discovery, neuroscience, and LLMs for biology`
4. Select **Public**
5. Check **Add a README file**
6. Click **Create repository**

## Step 5: Clone and Add Your Files

```bash
# Clone the empty repo to your computer
git clone https://github.com/YOUR_USERNAME/computational-biology-portfolio.git
cd computational-biology-portfolio

# Copy the portfolio files into this folder
# (copy all contents from the github-portfolio folder)

# Stage all files
git add .

# Make your first commit
git commit -m "Initial portfolio structure with project READMEs"

# Push to GitHub
git push origin main
```

## Step 6: Add Projects as You Complete Them

Each time you finish a notebook:

```bash
# Add the new notebook
git add 01-genomics-expression-analysis/01_data_exploration.ipynb

# Commit with a clear message
git commit -m "Add data exploration notebook for genomics project"

# Push to GitHub
git push origin main
```

## Step 7: Keep Your README Updated

After completing each project, update:
- The **Key Results** section in each project's README
- The **What I Learned** section
- The main portfolio README with any new skills

## Tips for a Strong Portfolio

- **Commit often.** Small, frequent commits show consistent work.
- **Write clear commit messages.** "Add Random Forest classification with 96% accuracy" beats "update notebook."
- **Clear all notebook outputs before committing** (Cell → All Output → Clear in Jupyter). This keeps the repo clean and reviewers can re-run your code.
- **Add a .gitignore** to exclude data files, checkpoints, and temp files.

## Recommended .gitignore

Create a file called `.gitignore` in the root of your repo:

```
# Data files (too large for GitHub)
*.csv
*.tsv
*.h5
*.pkl
data/

# Jupyter checkpoints
.ipynb_checkpoints/

# Python
__pycache__/
*.pyc
.env

# OS files
.DS_Store
Thumbs.db
```

Note: Keep small CSV files that are needed to run your notebooks.
Small sample datasets are fine — just don't upload large raw data files.
