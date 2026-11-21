## Project 3: Acquisition and Integration

### Data Sources
This project analyzes Charlotte Hornets scoring statistics from the 2025–2026 NBA season using `scoring.csv` and `team_scoring.csv`.

The CSV files were originally obtained from Kaggle and are retrieved for this notebook from the project's GitHub repository.

GitHub dataset URL:
https://raw.githubusercontent.com/asmaramraj/dsa405-project/main/data/raw/archive.zip

### Acquisition Method
The notebook uses Python's requests library to download the data, saves the raw ZIP file to `data/raw/`, and extracts the CSV files. It includes caching, a coursework User-Agent, a one-second request delay, and HTTP error handling.

### Join Design
The analysis uses `gameid` to match Charlotte Hornets game records with opposing-team scoring records in a one-to-one inner join.

The join produced 82 records, representing 41 home games and 41 away games.

### Verification
The notebook uses assertions to check row counts, duplicate game IDs, missing join keys, valid percentages, and the home/away split.

### How to Run
1. Open `DSA405_002_FA26_P3_asmaramr.ipynb` in Google Colab.
2. Run the notebook cells from top to bottom.
3. The acquisition code downloads and caches the data.
4. The remaining cells perform the join and verification checks.
