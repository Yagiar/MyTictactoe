<!-- # ⭕ Tic-Tac-Toe -->

[//]: # (<img alt="workshop/tictactoe" width="1412" src="../.resources/tictactoe.png">)

#### A standard game of Tic-Tac-Toe in Leo.
|   |   |   |
|---|---|---|
| ⭕ | ⭕ | ❌ |
| ⭕ | ❌ | ⭕ |
| ❌ | ❌ | ⭕ |

## Model representations
Composite data types are possible to create by creating Leo with the `struct` keyword. 
Leo allow users to define composite data types with Leo, and it is.
The game board is represented by a `struct` called `Board`, which contains three `Rows`.
Another alternative representation can be used as an array, however in Leo, they are not yet supporting this. 

## Code Overview
The code defines two main structs: `Row` and `Board`, to represent a row and the game board, respectively. It also includes functions to create a `new game board`, `check for a win`, `and make a move`.

struct `Row`: Represents a row in the Tic Tac Toe board, with each cell containing a value (0 for empty, 1 for player 1, and 2 for player 2).<br>
struct `Board`: Represents the game board, consisting of three rows.<br>
`new()`: Returns an empty game board.<br>
`check_for_win(b: Board, p: u8)`: Checks if a player (p) has won on the given board (b).<br>
`make_move(player: u8, row: u8, col: u8, board: Board)`: Makes a move for a player on the board and returns the updated board and the winner (0 for no winner, 1 for player 1, 2 for player 2).<br>

## Running the Program

Leo provides users with a command line interface for compiling and running Leo programs.
Users may either specify input values via the command line or provide an input file in `inputs/`.

### Providing inputs via the command line.
1. Run 
```bash
leo run <function_name> <input_1> <input_2> ...
```
See `./run.sh` for an example.


### Using an input file.
1. Modify `inputs/tictactoe.in` with the desired inputs.
2. Run
```bash
leo run <function_name>
```

## Executing the Program
```bash
leo execute <function_name> <input_1> <input_2> ...
```

## Playing the Game

### 1. Create a new game board
```bash
leo run new
```
|   |   |   |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 0 | 0 |
| 0 | 0 | 0 |

### 2. Player 1 makes a move
```bash
leo run make_move 1u8 1u8 1u8 "{ r1: { c1: 0u8, c2: 0u8, c3: 0u8 }, r2: { c1: 0u8, c2: 0u8, c3: 0u8 }, r3: { c1: 0u8, c2: 0u8, c3: 0u8 } }"
```
|   |   |   |
|---|---|---|
| 1 | 0 | 0 |
| 0 | 0 | 0 |
| 0 | 0 | 0 |

### 3. Player 2 makes a move
```bash
leo run make_move 2u8 2u8 2u8 "{ r1: { c1: 1u8, c2: 0u8, c3: 0u8 }, r2: { c1: 0u8, c2: 0u8, c3: 0u8 }, r3: { c1: 0u8, c2: 0u8, c3: 0u8 } }"
```
|   |   |   |
|---|---|---|
| 1 | 0 | 0 |
| 0 | 2 | 0 |
| 0 | 0 | 0 |

Discord: Attak Helicopter#9164
