[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Match Report Model

## Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| home_id | integer | Used to access home team data |
| away_id | integer | Used to access away team data |
| home_score | integer | Number of goals scored by the home team |
| away_score | integer | Number of goals scored by the away team |
| league_id | integer | Null or the id of the league the match belongs to. |
| is_tournament | boolean | True if the match is part of a tournament |
| active_tournament | boolean | True if the tournament is still active. At the end of the tournament, all users will have all of their matches change this boolean to false |

##  Relationships

```ruby
has_many :match_events
has_one :user, through: :team
has_one :tournament, through: :team
has_one :league, through: :team
```

## Functions

User can...

+ View the match report
+ Click through different stats pages

## Notes

![...](../../resources/ellipsis.gif)
