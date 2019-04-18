[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# League Model

Leagues will have two possible starting dates throughout the in-game year. Larger leagues will span an entire in-game year while small leagues may run 2 seasons during an in-game calendar year.

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| name | string | Name of the league |
| founded_year | integer | Year the league was founded |
| founded_month | integer | Month the league was founded |

##  Relationships

<!-- ```ruby
belongs_to :god_box
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
``` -->

## Functions

User can...

+ Create a League
+ Rename a League
+ Dissolve a League
+ Join a League
+ Leave a League

## Notes

**Possible League Styles**
+ [Round Robin](#round_robin)

### Round Robin

Round Robin would require that every team plays each team an equal number of times.
