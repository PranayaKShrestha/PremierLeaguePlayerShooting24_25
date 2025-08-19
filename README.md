# Premier League Player Shooting Statistics 2024-2025

## Project Objective 

Create a simple and clear interactive dashboard that displays the shooting statistics and shot map of every Premier League player (excluding goalies) in the 2024-2025 season.

## Dataset Used

- <a href="https://github.com/PranayaKShrestha/PremierLeaguePlayerShooting24_25/blob/main/players_stats_epl_2024.csv">PlayerStatsDataset</a>
- <a href="https://github.com/PranayaKShrestha/PremierLeaguePlayerShooting24_25/blob/main/shot_location_epl_2024.csv">PlayerShotLocationDataset</a>

## Data Scraping Process 

I scraped Premier League shot location data from Understat using the understatapi Python client. First, I pulled all player IDs from the 2024–25 EPL season and looped through each player to collect their shot-level data (x, y coordinates, xG, result, and shot type). To avoid rate limiting, I added error handling and delays between requests. Finally, I combined all player-level DataFrames into a single dataset. I excluded own goals from the dataset and removed any games that were not in the Premier League. 

## Dashboard

<img width="1948" height="1196" alt="image" src="https://github.com/user-attachments/assets/a1fd71d0-f2dd-4428-8fdd-505c0a3713ab" />

<img width="1978" height="1194" alt="image" src="https://github.com/user-attachments/assets/84a976a0-c183-4323-8a1a-241345725d94" />



Interactive Filters (Top Bar)

Filter by Player, Result (Goal, Blocked, Missed, etc.), and Shot Type (Left Foot, Right Foot, Header, etc.) to drill into specific subsets of data.

Summary KPIs (Top Row)

Goals: Total number of goals scored.

xG (Expected Goals): Sum of all xG values for the selected dataset.

xG Difference: Goals minus xG, showing overperformance or underperformance.

xG Chain: Total xG contributions including passes leading to shots.

xG Buildup: xG created through possession sequences excluding shots/assists.

Shot Type Distribution (Top Right)

Pie chart displaying the breakdown of shots taken with Right Foot, Left Foot, Head, or Other Body Parts.

Density Shot Map (Bottom Left)

Heatmap visualization of shot locations across the pitch, highlighting high-volume shooting areas.

Shot Result Map (Bottom Right)

Scatter plot showing individual shot outcomes, color-coded by Result (Goal, Blocked, Missed, Saved, Shot on Post).

Provides spatial context for how effective shooting has been from different areas.
