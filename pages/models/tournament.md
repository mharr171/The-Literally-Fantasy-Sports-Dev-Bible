[The Literally Fantasy Sports Dev Bible](https://github.com/mharr171/The-Literally-Fantasy-Sports-Dev-Bible)

# Tournament Model

## Data

| Name | Datatype | Description |
|:--- |:---:| --- |
| name | string | Name of the Tournament |

##  Relationships

<!-- ```ruby
has_one :god_box
has_many :teams
has_many :players, through: :teams
has_many :users, through: :teams
``` -->

## Functions

User can...

+ Opt Into Future Tournaments
+ Opt Out of Future Tournaments

## Notes

**Possible Tournament Styles**
+ [Single Elimination](#single_elimination)
+ [Double Elimination](#double_elimination)

### Single Elimination

| # of Teams | # of Games |
|:---:|:---:|
| 4 | 3 |
| 8 | 7 |
| 16 | 15 |
| 32 | 31 |
 
### Double Elimination

| # of Teams | # of Games |
|:---:|:---:|
| 4 | 6-7 |
| 8 | 1-15 |
| 16 | 30-31 |
| 32 | 62-63 |
