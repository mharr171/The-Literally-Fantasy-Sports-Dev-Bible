[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Team Model

## Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | The name of team. Used on team profile page and leaderboards |
| name_abbr | string | Abbreviation of the team's name |

##  Relationships

```ruby
has_one :user
has_many :players
has_one :league
has_one :tournament
```

## Functions

User can...

+ Create a Team <sup>1</sup>
+ Rename a Team
+ Dissolve a Team

## Notes

<sup>1</sup> One future feature will be that users of sufficient income or notoriety will be able to control multiple teams, creating a farm system<sup>[*](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible/blob/master/pages/features.md#farm-systems--multiple-teams)</sup> for their dynasty.
