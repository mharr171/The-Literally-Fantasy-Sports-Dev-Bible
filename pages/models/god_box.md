[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# God Box

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| year | integer | The current year in-game |
| week | integer | The current week in-game |
| day | integer | The current day in-game |
| tournament_freq | integer | The number of ms between each tournament |

**Related to [Player](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/models/player.md)**

| Name | Datatype | Description |
|:--- |:---:| --- |
| stat_play_side_growth | integer | The amount of growth for Player.stat_play_side_* |
| stat_play_side_decay | integer | The amount of decay for Player.stat_play_side_* |
| stat_play_side_decay_after | integer | How many games not playing in a particular position before stats begin to decay |
|  |  |  |
|  |  |  |

##  Relationships

<!-- ```ruby
has_many :clubs
has_many :users, through: :clubs
has_many :teams, through: :users
has_many :tournaments
has_many :leagues
``` -->

## Functions

Admin can...

+ Set the time interval for tournaments
+ Manually run tournaments
+ Send notifications to all users playing on the particular godbox (server of sorts)

## Notes

From Game Engine:
> The God Box will be responsible for holding settings for running both the game and match engines. Here, admins will be able to adjust things like the frequency of tournaments, how quickly reputation grows/wanes, or global rates for skill progressions.

Some of these features may be postponed or cancelled.

**Possible Time Scale**
In game there will be 12 months, each with 4 weeks, made up of 7 days

| Real Time | In Game | Notes |
|:---:|:---:| --- |
| 1 Hour | 1 Day |  |
| 7 Hours | 1 Week |  |
| 28 Hours | 1 Month |  |
| 84 Hours | 3 Months | Tournament is held |
| 14 Days | 1 Year |  |
| 70 Days | 5 Years | Decent Length Career |
| 140 Days | 10 Years | Good Length Career |
| 210 Days | 15 Years | Great Length Career |
| 280 Days | 20 Years | Amazing Length Career |
| 350 Days | 25 Years | Godlike Length Career |

TODO: Relationships for all models