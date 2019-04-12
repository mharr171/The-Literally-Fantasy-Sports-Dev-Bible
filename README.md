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

+ [Player Trait System](#player-trait-system)
+ [Player Face System](#player-face-system)
+ [Training System](#training-system)
+ [Trading System](#trading-system)
+ [Home/Away Crowd Attendance](#home-away-crowd-attendance)
+ [Ratings Based Tournament/Season Play](#ratings-based-tournament-season-play)
+ [Social (Guild) System / Create-A-League](#social-guild-system-create-a-league)
+ ![...](./ellipsis.gif)

### Future Features List

+ [Farm Systems / Multiple Teams](#farm-systems-multiple-teams)
+ ![...](./ellipsis.gif)

### Features In-Depth

##### Player Trait System

![...](./ellipsis.gif)

##### Player Face System

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

![...](./ellipsis.gif)

##### Farm Systems / Multiple Teams

![...](./ellipsis.gif)

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
has_many :players
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

+ Create Team <sup>[1](#team-notes)</sup>
+ Rename Team
+ Dissolve Team

### Player Functions

User can...

+ ![...](./ellipsis.gif)

### Tournament Functions

User can...

+ ![...](./ellipsis.gif)

### League Functions

User can...

+ ![...](./ellipsis.gif)

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

<sup>1</sup> One future feature will be that users of sufficient income or notoriety will be able to control multiple teams, creating a farm system<sup>[↑](#farm-systems-multiple-teams)</sup> for their dynasty.

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