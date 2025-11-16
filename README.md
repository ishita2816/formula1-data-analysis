# formula1-data-analysis
I am passionate about Formula-1 racing so I thought I would combine two things I love the most, data and racing. So here's data analysis of Formula 1 races focusing on driver performance, pit strategy, team dominance, and race outcome prediction.
## data sources 
https://www.formula1.com
## steps for inquiring data 
1. making excel tables out of racing results data on official F1 website 
2. converting those excel tables to csv
3. reading all these csv files in jupyter notebook and displaying first few rows
4. combining all these csv files into one using pd.concat 

## basic visualizations to get a feel of data
1. Counting wins per driver and plotting a bar graph
2. counting wins per team and plotting a bar graph
3. counting races per year and plotting a line graph

## analyses 
1. Driver Performance: Lewis Hamilton dominates the decade with 83 wins, followed by Max Verstappen with 63 wins. Other drivers, like Charles Leclerc and Carlos Sainz, have sporadic wins at specific circuits, showing targeted strengths.
2. Team Dominance: Mercedes is the leading team with 116 wins, followed by Red Bull Racing and Ferrari. A few teams dominate nearly every track, emphasizing the importance of team strategy in F1.
3. Track-Specific Performance: Certain drivers and teams consistently perform well at specific circuits. Hamilton and Mercedes dominate tracks like Abu Dhabi, Great Britain, and Japan, while Red Bull Racing excels at Austria, Mexico, and Monaco.
4. Race Trends: Most seasons have 21–24 races, though some years like 2023 had more races. Variations reflect calendar adjustments and extraordinary circumstances.
### 01_data_collection.ipynb
- Loaded and combined all yearly race results into a single DataFrame.
- Verified data integrity and displayed the first few rows.
- Saved the combined dataset as `all_f1_data.csv` in the `data/` folder.
### 02_track_performance.ipynb
- Analyzed which drivers and teams win at which tracks (Grand Prix) from 2014–2024.
- Created **heatmaps** showing:
  - Wins per track by driver (`visuals/wins_per_track_driver.png`)
  - Wins per track by team (`visuals/wins_per_track_team.png`)
- Heatmaps saved in `visuals/` for portfolio display.

## errors encountered 
1. the data did not have an year column so we had to use pandas to manually add one
2. after merging my dataset and one from github used for pit stop and grid position there were a few duplicate columns 