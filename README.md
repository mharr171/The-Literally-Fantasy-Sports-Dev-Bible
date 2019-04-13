# The Literally Fantasy Sports Dev Bible

<p align="center">
<img src="https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/raw/master/lfs.png" width="50%" alt="Screencap from Literally Fantasy Sports 'proof-of-concept'">
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
+ [Features In-Depth](#features-in-depth)

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
+ ![...](./ellipsis.gif)

### Future Features List

+ [Farm Systems / Multiple Teams](#farm-systems--multiple-teams)
+ [Various League Types](#various-league-types)
+ ![...](./ellipsis.gif)

### Features In-Depth

##### Player Ability System

Each player will have the potential to unlock a set number of abilities that may correlate with either their personalities, position, or playstyle.

##### Player Personality System

A multitude of personalities will run rampant through the leagues, from hard-working to natural talent, brooders and emotions that shoot over the moon. Users will have to manage different personalities within their squad.

##### Player Personality System

The more players have time to practice and play together, the better their performance on the pitch will be. Some players will gel together quickly while others may take more time.

##### Player Face System

Every player will have a unique face with millions of possible combinations of available facial features, allowing every player to make a lasting impact.

##### Squad Heatmap System

![...](./ellipsis.gif)

##### Training System

![...](./ellipsis.gif)

##### Trading System

![...](./ellipsis.gif)

##### Home/Away Crowd Attendance

![...](./ellipsis.gif)

##### Ratings Based Tournament/Season Play

![...](./ellipsis.gif)

##### Social (Guild) System / Create-A-League

Create a league with friends (or strangers) to get more regular playing time for your squad and win big prizes. From a single-owner league to democratic leagues with rule-changing votes, you'll have more matches on your schedule than you can handle! The social system gives you opportunities to play the same teams and compete against eachother over longer periods of time.<sup>[Various League Types](#various-league-types)</sup>


##### Farm Systems / Multiple Teams

Once you've proven you can be successful, you will have the opportunity to open up a second team to play in divisions below your top squad meaning more players, more games, more money.


##### Various League Types

Two types of leagues may become available for creation. The first being a democratic league with rules that are voted on periodically by teams who have ownership in the league. The second would be a league started and owned by a single player with rules set only by them. <sup>1∵</sup>

<sup>1∵</sup> Motorsport Manager

<!--

##### N_e_w

![...](./ellipsis.gif)

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
| manager_name | string | Used to address the user in-game and displayed on profile page |

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
| team_name | string | The name of team. Used on team profile page and leaderboards |

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
|  |  |  |

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
|  |  |  |

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
|  |  |  |

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

+ ![...](./ellipsis.gif)

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

![...](./ellipsis.gif)

### Team Notes

<sup>1</sup> One future feature will be that users of sufficient income or notoriety will be able to control multiple teams, creating a farm system<sup>[↑](#farm-systems--multiple-teams)</sup> for their dynasty.

### Player Notes

![...](./ellipsis.gif)

### Tournament Notes

![...](./ellipsis.gif)

### League Notes

![...](./ellipsis.gif)

<!--

### N_e_w Notes

![...](./ellipsis.gif)

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