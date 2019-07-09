---
layout: post
title:      "Feature Selection in the World of Data Science"
date:       2019-07-09 02:31:23 +0000
permalink:  feature_selection_in_the_world_of_data_science
---

   
**What is Feature Selection**
Data scientists use feature selection to help them better select the features, or independent variables, which will most contribute to their prediction variable or target. It is a core concept to the data preparation processes data scientists run on a consistent basis and work to improve the overall performance of both classification and regression models. Choosing the best features is just as important as eliminating the worst features as detractors can significantly affect the model’s output. Irrelevant features add unnecessary noise to ML models and detract from the overall accuracy, efficiency, and value as a predictor. Very simply, feature selection aids in the efforts to:

* Improve Accuracy
* 
* Reduce Overfitting
* 
* Reduce Training Time 

All of the noted improvements above due to feature selection are measurable! Try running your initial models without any feature selection first to ensure the impact resonates.

**My Recent Experience with Feature Selection**
On a recent project, I worked with an impressive dataset that contained over 1.7 million player records from actual matches of Player Unknown’s Battlegrounds (PUBG). PUBG is an incredibly popular online multiplayer battle royale video game developed and published by PUBG Corporation. In the game, up to one hundred players parachute onto an island and scavenge for weapons and equipment to kill others while avoiding getting killed themselves.

Gameplay Overview
Battlegrounds is a player versus player shooter game in which up to one hundred players fight in a battle royale, a type of large-scale last man standing deathmatch where players parachute onto an island, scavenge for weapons and equipment, and fight to remain the last alive. 
 
Each match starts with players parachuting from a plane onto one of the four maps. The plane's flight path across the map varies with each round, requiring players to quickly determine the best time to eject and parachute to the ground. Players start with no gear beyond customized clothing selections which do not affect gameplay. Once they land, players can search buildings, ghost towns and other sites to find weapons, vehicles, armor, and other equipment. These items are procedurally distributed throughout the map at the start of a match, with certain high-risk zones typically having better equipment. Killed players can be looted to acquire their gear as well. 
 
Players can opt to play either from the first-person or third-person perspective, each having their own advantages and disadvantages in combat and situational awareness; though server-specific settings can be used to force all players into one perspective to eliminate some advantages. Players can choose to enter the match solo, duo, or with a small team of up to four people. The available safe area of the game's map decreases in size over time, directing surviving players into tighter areas to force encounters. The last player or team standing wins the round.

In my project, I focused on Squad FPP (First Person Perspective) games to predict winning and losing players based on a large set of available features. As a gamer and competitive person, I jumped at the opportunity to analyze player statistics and put my data science skills to good use.

I will walk you through the basic techniques and steps involved in feature selection. At a high level, I will be evaluating features based on:

* Statistical Impact: looking at scale, range, distribution, normality, multicollinearity, type (numerical/categorical)
* 
* Model-Driven Feature Importance testing
* 
* Situational Context and Experience 

**Initial Exposure - Gaining a Better Understanding of the Features**

Step 1 of the OSEMN Data Science Framework mandates that we Obtain our data and then proceed to consume it. We can quickly do this by downloading this available PUBG dataset on Kaggle and passing it into a Pandas Data Frame for us to work with going forward.  We can now preview our data and initiate our first exposure to the raw available features. To better organize this information, it would be best to create a data dictionary of the features with descriptions in context of dataset and then designate a target variable.

Data Dictionary for Team First Person Player PUBG Dataset

* Player_Id: Unique Player ID 
* 
* Team_Id: Unique Team ID 
* 
* Match_Id: Unique Match ID 
* 
* Assists: Total number of assists the player has utilized 
* 
* Boosts: Total number of boosts the player has scored 
* 
* Damage_Dealt: Total hit points that the player has dealt to opponents 
* 
* Knockdowns: Total number of knockdowns the player has scored - DBNO - "Down but not      out" 
* 
* Headshot_Kills: Total number of headshot kills the player has scored 
* 
* Heals: Total number of heals the player has performed 
* 
* Killer_Placement: Ranking of the player that killed you 
* 
* Kill_Points: Total number of kills the player has scored 
* 
* Kills: Total number of kills the player has scored 
* 
* Kill_Streak: Total number of kills in a row, without dying, the player has scored in agame 
* 
* Longest_Kill: The kill from the furthest distance from the victim 
* 
* Match_Duration: The total amount of time of a single match (in seconds) 
* 
* Match_Type: Whether the game was played in first-person (fpp) or third-person (tpp) Max_Place: Player's highest placement at the end of a match 
* 
* Num_Squads: Total number of squads participating in a game 
* 
* Rank_Points: Player's total points from previous matches 
* 
* Revives: Number of revives the player has performed 
* 
* Ride_Distance: Total distance (in meters) that the player has travelled in a vehicle Road_Kills: Player's total kills while in a vehicle 
* 
* Swim_Distance: Total distance (in meters) that the player has swam in the water Friendly_Fire: Total number of friendly-fire kills, when one player kills another player on      his/her squad 
* 
* Vehicle_Destroys: Total number of vehicles destroyed 
* 
* Walk_Distance: Total distance (in meters) that the player has travelled on foot Weapons_Acquired: Total number of weapons a player picks up 
* 
* Win_Points: Total number of points earned from wins 


**Target Variable**
* Win/Loss: Binary 0 or 1 whether the player was on the winning team for the match or was      eliminated


After wrapping your head around the total number and definitions of the features, we can move to phase 2 and look at the features from the perspective of a machine.

**Take Another Look, A Little Deeper This Time**

“Garbage in, garbage out” is a simple but powerful mantra that should be constantly top of mind for data scientists as they begin any project. Pre-processing data is one of the most important (and unfortunately time consuming) steps along the data science pipeline. It introduces the S in OSEMN, Scrubbing. At this stage, we perform many assessments of the data to detect null or missing values, datatypes as well as determine the range, scale, distribution normality. Although this process is exhaustive, it offers us the opportunity to become more intimate with our features. Blood, sweat, and tears that will pay off down the line. In order to improve our output, we need to ensure that the substance we are starting with is pure and without baggage.

*Identifying Datatypes*




*Identifying Null Values*



**In-Depth Statistical Evaluation and Model Readiness Assessment**

Now, we can leverage some useful Python packages and statistical tests to deeply evaluate each feature from an unbiased point-of-view. I started this phase by generating heat map with Seaborn to check the features for evident multicollinearity. Features that are correlated with one another will affect our ability to accurately predict our target. A heat map helps us to detect correlation amongst features to validate their independence from one another amplifying their value to our classification goal. Based on our findings from the heat map, we can create a list of candidates for feature removal and continue to add our evidence to this list to make the best decision at the final phase of this endeavor (sorry to spoil the ending).

*Generate a Heatmap*



*Creating a List for the Feature Candidates for Removal*


Use Histograms with Matplotlib to Visualize the Data
Raw Data



Remove Outliers



Transform numerical features – Log Scaling




**Leverage Prior Knowledge and Expertise** 

Full disclosure, this project requires in-depth knowledge of PUBG gameplay, hundreds of hours of experience on the sticks, and a lot of patience. It also cost me $14.99, the price of the game. But that investment enabled me to become the expert that I needed to be to evaluate the available features in the context of the video game. That context or “gut feeling” is another important tool to leverage in order to augment our statistical tests, data visualization skills, and machine learning models. At this crucial phase, we deep dive on the significance of the features and how they relate to and can predict winning and losing a match.

As a gamer, I felt that the most significant features would be:

* Kills
* 
* Kill Streak
* 
* Kill Points 


Generally, statistics involving concrete actions that directly eliminate opponents and increase the chances for a single player to be the last survivor and win. It makes sense that those players that can more effectively kill other players have a better chance of not being killed themselves.

With this idea in mind, I can prioritize including the above features in my models as I believe them to be significant predictors of match outcomes.

**Put Algorithms to Work**

We have been working very hard to evaluate the available features in this dataset, but now it is time to let our models perform some of the informative validation work for us. Based on the data transformations, outlier removal, and initial eliminations, we can run our rounds of classification with ALL features and perform feature importance tests.

*Logistic Regression Feature Importance*




*Random Forest Feature Importance*




*XGBoost Feature Importance*



The above results can be factored into our “Candidates for Removal List”. As you can see, each of my classification models outputted differing results. But this is to be expected and now we can cater our features to each of the three models I used.

**Make Up Your Mind Already, Soups On**

I have gathered a plethora of evidence around our features in the PUBG dataset. Now that we have this information aggregated, we can finally make the decision and choose the best features for each of our three models.

*Logistic Regression Final Features*


*Random Forest Final Features *


*XGBoost  Final Features *



With our separate data frames in hand, we can perform more EDA or move forward with our Modeling before we finally complete our OSEMN methodology and iNterpret our results.
