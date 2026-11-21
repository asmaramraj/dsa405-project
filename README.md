## P3: Acquisition and Integration

### Data Sources
- **Original publisher:** Szymon Jwiak (Kaggle)
- **Dataset:** NBA Scoring Boxscores
- **Publisher URL:** https://www.kaggle.com/datasets/szymonjwiak/nba-scoring-boxscores-1997-2023
- **Acquisition URL:** https://raw.githubusercontent.com/asmaramraj/dsa405-project/main/data/raw/archive.zip
- **Files:** scoring.csv and team_scoring.csv

### Acquisition Method
I used Python's requests library to retrieve a ZIP archive from GitHub. My acquisition code includes a coursework User-Agent, a one-second delay, local caching, and error handling. The downloaded data is saved to the data/raw folder.

### A8 Plan Comparison
In A8, I planned to use public basketball data instead of scraping restricted NBA.com endpoints. I did not specify the exact publisher, URL, or acquisition method. In P3, I used data originally obtained from Kaggle and automated retrieval from a GitHub-hosted copy. This follows my general approach but adds acquisition details that were missing from A8.

### Join and Verification
I joined Charlotte Hornets game records with their opponents' scoring records using gameid and a one-to-one inner join. The result contained 82 games, including 41 home and 41 away games. Assertions verified the row count, unique game IDs, missing values, and scoring percentages.

### How to Run
1. Open DSA405_002_FA26_P3_asmaramr.ipynb in Google Colab.
2. Run all cells in order.
3. The acquisition code retrieves and caches the ZIP archive.
4. The notebook extracts the CSV files, performs the join, and runs verification checks.
