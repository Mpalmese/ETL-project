Extract, Transform, and Load (ETL) Project


Project Overview:

In this group project, we downloaded two Comma Separated Values (CSV) files from the NHL Game Data on Kaggle. Specifically, we looked at one file with the record of each NHL game in the dataset. The other file looked at the team information, such as names. The purpose of this project was to see how each NHL team performed during the playoffs from 2012-2017 using the ETL process. 

Sources of data: game.csv and team_info.csv
Link: https://www.kaggle.com/martinellis/nhl-game-data#game.csv

Extract and cleaning:
To start, we imported our dependencies (Pandas, Sqlalchemy, MySQLdb) into Jupyter Notebook and extracted raw data from the website. After we exported game data and team info data, we extracted these CSV files into two separate data frames. With proper data cleansing, we were able to combine relevant columns and rename columns in each data frame. 

Transforming:
Next, we transformed game data frame and team info data frame and merged the two tables together as one data frame. The final playoffs data frame contained the columns: 
game_id, season, away_team, home_team, away_goals, home_goals, outcome, winning_team

Load: 
After these steps, the single data frame was uploaded to a SQLite relational database named “playoff_db". The database features information including game id, season (year), away team name, home team name, away goals, home goals, outcome (win or loss), and winning team name. 

The queries consisted of:
1) Playoff_data table, 
2) The winner of the NHL playoffs (2012-2013) season, 
3)  How many goals each team made in the 2012-2013 season in descending order,
4) Query winner of NHL playoffs in 2016-2017 season,
5) How many goals each team made in the 2016-2017 season in descending order. 


**In addition to the SQL database, a Flask application is available to easily traverse the data and locate individual teams and winners of the NHL playoffs. 





