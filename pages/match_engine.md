[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Match Engine

## Index

+ [Match Walkthrough](#match-walkthrough)
+ [Player Positions](#player-positions)
+ [Player Roles](#player-roles)
+ [Player Skills](#player-skills)
+ [Player Chemistry](#player-chemistry)
+ [Heatmaps](#heatmaps)
+ [Home/Away Crowd Attendance](#homeaway-crowd-attendance)

## Match Walkthrough

### Front

+ Each team submits a roster with 11 active players and up to 4 possible subs 
+ Users can set up auto-subs for each active player in case of injury
+ Max one injury per side per match
+ No subs outside of injury
+ Matches are 90 minutes plus stoppage time
+ Each minute consists of TWO ticks
+ Each tick an event may occur
+ A [Match Report](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/models/match_report.md) is generated with the results and displayed for the user.

### Back

#### Subs
4 Subs — 1 FW 1 MD 1 DF 1GK
Any subs will have their footedness and side-to-side playability adjusted to make subbing easier. This means that no 'defender' would be inadequate to sub for any other 'defender' just because of their footedness or because they play on the left instead of the right.

## Player Positions

|   | Positions |
|:---:| --- |
| ST | Striker |
| AM | Attacking Midfielder |
| M | Midfielder |
| DM | Defensive Midfielder |
| D | Defender |
| SW | Sweeper |
| GK | Goalkeeper |

## Player Roles

example: Goalkeeper vs Sweeper Keeper

## Player Skills

Possible Proc Times

+ skills that have odds to proc during attacking phase to boost chances to score
+ skills that have odds to proc during transition phase to boost chances to maintain/obtain possession
+ skills that have odds to proc during defending phase to boost chances to force turnover
+ skills that have odds to proc during any of the three aforementioned phases that specifically counter another skill

<sub>[Game Engine](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/game_engine.md#player-skills)</sub>

## Player Chemistry

![...](../resources/ellipsis.gif)

<sub>[Game Engine](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/game_engine.md#player-chemistry)</sub>

## Heatmaps

![...](../resources/ellipsis.gif)

<sub>[Game Engine](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/game_engine.md#heatmaps)</sub>

## Home/Away Crowd Attendance

![...](../resources/ellipsis.gif)

<sub>[Game Engine](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/game_engine.md#homeaway-crowd-attendance)</sub>
