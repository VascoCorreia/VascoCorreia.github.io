---
title: "Fauna Wars"
layout: single
permalink: /fauna-wars/
author_profile: true
toc: true
header:
  overlay_image: 
  overlay_filter: rgba(0, 0, 100, 0.1)
  image_description: "Fauna Wars Banner."
---
<a href="https://github.com/VascoCorreia/Fauna-Wars" target="_blank"> <i class="fab fa-brands fa-github fa-2x"></i></a>
{: .text-right}

## <i class="fa fa-solid fa-book" style="color: #ae0c4e;"></i> Instructions 

Fauna Wars has been developed to be only played on a local computer, the database is created locally and the server runs with NodeJS on the local machine.

To run the server you need to acess the cmd in the folder downloaded using cd "path_to_folder and run the serverScript.js using the command node serverScript.js

Inside the Database folder there are 2 sql scripts used to initialize and populate the database these need to be run for example using MySQL Workbench in order for the game to work. The queries.sql are some test queries that I used.

The game is set to run on port 3306.

## <i class="fas fa-solid fa-gamepad" style="color: #ae0c4e;"></i> Gameplay  
### Map
Clicking the Map box changes the main window to the world map window. Here the player can see his own, his allies and his enemys cities. Clicking on a city will show the Username, player faction, player total points and city name clicking it also allows the player to send an attack if it is an enemy.
See the image below.

![Map](/assets/images/FaunaWars/map.png){: .align-center}  

### City
Clicking the city box changes the main window to the players current selected village view. Here the players can see his buildings and their levels. Here the player can interact with some of his buildings taking him to different windows.

In the build page the player can upgrade the buildings on his currently selected city. Building or upgrading a building cost resources and takes time.

![City](/assets/images/FaunaWars/city.png){: .align-center}  

#### City Dropdown
In this section the player can see the currently selected city name. There is also a button here to show a dropdown menu with all the player cities. Here the player can click a certain city in the dropdown menu to select it.

![City Dropdown](/assets/images/FaunaWars/cityDropdown.png){: .align-center}  

### Buildings
Buildings are one of the main concepts in Fauna Wars. Each building has levels and a level cap to build or upgrade a building you require resources.

You will require more resources the higher the level of the building. The buildings exist in players cities and they define how much points a player possesses. Each building and building level gives the players points

### Attacking and Defending
Attacking is one of the core concepts in Fauna Wars. In the world map view after selecting an enemy city a player can select the attack button which leads the player to the window shown below. Here he can select the number of troops he wants to send in an attack. 

After sending an attack the troops take a set amount of time to arrive at the enemy. The time the army takes to arrive is always calculated depending on the distance between the cities.

![Attack Menu](/assets/images/FaunaWars/attackingMenu.png){: .align-center}  

#### Attack Points
To know the strength of an attack a total of an army Attack points is calculated.

The formula used is:

![Attack Points](/assets/images/FaunaWars/attackPointsFormula.png){: .align-center}  

#### Defense Points
To know the strength of a defense a total of an army Defense points is calculated.

The formula used is:

![Defense Points](/assets/images/FaunaWars/defensePointsFormula.png){: .align-center}  

#### Calculating the winner

To know who wins a battle we calculate the ratio between the Total Attack points of the attacker and Total Defense Points of the Defender is done.

The formula used is:

-If Ratio > 1, then Attacker Wins
-If 0 < Ratio < 1, then Defender Wins
-If Ratio = 1, then Defender Wins  

#### Troops Lost
To know the number of troops the attacker and defender loose in a battle the ratio between the Total Attack points of the attacker and Total Defense Points of the Defender is used. When the ratio is between 0 and 1 (normalized value), the attacker loses all troops since he lost battle and we use this to know of many troops the defender loses.

#### Conquering
When the attacker wins a battle, he conquers the enemy city he attacked. This city belongs now to the attacker and he can do what he wants with it. The resources that were present in the city the moment it was conquered also now belong to the attacker. The buildings stay at the level they were. The only thing that changes is the faction and owner.

### Troops
Clicking the Recruit box changes the main window to the Recruit window. In the city main view clicking on the Barracks will also take the player to this window. Here the player can recruit troops that stay in the city they are being recruited on until the player gives them some action. Recruiting troops cost resources and takes time.

![Troops](/assets/images/FaunaWars/troops.png){: .align-center}  

### Enemy Movements
In this section the player can see information about enemy movements that are happening related to his currently selected city. Enemy movements include attacks coming to the current city.

![Enemy Movements](/assets/images/FaunaWars/EnemyMovements.png){: .align-center}  

### Player Movements
In this section the player can see information about ally movements that are happening related to his currently selected city. Allied movements include his own movements.

![Player Movements](/assets/images/FaunaWars/playerMovements.png){: .align-center}  

### Leadboards
In this section the player can see the leaderboards.

![Map](/assets/images/FaunaWars/leaderBoards.png){: .align-center}  

## <i class="fa fa-solid fa-book" style="color: #ae0c4e;"></i> Documentation 

| Document | View |
| :--------: | :--------: |
| Game Design Document   | [View](https://drive.google.com/file/d/1TWrBPBrXl8kVQZKH6y9IPBuwREMJA5UG/view?usp=sharing){: .btn .btn--primary}   |

