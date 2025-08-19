# Premier League Player Shooting Statistics 2024-2025

## Project Objective 

Create a simple and clear interactive dashboard that displays the shooting statistics and shot map of every Premier League player (excluding goalies) in the 2024-2025 season.

## Dataset Used

- <a href="https://github.com/PranayaKShrestha/PremierLeaguePlayerShooting24_25/blob/main/players_stats_epl_2024.csv">PlayerStatsDataset</a>
- <a href="https://github.com/PranayaKShrestha/PremierLeaguePlayerShooting24_25/blob/main/shot_location_epl_2024.csv">PlayerShotLocationDataset</a>

## Data Scraping Process 

I scraped Premier League shot location data from Understat using the understatapi Python client. First, I pulled all player IDs from the 2024–25 EPL season and looped through each player to collect their shot-level data (x, y coordinates, xG, result, and shot type). To avoid rate limiting, I added error handling and delays between requests. Finally, I combined all player-level DataFrames into a single dataset. I excluded own goals from the dataset and removed any games that were not in the Premier League. 

## Dashboard



