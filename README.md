# DATA-202 Starbucks Spending Analysis

Statistical analysis of the Starbucks Customer Ordering Patterns dataset for DATA-202 (Mathematics for Applied Data Science) at San Jose State University.

## Team

| Name |
|------|
| Naman Sudan |
| Priya Venugopal Nair |
| Sanjana Vivek Phalke |
| Varuna Vyomessh |

## Setup

1. **Clone and create environment**
   ```bash
   git clone https://github.com/NamanSudan/data202-starbucks-analysis.git
   cd data202-starbucks-analysis
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

2. **Download the dataset**

   Download from [Kaggle](https://www.kaggle.com/datasets/likithagedipudi/starbucks-customer-ordering-patterns) and place the CSV in `data/`.

3. **Launch JupyterLab**
   ```bash
   jupyter lab
   ```

4. **Open notebooks in order** (01, 02, 03, 04) and run cells.

## Project Structure

```
data202-starbucks-analysis/
├── data/                  # Dataset (not tracked in git)
├── notebooks/             # Jupyter notebooks (one per analysis area)
├── presentation/          # Slides
├── report/                # LaTeX report (10-12 pages, double column)
├── requirements.txt
└── README.md
```

## License

Educational use only, DATA-202 at SJSU.
