# pitch_effectiveness
After the cancellation of the 2020 season, Notre Dame baseball has little to no data with which to evaluate pitchers, build development plans and prepare for the 2021 season. Without data from the 2020 season, this project helps pitchers locate their pitches more effectively by taking a weighted average of similar pitchers. The methodology is outlined below:
1. Find the average release height, release side, extension, velocity, horizontal break, and vertical break for every pitch of all of ND's pitchers. eg: Pitcher A's fastball, Pitcher C's curveball.
2. For all pitches of the same pitch type by a pitcher of the same handedness against a batter of the same handedness in a game between two power five teams (all fastballs thrown by RHP to RHH, or all curveballs thrown by LHP to RHH), find the number of standard deviations between that pitch's release height, release side, extension, velocity, horizontal break, and vertical break and the pitcher's average for that pitch type. 
3. For all pitches of the same pitch type in a game between two power five teams, create a similarity score defined as (1/sum(standard deviations))^3
4. This similarity score was used to take a weighted average of three important statistics (whiff rate, average exit velocity, and ground ball rate) in various zones of the strike zone.
5. A heatmap was created to display the weighted averages in various zones of the strike zone. 

- 'data_prep.ipynb' was used to create a properly formatted dataset of all games recorded by a Trackman radar between two power 5 (ACC, SEC, PAC 12, B1G 10, BIG 12) teams
- 'pitcher_grouping.ipynb' was used to perform the data analysis
- sample output graphs are also included
