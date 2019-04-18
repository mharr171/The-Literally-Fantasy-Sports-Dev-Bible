[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Club Model

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| name | string | The name of club. Used on club profile page and leaderboards |
| name_abbr | string | Abbreviation of the club's name |

##  Relationships

<!-- ```ruby
belongs_to :god_box
belongs_to :user
has_many :teams
has_many :players, through: :teams
has_many :leagues, through: :teams
has_many :tournaments, through: :teams
``` -->

## Functions

User can...

+ Create a Club
+ Rename a Club
+ Dissolve a Club (and related teams)

## Notes

[Clubs vs Teams](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/models.md#club-vs-team)