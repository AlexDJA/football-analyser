# Football Analyser

A machine learning project that predicts football match outcomesfor teams in the Top Five European Leagues (2024/25 Edition).

## Features

- **Match Outcome Prediction**: Predicts the outcome of matches between any two teams using Random Forest Classifier
- **Team Strength Analysis**: Calculates team strength metrics based on aggregated player statistics

## Project Structure

```
./
├── football_updated.ipynb      # Main notebook for match outcome prediction
├── requirements.txt             # Python dependencies
├── players_data_light-2024_2025.csv  # Dataset (optional - can be downloaded from Kaggle)
└── README.md                    # This file
```

## Prerequisites

- Python 3.8 or higher
- Jupyter Notebook or JupyterLab
- Kaggle account (for downloading the dataset)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/FootballAnalyser.git
   cd FootballAnalyser
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up Kaggle API** (if you want to download data automatically)
   - Go to your Kaggle account settings
   - Download your `kaggle.json` API credentials
   - Place it in `~/.kaggle/kaggle.json` (or `C:\Users\<YourUsername>\.kaggle\kaggle.json` on Windows)
   - Make sure the file has proper permissions (read-only for owner)

## Usage

### Match Outcome Prediction

Open `football_updated.ipynb` and run all cells. The notebook will:
1. Download the dataset from Kaggle
2. Calculate team strength metrics
3. Train a Random Forest model on synthetic match data
4. Allow you to predict match outcomes

**Example:**
```python
predict_match_outcome("Paris S-G", "Barcelona")
predict_match_outcome("Real Madrid", "Bayern Munich")
```

## Dataset

The project uses the [Football Players Stats 2024-2025](https://www.kaggle.com/datasets/hubertsidorowicz/football-players-stats-2024-2025) dataset from Kaggle.

The dataset includes:
- Player statistics (goals, assists, expected goals, etc.)
- Team information (Squad, Competition)
- Match performance metrics

**Note**: The dataset is automatically downloaded when you run the notebooks. If you prefer to use a local copy, you can download it manually from Kaggle and place it in the project directory.

## Technologies Used

- **Python**: Core programming language
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning algorithms
  - Random Forest Classifier
  - Decision Tree Regressor
- **KaggleHub**: Dataset downloading
- **Jupyter Notebook**: Interactive development environment

## Model Details

### Match Prediction Model
- **Algorithm**: Random Forest Classifier
- **Features**: Difference in team statistics (goals, assists, expected goals, pass completion %, etc.)
- **Output**: Win probability for each team and draw probability

### Player Statistics Model
- **Algorithm**: Decision Tree Regressor
- **Features**: Player performance metrics
- **Output**: Predicted goals, assists, and other statistics

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the MIT License.

## Acknowledgments

- Dataset provided by [hubertsidorowicz](https://www.kaggle.com/hubertsidorowicz) on Kaggle

