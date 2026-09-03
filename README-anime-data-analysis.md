# Anime Data Analysis (EDA)

Exploratory data analysis on an anime dataset to understand what actually drives audience engagement — genre popularity, user engagement, and score distribution — using Python, Pandas, and Seaborn/Matplotlib.

## Project Overview

This project explores a large collection of anime titles to answer a simple question: **what makes an anime popular?** Rather than relying on assumptions, the analysis works directly from the data — cleaning it, profiling it, and visualizing it to surface patterns in genre, audience size, and rating behaviour that a casual viewer wouldn't notice.

The goal was to practice a complete, real-world EDA workflow: load messy data, clean and validate it, ask focused questions, and communicate findings through clear visuals rather than raw tables.

## Dataset

- **Source:** Public anime metadata dataset (title, genre(s), type, episodes, score, number of members/ratings, popularity rank, and related metadata).
- **Format:** CSV, loaded and processed with Pandas.
- **Size:** Several thousand titles spanning multiple decades and genres.
- **Preprocessing steps:**
  - Handling missing/placeholder values (e.g. unrated or unaired titles)
  - Splitting and normalising multi-genre fields for genre-level analysis
  - Converting types (episode counts, scores, member counts) to numeric formats
  - Removing duplicate entries and obvious data-entry errors

## Tools & Libraries

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Pandas | Data loading, cleaning, and transformation |
| Matplotlib | Base plotting (distributions, trend lines) |
| Seaborn | Statistical visualizations (box plots, heatmaps, category comparisons) |
| Jupyter Notebook | Interactive analysis and documentation |

## Key Insights

- **Genre popularity is uneven:** A small number of genres (e.g. Action, Comedy, Drama) account for a disproportionate share of highly-rated and highly-engaged titles compared to niche genres.
- **Engagement doesn't always track quality:** Some titles with mid-range scores have very high member/engagement counts, suggesting popularity and critical score measure different things.
- **Score distribution is centrally clustered:** Most anime cluster around an average score band, with relatively few titles at the extreme high or low ends — a fairly normal-shaped distribution once outliers are removed.
- **Format matters:** TV series and movies show different score and engagement patterns compared to OVAs and specials, which tend to have smaller but more dedicated audiences.

## Project Structure

```
anime-data-analysis/
├── data/
│   └── anime_raw.csv
├── notebooks/
│   └── anime_eda.ipynb
├── outputs/
│   └── charts/
├── requirements.txt
└── README.md
```

## Code Execution Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/praveendell6334/anime-data-analysis.git
   cd anime-data-analysis
   ```

2. **Set up a virtual environment (optional but recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the analysis**
   ```bash
   jupyter notebook notebooks/anime_eda.ipynb
   ```
   Run all cells in order — the notebook loads the raw dataset, applies the cleaning steps, and regenerates every chart used in the analysis.

5. **View outputs**
   Generated charts are saved to `outputs/charts/` for use outside the notebook.

## Future Improvements

- Add a genre-based recommendation feature using a simple similarity score
- Bring in release-year metadata to analyse trends over time
- Package the cleaning steps into a reusable Python module

## Author

**S. Praveen** — Aspiring Data & Financial Analyst
📧 praveen70342@gmail.com · [GitHub](https://github.com/praveendell6334)
