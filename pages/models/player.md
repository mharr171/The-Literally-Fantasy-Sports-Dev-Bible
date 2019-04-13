[The Literally Fantasy Sports Dev
Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Player Model

## Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name_first | string | Player's first name |
| name_last | string | Player's last name |
| age | integer | Player's age as a whole number |
| age_progress | float | Player's progress towards incrementing age |

##  Relationships

```ruby
has_one :team
has_one :user, through: :team
has_one :tournament, through: :team
has_one :league, through: :team
```

## Functions

User can...

+ Scout for New Players
+ Train a Player
+ Heal a Player
+ Trade a Player
+ Sell a Player

## Notes

![...](../../resources/ellipsis.gif)
