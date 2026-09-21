# NBA Draft Combine Exploratory Data Analysis

An exploratory data analysis (EDA) of NBA Draft Combine data using Python, Pandas, and Matplotlib in a Jupyter Notebook. The analysis investigates player measurements, athletic performance, and positional trends.

## Dataset

- **Source:** NBA Draft Combine dataset from Kaggle
- **File:** `draft_combine_stats.csv`: 1,202 player records from the 2001–2023 combines
- **Columns analyzed:** season, player name, position, height (without shoes), wingspan, weight, standing reach, and max vertical leap
- **Cleaning:** kept only the columns above and dropped rows with missing values

## Research Questions

1. How many players participated in the combine by position?
2. What is the average weight of centers, and how does it compare to the average combine player?
3. What is the relationship between height and weight among combine players?
4. Is there a correlation between wingspan and maximum vertical leap?
5. Which guards (PG, SG, PG-SG, SG-PG) are above the median for vertical leap, standing reach, and wingspan?
6. Who were the tallest and heaviest players in each combine season?

## Approach

- Filtered the dataset to the relevant columns and removed rows with missing values
- Counted players by position and plotted the counts as a bar chart
- Compared the average weight of centers to the overall average
- Plotted scatter plots of height vs. weight and wingspan vs. max vertical leap
- Filtered guards above the median of all combine players on all three athletic measurements: max vertical leap > 34.5 in, standing reach > 104 in, wingspan > 82.75 in
- Used `groupby` with `idxmax` to find the tallest and heaviest player in each season

## Key Findings

- Power forwards, point guards, and shooting guards were the three most common positions in the dataset.
- Centers averaged roughly 250 lb, compared with roughly 215 lb for all combine players.
- The height vs. weight scatter plot shows a strong positive relationship.
- The wingspan vs. max vertical leap scatter plot shows a weak or slightly negative relationship.
- Only three guards cleared the above-median cutoff on all three measurements: Xavier Henry, Jalen Williams, and Maxwell Lewis.
- The tallest and heaviest player each season was usually a frontcourt player, most often a center.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Jupyter Notebook

## Skills Demonstrated

- Data cleaning
- Exploratory data analysis (EDA)
- Data visualization
- GroupBy operations
- Filtering and aggregation
- Interpreting scatter plots and summary statistics

## Visualizations

- Bar chart of players by position
- Scatter plot of height vs. weight
- Scatter plot of wingspan vs. max vertical leap
- Tables of elite athletic guards and of the tallest and heaviest players per season

## How to Run

```bash
git clone https://github.com/jalsavani/NBA-Draft-Combine-EDA.git
cd NBA-Draft-Combine-EDA
pip install pandas matplotlib jupyter
jupyter notebook data_exploaration.ipynb
```

Keep `draft_combine_stats.csv` in the same folder as the notebook.

## Project Structure

```
NBA-Draft-Combine-EDA/
├── data_exploaration.ipynb   # Full analysis notebook
├── draft_combine_stats.csv   # Kaggle dataset
└── README.md
```

## Future Improvements

- Compute correlation coefficients instead of relying on scatter plots alone
- Calculate the elite-athlete cutoffs with `quantile()` rather than hardcoding them
- Add regression analysis
- Build interactive visualizations with Plotly
- Create positional clustering models
- Explore trends across combine seasons

## Author

**Jal Savani**: [GitHub](https://github.com/jalsavani) · [LinkedIn](https://www.linkedin.com/in/jal-savani-170413346)
