# The Literally Fantasy Sports Dev Bible

<p align="center">
<img src="https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/raw/master/resources/lfs.png" width="50%" alt="Screencap from Literally Fantasy Sports 'proof-of-concept'">
</p>


This is the hub for all information pertaining to the development of Literally Fantasy Sports. A very quick, 'proof-of-concept' project can be found [here](https://literallyfantasysports.herokuapp.com).

</br>
</br>
</br>

---

</br>
</br>
</br>

## Index

+ [Features](#features)
+ [Models](#models)
+ [Functions](#functions)
+ [Notes](#notes)

</br>
</br>
</br>

---
[Top](#the-literally-fantasy-sports-dev-bible)


</br>
</br>
</br>

## Features

### Features Index

+ [Pre-Alpha Features List](#pre-alpha-features-list)
+ [Future Features List](#future-features-list)
+ [Features Explained](#features-explained)

### Pre-Alpha Features List

+ [Player Ability System](#player-trait-system)
+ [Player Personality System](#player-personality-system)
+ [Player Chemistry System](#player-chemistry-system)
+ [Player Face System](#player-face-system)
+ [Squad Heatmap System](#squad-heatmap-system)
+ [Training System](#training-system)
+ [Trading System](#trading-system)
+ [Home/Away Crowd Attendance](#homeaway-crowd-attendance)
+ [Ratings Based Tournament/Season Play](#ratings-based-tournamentseason-play)
+ [Social (Guild) System / Create-A-League](#social-guild-system--create-a-league)
+ ![...](./resources/ellipsis.gif)

### Future Features List

+ [Farm Systems / Multiple Teams](#farm-systems--multiple-teams)
+ [Various League Types](#various-league-types)
+ ![...](./resources/ellipsis.gif)

### Features Explained

#### Player Ability System

Each player will have the potential to unlock a set number of abilities that may correlate with either their personalities, position, or playstyle.

#### Player Personality System

A multitude of personalities will run rampant through the leagues, from hard-working to natural talent, brooders and emotions that shoot over the moon after a big win. Users will have to manage different personalities within their squad.

#### Player Personality System

The more players have time to practice and play together, the better their performance on the pitch will be. Some players will gel together quickly while others may take more time.

#### Player Face System

Every player will have a unique face with millions of possible combinations of available facial features, allowing every player to make a lasting impact.

#### Squad Heatmap System

Users will be able to see where their strengths and weaknesses are on the field along with their opponent's. This will allow users to make quick adjustments to their squad to combat another team's strengths or to cover their weaknesses without having to dive deep into numbers. The squad heatmap system aims to create a new way of looking at the game of football.

#### Training System

Users will eventually have a plethora of training options for their players. From individualised sessions to group training, users will have the opportunity to customize their training so they can mold the team of their dreams.

#### Trading System

What sort of fantasy league simulator would this be if you could not trade your players away? Better yet, you can bring in some expensive, shiny, young talent to liven up your squad! Trading will allow different types of playstyles for all users, giving users the option to buy their talent rather than groom it themselves.

#### Home/Away Crowd Attendance

Home field advantage is definitely a thing but so is the support of your travelling fans. Grow your reputation to encourage more fans to follow your team on the road, schedule busses to shuttle them along with the team, or outright ban away supporters' sections in your own stadium. The choice will be yours, but remember that everything has a consequence!

#### Ratings Based Tournament/Season Play

Each team will have a rating (elo-esque) that will help match them against evenly matched opponents for regularly scheduled tournaments. This is the base of the game itself and the games that teams MUST play.

#### Social (Guild) System / Create-A-League

Create a league with friends (or strangers) to get more regular playing time for your squad and win big prizes. From a single-owner league to democratic leagues with rule-changing votes, you'll have more matches on your schedule than you can handle! The social system gives you opportunities to play the same teams and compete against eachother over longer periods of time.<sup>[Various League Types](#various-league-types)</sup>


#### Farm Systems / Multiple Teams

Once you've proven you can be successful, you will have the opportunity to open up a second team to play in divisions below your top squad meaning more players, more games, more money.


#### Various League Types

Two types of leagues may become available for creation. The first being a democratic league with rules that are voted on periodically by teams who have ownership in the league. The second would be a league started and owned by a single player with rules set only by them. <sup>1∵</sup>

<sup>1∵</sup> Motorsport Manager

<!--

#### N_e_w

![...](./resources/ellipsis.gif)

-->

</br>
</br>
</br>

---
[Top](#the-literally-fantasy-sports-dev-bible) • [Features Index](#features-index)


</br>
</br>
</br>

## Models

### Models Index

+ [User](#user-model)
+ [Team](#team-model)
+ [Player](#player-model)
+ [Tournament](#tournament-model)
+ [League](#league-model)

### User Model

+ [User Functions](#user-functions)
+ [User Notes](#user-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| email | string | Used for logging in |
| password | string | Used for logging in |
| name | string | Used to address the user in-game and displayed on profile page |

####  Relationships

```ruby
has_many :teams
has_many :players, through: :teams
has_many :tournaments, through: :teams
has_many :leagues, through: :teams
```

### Team Model

+ [Team Functions](#team-functions)
+ [Team Notes](#team-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | The name of team. Used on team profile page and leaderboards |
| name_abbr | string | Abbreviation of the team's name |

####  Relationships

```ruby
has_one :user
has_many :players
has_one :league
has_one :tournament
```

### Player Model

+ [Player Functions](#player-functions)
+ [Player Notes](#player-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name_first | string | Player's first name |
| name_last | string | Player's last name |
| age | integer | Player's age as a whole number |
| age_progress | float | Player's progress towards incrementing age |

####  Relationships

```ruby
has_one :team
has_one :user, through: :team
has_one :tournament, through: :team
has_one :league, through: :team
```

### Tournament Model

+ [Tournament Functions](#tournament-functions)
+ [Tournament Notes](#tournament-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | Name of the Tournament |

####  Relationships

```ruby
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
```

### League Model

+ [League Functions](#league-functions)
+ [League Notes](#league-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | Name of the league |
| founded | integer | Year the league was founded |


####  Relationships

```ruby
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
```

<!--

### N_e_w Model

+ [N_e_w Functions](#n_e_w-functions)
+ [N_e_w Notes](#n_e_w-notes)

#### Data

| Name | Datatype | Description |
| ---:|:---:| --- |
|  |  |  |

####  Relationships

```ruby
```

-->

</br>
</br>
</br>

---
[Top](#the-literally-fantasy-sports-dev-bible) • [Models Index](#models-index)


</br>
</br>
</br>

## Functions


### Functions Index

+ [User](#user-functions)
+ [Team](#team-functions)
+ [Player](#player-functions)
+ [Tournament](#tournament-functions)
+ [League](#league-functions)

### User Functions

User can...

+ Sign up
+ Log in
+ Log Out

### Team Functions

User can...

+ Create a Team <sup>[1](#team-notes)</sup>
+ Rename a Team
+ Dissolve a Team

### Player Functions

User can...

+ Scout for New Players
+ Train a Player
+ Heal a Player
+ Trade a Player
+ Sell a Player

### Tournament Functions

User can...

+ Opt Into a Tournament
+ Opt Out of a Tournament

### League Functions

User can...

+ Create a League
+ Rename a League
+ Dissolve a League
+ Join a League
+ Leave a League

<!--

### N_e_w Functions

User can...

+ ![...](./resources/ellipsis.gif)

-->

</br>
</br>
</br>

---
[Top](#the-literally-fantasy-sports-dev-bible) • [Functions Index](#functions-index)


</br>
</br>
</br>

## Notes

### Notes Index

+ [User](#user-notes)
+ [Team](#team-notes)
+ [Player](#player-notes)
+ [Tournament](#tournament-notes)
+ [League](#league-notes)


### User Notes

![...](./resources/ellipsis.gif)

### Team Notes

<sup>1</sup> One future feature will be that users of sufficient income or notoriety will be able to control multiple teams, creating a farm system<sup>[↑](#farm-systems--multiple-teams)</sup> for their dynasty.

### Player Notes

![...](./resources/ellipsis.gif)

### Tournament Notes

![...](./resources/ellipsis.gif)

### League Notes

![...](./resources/ellipsis.gif)

<!--

### N_e_w Notes

![...](./resources/ellipsis.gif)

 -->

<!--

<sup>[1](#s_u_b_j_e_c_t-notes)</sup> 

-->

<!--

<sup>[↑](#s_u_b_j_e_c_t)</sup> 

-->

</br>
</br>
</br>

---
[Top](#the-literally-fantasy-sports-dev-bible) • [Notes Index](#notes-index)


</br>
</br>
</br>