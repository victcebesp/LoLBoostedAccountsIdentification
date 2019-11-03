# League of Legends boosted accounts detection. Data Science

<p align="center">
  <img width="460" height="300" src="images/lol_logo.png">
</p>

## Domain description

League of Legends is a MOBA (Multiplayer Online Battle Arena) computer game. It was release in October 2009 by Riot Games, Inc. and since there, the number of players has been increasing until reaching 100 million players as September 2019. The game consists in two teams of 5 people who choose a champion to play with, trying to destroy the enemy team's base.

The high-end goal of the game is climbing the different leagues from bronze to challenger, where best players play. A possible aim of this project is to find out which differs a challenger player from the ones in lower leagues. In addition, I want to find out if it is possible to identify boosted accounts.

## Analysis strategy and plans

As the data source is an API, initially I will use the requests library to query the API and get the data from different endpoints. This data will be retrieved in a JSON format so I will have to transform it into a dataframe with the variables needed for the analysis. After this, and because of the fact that from different endpoints different kind of information can be retrieved, it will be necessary merging the dataframes created from data of the different APIs.

From this point on, I think it will be interesting calculating the win ratio / win percentage for the best players of each league and compare them to extract some insights from there. In order to go deeper into the details, it will be necessary analyzing many matches from the best players of each league to check if there is a common behavior shared across all of them. In addition, it may be interesting checking the most-used champions in each league and what makes those champions more interesting in order to help the players to move forward higher leagues. Apart from that, it may be interesting comparing players based on other stats.

## Initial investigations and results

Some initial insights have been extracted.

Firstly, we can say that the game is matching the players correctly. This means, that players are matched agains enemies that have the same level. We can see this in the scatter plots for each league where the more games a player plays, the win ratio tends to approach to one.

In addition, beta distributions for the probability of wining a game (wins / totalGames) have been plotted. Something curious is happening here. In lower leagues, players tend to win less than 50% of their matches. Once we start moving toward higher leagues, this probability increases until challenger in which players tend to win around 55% of the matches.

Something strange is happening in platinum. My hypothesis is that this is caused by paid account boostings which could alter other players game experience.

Win ratio (wins / losses) keeps increasing while moving to higher leagues.
