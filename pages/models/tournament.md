[The Literally Fantasy Sports Dev
Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Tournament Model

## Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | Name of the Tournament |

##  Relationships

```ruby
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
```

## Functions

User can...

+ Opt Into a Tournament
+ Opt Out of a Tournament

## Notes

![...](../../resources/ellipsis.gif)
