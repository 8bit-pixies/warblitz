# Design

## User Interface

The key motivation for Warblitz is for the game to be played on a chess board, and open the possibility to be able to quickly to record using chess algebraic notation (though not a hard constraint)

```
8 . . . . . . . .
7 . . . . . . . .
6 . . . . . . . .
5 . . . . . . . .
4 . . . . . . . .
3 . . . . . . . .
2 . . . . . . . .
1 . . . . . . . .
  a b c d e f g h
```

Having this easily representable on a chessboard also means that it is easy to implement and test out AI ideas and game ideas.

## Units

K - commander (King)

R - sniper (Rook)
N - knight (Knight)
B - bishop (Bishop)

A - archer (-)
S - soldier (-)
M - mage (-)

This enables ascii UI to be generated

```
 8 . . . . . . . .  + <Jad the Barbarian>
 7 . . k . f . . .  | Commander, Cost: [-]
 6 . . a . . . . .  | HP:11/11(+1), STR: 3(-), MEL
 5 . . . . . . . .  | 
 4 . . . . . . . .  | On ATK, gain 1 draw dice at
 3 . . . f . f . .  | beginning of your next turn
 2 . . .[K]. . . .  | if any adj. sq is an ally. 
 1 . . . . . . . .  | 
   a b c d e f g h  + -------------------------
                    | HND: GS,
<rel> TR,           | DEF:-, ATK:-, SPC:-
<REL>               * EVT:-, BST:-,
```

By convention the player that starts first will be on the "white" side and the player that starts second will be on the "black" side.

On the left side is all information which is public to both players. On the right, bottom side is all information which is private to the player. On the right, top side is the information card based on what is selected by `[ ]`.

General abbreviations

* ATK: Attack
* BST: Boost
* DEF: Defense
* EVT: Event
* HND: Hand
* HP: Health Points
* SPC: Special
* STR: Strength

The cards and relics are also abbreviated and can be found in the reference sheet. In the UI, the information can be found by moving `[ ]` over the abbreviations