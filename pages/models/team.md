[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Team Model

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| name | string | The name of team. Used on team profile page and leaderboards |
| name_abbr | string | Abbreviation of the team's name |

##  Relationships

<!-- ```ruby
has_one :club
has_one :user, through: :club
has_many :players
has_one :league
has_one :tournament
``` -->

## Functions

User can...

+ Create a Team
+ Rename a Team
+ Dissolve a Team

## Notes

[Clubs vs Teams](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/models.md#club-vs-team)