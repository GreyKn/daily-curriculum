# Scrabble

Use TDD to create classes that would be used to build a scrabble game (don't actually build a interactive game (yet))

|Letter                        | Value|
|:----------------------------:|:----:|
|A, E, I, O, U, L, N, R, S, T  |   1  |
|D, G                          |   2  |
|B, C, M, P                    |   3  |
|F, H, V, W, Y                 |   4  |
|K                             |   5  |
|J, X                          |   8  |
|Q, Z                          |   10 |

## Bronze

Minimum 8 specs

#### `Scrabble` class

- `self.score(word)` returns the total score value for the given word (case insensitive)
- `self.highest_score_from(array_of_words)` returns the word in the array with the highest score.
    - Note that it’s better to use fewer tiles, so if the top score is tied between multiple words, pick the one with the fewest letters.
    - But there is a bonus for using all seven letters. If one of the highest scores uses all seven letters, pick that one
    - But if the there are multiple words that are the same score and same length, pick the first one in supplied list

## Silver

Minimum 11 specs

#### `Player` class

- `self.new(name)` creates a new instance with the instance variable `name` assigned
- `#name` returns the `@name` instance variable
- `#total_score` Adds and returns the total score of the players words
- `#won?` If the player has over 100 points, returns `true`
- `#plays` An Array of the words played by the player.
- `#play(word)` Adds the word to the `plays` Array
    - Returns false if player as won
- `#highest_scoring_word` Returns the highest scoring word the user has played.
- `#highest_word_score` Returns the `highest_scoring_word` score.


## Gold

Minimum 5 specs

#### `TileBag` class

- `self.new` creates an instance with a collection of default tiles
- `#draw_tiles(n)` returns n number of random tiles, removes the tiles from the default set.
- `#tiles_remaining` returns the number of tiles remaining in the bag

#### `Player` class

- `#tiles` a collection of letters that the player can play (max 7)
- `#draw_tiles(tile_bag)` fills tiles array until it has 7 letters from the given tile bag

Default Tiles
- A-9
- B-2
- C-2
- D-4
- E-12
- F-2
- G-3
- H-2
- I-9
- J-1
- K-1
- L-4
- M-2
- N-6
- O-8
- P-2
- Q-1
- R-6
- S-4
- T-6
- U-4
- V-2
- W-2
- X-1
- Y-2
- Z-1

## Platinum

Minimum 20 specs

#### `Dictionary` class

Create a method for searching a list of words to determine if a give word is a valid word.

#### `Board` class

Create a `Board` class that has a matrix of tile places. Check if a word can be played on a given tile place in a certain direction.
