# NBA Stats Application

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-2.0+-lightgrey.svg)](https://flask.palletsprojects.com/)
[![Vue.js](https://img.shields.io/badge/Vue.js-3.0+-green.svg)](https://vuejs.org/)
[![SQLite](https://img.shields.io/badge/SQLite-3.0+-blue.svg)](https://www.sqlite.org/)

## Overview
The NBA Stats Application is a web-based platform that allows users to look up and compare player and team statistics from the NBA. The application is built using a combination of Python for the backend, SQL for database management, and Vue.js for the frontend.

## Why this project?
This project was created to gain practical, hands-on experience writing and using SQL within a full-stack web application. Working with NBA data provided a motivating, real-world dataset that made learning concrete: I focused on schema design, data import pipelines, joins and aggregations, window functions, and basic query optimization while building features that surface meaningful basketball insights.

## Screenshots

<a href="screenshots/player_search.png"><img src="screenshots/player_search.png" width="300" alt="Player Search"></a>
<a href="screenshots/player_compare.png"><img src="screenshots/player_compare.png" width="300" alt="Player Comparison"></a>
<a href="screenshots/team_search.png"><img src="screenshots/team_search.png" width="300" alt="Team Search"></a>

## Data Source
The application uses historical NBA data sourced from Kaggle: [Historical NBA Data and Player Box Scores](https://www.kaggle.com/datasets/eoinamoore/historical-nba-data-and-player-box-scores). This dataset includes comprehensive player and team statistics used for analysis and visualization.

## Features
- **Player Search**: Users can search for individual players and view their statistics.
- **Team Search**: Users can search for NBA teams and view their statistics.
- **Player Comparison**: Users can compare statistics between different players.
- **Team Comparison**: Users can compare statistics between different NBA teams.
- **Trend Visualization**: The application provides visual representations of trends in player and team statistics, highlighting positive or negative changes over time.

## Project Structure
The project is organized into two main directories: `backend` and `frontend`.

### Backend
- **app.py**: Main entry point for the Flask backend application.
- **models/player.py**: Defines the `Player` class and its properties.
- **routes/stats.py**: Contains route handlers for fetching statistics.
- **db/schema.sql**: SQL schema for the database.
- **data/**: Directory containing CSV data files (Games.csv, Players.csv, PlayerStatistics.csv, TeamStatistics.csv).
- **check_columns.py**: Script to check data columns.
- **import_csv.py**: Script to import CSV data.
- **setup_env.bat**: Batch file for environment setup.
- **test_api.py**: Script to test the API.
- **requirements.txt**: Lists Python dependencies for the backend.

### Frontend
- **src/App.vue**: Root Vue component for the application.
- **src/main.js**: Entry point for the Vue application.
- **src/components/**: Contains Vue components including PlayerCompare.vue, PlayerSearch.vue, TeamCompare.vue, TeamSearch.vue, and TrendView.vue.
- **src/composables/**: Contains composables like usePlayerSearch.js.
- **src/utils/**: Contains utility files like statUtils.js.
- **package.json**: Configuration file for npm.

## Setup Instructions
1. **Clone the repository**:
   ```
   git clone https://github.com/chriswdev84/nba-stats-app
   cd nba-stats-app
   ```

2. **Backend Setup**:
   - Navigate to the `backend` directory.
   - Install the required Python packages:
     ```
     pip install -r requirements.txt
     ```
   - Set up the database using the schema defined in `db/schema.sql`.

3. **Frontend Setup**:
   - Navigate to the `frontend` directory.
   - Install the required npm packages:
     ```
     npm install
     ```
   - Start the Vue application:
     ```
     npm run serve
     ```

## Running the Application
1. **Backend**:
   - Navigate to the `backend` directory.
   - Run the Flask server:
     ```
     python app.py
     ```

2. **Frontend**:
   - The frontend should be running from the setup. If not, navigate to the `frontend` directory and run:
     ```
     npm run serve
     ```

## API Documentation
The backend provides RESTful APIs for accessing NBA statistics.

### Endpoints
- `GET /api/players/{player_name}`: Fetch player statistics with optional filters (hidePreseason, hidePlayoffs, hideUnplayed).
- `GET /api/teams/{team_name}`: Fetch team statistics.
- `GET /api/players/{player_name}/timeline`: Get trend data for a player.
- `GET /api/teams/{team_name}/timeline`: Get trend data for a team.
- `POST /api/compare_teams`: Compare two teams (placeholder).

For detailed API usage, refer to `backend/test_api.py`.

## Testing
Run the backend tests:
```
cd backend
python test_api.py
```

For frontend testing, use Vue's testing tools if configured.