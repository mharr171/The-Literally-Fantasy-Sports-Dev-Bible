[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Match Report Model

Match Reports are...

**Tournament** Match Reports will *expire* after 72 *actual* hours.

**League** Match Reports will *expire* after 144 *actual* hours.

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| home_id | integer | Used to access home team data |
| away_id | integer | Used to access away team data |
| tournament_id | integer | *NULL* or the id of the tournament the match belongs to. |
| league_id | integer | *NULL* or the id of the league the match belongs to. |

| Name | Datatype | Description |
|:--- |:---:| --- |
| home_score | integer | Number of goals scored by the home team |
| away_score | integer | Number of goals scored by the away team |
| home_roster_id_(1-15) | integer | Used to access home team player data |
| away_roster_id_(1-15) | integer | Used to access away team player data |

##  Relationships

<!-- ```ruby
has_many :match_events
``` -->

## Functions

User can...

+ View the match report
+ Click through different stats pages

## Notes

TODO: Create match_event model? (Do I still want to use match_events? Too many objects?)
TODO: Decide additional data needed after flushing out match engine and player models
