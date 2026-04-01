# Contributing Guide

Development workflow and branch conventions for the DATA-202 Starbucks analysis project.

## Branch Naming

All branches follow this pattern:

```
<name>/<type>/<short-description>
```

- `name` is your first name (lowercase)
- `type` is one of the branch types below
- `short-description` is a few words separated by hyphens

### Branch Types

| Prefix | Purpose | Example |
|--------|---------|---------|
| `explore/` | Notebook analysis, data exploration | `naman/explore/spending-distributions` |
| `analysis/` | Statistical tests, modeling | `priya/analysis/hypothesis-testing` |
| `feat/` | New scripts, utilities | `naman/feat/data-prep` |
| `fix/` | Bug fixes | `varuna/fix/notebook-import-error` |
| `chore/` | Dependencies, setup, config | `naman/chore/add-requirements` |
| `docs/` | Documentation, report drafts | `sanjana/docs/update-readme` |
| `presentation/` | Slide decks | `priya/presentation/mid-slides` |

### Examples

```bash
git checkout main
git pull origin main
git checkout -b naman/explore/spending-distributions

git checkout main
git pull origin main
git checkout -b priya/analysis/hypothesis-testing
```

## Git Workflow

We use **trunk-based development** with `main` as the single protected branch.

```
main (protected)
  └── <name>/<type>/<description> (short-lived branches)
```

### Workflow

1. **Pull latest main**: `git pull origin main`
2. **Create a branch** from `main` using the naming convention
3. **Do your work** with clear commits
4. **Push and open a PR** to `main`
5. **Get a review** from at least one teammate
6. **Merge** after approval

### Commit Messages

Keep them short and descriptive:

```
add descriptive stats and outlier detection

- Compute five-number summary for all numerical columns
- IQR-based outlier detection with fence values
- Box plots by order channel and rewards membership
```

## Pull Request Guidelines

### PR Title

Short, descriptive. Examples:
- `Add data exploration notebook`
- `Fix correlation matrix axis labels`
- `Add hypothesis testing for rewards members`

### PR Description

```
## What this does
Brief description of the changes.

## Notebooks affected
- 01_data_exploration.ipynb
```

### Review Process

- At least 1 approval required
- Reviewer should pull the branch and run the notebooks locally
- No direct pushes to `main`

## Local Setup

```bash
git clone https://github.com/NamanSudan/data202-starbucks-analysis.git
cd data202-starbucks-analysis
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Download the dataset from [Kaggle](https://www.kaggle.com/datasets/likithagedipudi/starbucks-customer-ordering-patterns) and place the CSV in `data/`.
