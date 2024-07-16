# Chezz Design

For developer use.

## Version 0.1

### Board

Always represents a valid position. (Board has one of each king, castle rights are logical, enPassant is logical, half and full moves are logical)

#### Fields

pieceArray
turn
whiteKingCastle
whiteQueenCastle
blackKingCastle
blackQueenCastle
enPassant
halfMove
fullMove

#### Member Functions

String - Prints out the board (turn not necessary)
NewBoard - Generates a board with the default position
Clone
ReadFEN - err
GenerateFEN
Getters for everything (pieceArray should just be At - error if not a valid Square)
Move - returns error if invalid
IsStaleMate
IsCheckMate
GenerateLegalMoves

### Piece

Color
Type

#### Member Functions

MakePiece(rune) - Only ascii - err else
String - (Prints out values if not a normal piece)

### PieceType

value

### Color

value

#### Member Functions

String

### Square

value

#### Member Functions

MakeSquare
String - (Prints out value if not normal square)

ALLSQUARES

### Move

FromSquare
ToSquare
Promotion

#### Member Functions

String
MakeMove - (UCI representation)

## Version 0.2

### Game

These are things we want for game, note that this isn't fully fleshed out, it will be neccessary to determine how result is kept track of. (Should it be public or private, is it automatically updated?)

#### Fields

Board*
Result
MoveHistory
Tags (map[string]string)

#### Member Functions

String - Prints out the board along with who's turn it is.
Clone
NewGame - Necessary because of map and board
ToPGN
FromPGN
PrettyString

### Board

#### Member Functions

PrettyString
GeneratePseudoLegalMoves

### Piece

#### Member Functions

PrettyString

## Version 0.3

UCI Support
