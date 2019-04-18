[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# User Model

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| email | string | Used for logging in |
| password | string | Used for logging in |
| name | string | Used to address the user in-game and displayed on profile page |

##  Relationships

<!-- ```ruby
has_one :club
has_one :god_box, through: :club
has_many :teams, through: :club
has_many :players, through: :teams
has_many :tournaments, through: :teams
has_many :leagues, through: :teams
``` -->

## Functions

User can...

+ Sign up
+ Log in
+ Log Out

## Notes

![...](../../resources/ellipsis.gif)
