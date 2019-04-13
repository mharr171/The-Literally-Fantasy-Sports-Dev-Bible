[The Literally Fantasy Sports Dev
Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# League Model

## Data

| Name | Datatype | Description |
| ---:|:---:| --- |
| name | string | Name of the league |
| founded | integer | Year the league was founded |

##  Relationships

```ruby
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
```

## Functions

User can...

+ Create a League
+ Rename a League
+ Dissolve a League
+ Join a League
+ Leave a League

## Notes

![...](../../resources/ellipsis.gif)
