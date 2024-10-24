# Warband Lite Core (Warblitz)

## Object of the Game

Warband-Lite is a 2-player expandable grid-based skirmish game in which players take on the role of battling commanders. They will call forth mighty warriors, maneuver them about the battlefield, and play powerful events in an effort to destroy their opponent’s commanders.

## Component Overview

### Dice

* 3x six sided dice.

### Unit Card

* Name - the name of the unit
* Unit - one of Common/Elite/Commander
* Cost
* Health points
* Attack type - one of Melee/Range
* Ability - the unit's ability

```
+--------------------------------+
|<Name>                          |
|<Unit>, <Cost>                  |
|HP:00<+1>, STR:0<+1>, <MEL/RNG> |
|<Ability>                       |
+--------------------------------+
```

### Event & Relics Card

* Name - the name of the unit
* Unit - one of Common/Elite
* Cost
* Ability
* Phase

```
+----------------+
|<Name>          |
|<Unit>, <Cost>  |
|<Phase>         |
|<Ability>       |
+----------------+
```

## Setup

To setup a game of Warband, follow these steps:

1. Place the battlefield between the players.
2. Create a supply of damage and boost tokens within reach of both players.
3. Each player chooses a faction deck or builds a custom deck.
4. Each player places their commander, 2 starting units, and terrain on the battlefield as shown on the back of their commander's card.
5. Each player shuffles their remaining cards, places them face down into their draw pile.
6. Randomly determine which player will go first. The player that goes second starts their turn with one special token.

## Turn Sequence

Players will alternate taking turns until a player has won the game by destroying their opponent's commander. On a player's turn they must complete the following 5 phases in order:

1. Beginning
2. Deploy
3. Move
5. Attack

After the active player completes all phases, it becomes the opponents turn

### Phase 1: Beginning

At the beginning of their turn, the active player:
* Remove and discard all ATK, DEF, SPC, EVT tokens owned by the active player both in play and being held
* Discards their hand

Unless specified Boost tokens are not removed from play.

Next, any abilities that trigger at the beginning of a turn are resolved.

The player then rolls 3d6 to determine tokens distributed for this turn using the following table

- 1-2: Defend (DEF) token
- 3-4: Attack (ATK) token
- 5: Special (SPC) token
- 6: Event/Special (EVT) token

The DEF token prevents a would from being applied, whilst the ATK token provides an extra hit dice. The SPC token can be used as either a DEF or ATK token. The EVT token can be used a DEF or ATK token or consumed to draw a card from their draw pile and places it in their hand.

The player then may choose to assign DEF or ATK tokens to the units. The player may assign tokens to only their own unit on the battlefield, and may not assign more than one token to a single unit. Note during the course of a players turn, a unit may result in holding more than one token!

### Phase 2: Deployment

Deploy up to two units from your available reserves to the battlefield. To deploy a unit pay its cost by consuming a number of tokens equal to the unit's cost. Tokens consumed in this way are treated to be equivalent to 1 cost. The deployed unit is then place it on an empty space in the last three ranks of the battlefield, but not in front or adjacent to an enemy.

#### Adjacency

A card or space is adjacent to another one if they share an edge. Diagonals are not adjacent.

```
+-----+
|.|Y|.|
|Y|@|Y|
|.|Y|.|
+-----+
```

### Phase 3: Move

Move up to 3 different units you control 1 or 2 spaces each. Units can only move into or through empty, adjacent spaces. 

**Example: Moving**

```
+-----+
|.|^|.|
|.|@|.|
+-----+
```

```
+-----+
|.|^|.|
|.|^|.|
|.|@|.|
+-----+
```

Units can move vertically or horizontally 1 to 2 spaces.

```
+-----+
|.|^|>|
|.|@|.|
+-----+
```

Units can move 1 space vertically and 1 space horizontally or vice versa.

```
+-----+
|.|v|.|
|.|@|.|
+-----+
```

Units can move 1 space and then move back to their original space. (Sometimes units do this to trigger an after moving ability.)

```
+-----+
|.|.|x|
|.|@|.|
+-----+
```

Units CANNOT move diagonally

```
+-----+
|.|x|.|
|.|!|.|
|.|@|.|
+-----+
```

Structures CANNOT move.
Units CANNOT move through other cards.

### Phase 4: Attack

Attack with up to 3 different units you control. (They don’t need to be the same units that moved this turn.) To attack with a unit, follow these steps in order:

1. Declare a Target: Melee units (MEL) can target any adjacent card. Ranged units (RNG) can target any card up to 3 clear straight spaces away.
2. Roll: Roll a number of dice equal to the attacking unit's strength.
3. Add Damage: Add 1 damage to the target for each hit rolled. Ignore Special rolls unless otherwise specified

Melee table

- 1: Special
- 2-5: Hit
- 6: Hit / Special

Range table

- 1: Miss
- 2: Special
- 3-5: Hit
- 6: Hit / Special

**Damaging and Destroying Cards**

To add damage to a card, place damage tokens on it. A card’s life is reduced by 1 for each damage it has. If a unit's life ever reaches 0, that unit is destroyed. Gain 1 BST token each time a unit you control destroys an ENEMY unit.

**The Cost of Inaction**

Add 1 damage to your commander at the end of your Attack Phase if you did not target any enemy cards with an attack this turn.

### Event Cards

Play event cards on your turn during the phase listed on the card. To play an event card, pay its cost, resolve its effects, and then discard it. Event cards cannot be played while a game effect is being resolved, e.g. during deployment, moving, attacking, or when resolving an event, ability or other effect.

**Active Event Effects**

When playing an event with the ACTIVE keyword on it, instead of discarding it, place it in your active area. Event card effects are active while in either active area. At the start of your next turn, discard all events in your active area. Y ou cannot play an active event if you already have an active event with the same name in play.

### Winning the Game

When only 1 player’s commander remains on the battlefield, that player wins.

### Boost

Boost tokens have various effects based on the cards that are in play. To boost a card, place a boost token on it (no maximum). If a card’s effect requires you to spend 1 or more boost, remove that number of boost tokens from that card (the card must have at least that much boost to activate that effect).

### Force

To force a card 1 or more spaces, slide it that many clear straight spaces in a single direction (horizontal or vertical). Forcing a card is NOT considered moving it.

## Warband Construction

All Warbands are to contain:

* 1 Commander
* 3 Elite unit (1x MEL, 1x RNG, 1x Special)
* 12 Common unit (4x MEL, 4x RNG, 4x Special)

The deck contains:

* 2 Epic Events
* 6 Standard Events
* 1 Epic Relic
* 2 Common Relics
* 9 Card tokens (3 Attack, 3 Shield, 3 Special)

For a total of 20 cards.

During the Beginning Phase, you may discard any Event or Relic card for a SPC token. You may also discard any card for a card token of the same type.

**Alternative Mode**

An alternative mode can be played where both players decide not to use relics. In this scenario, the deck list is:

* 2 Epic Events
* 6 Standard Events
* 12 Card tokens (4 Attack, 4 Shield, 4 Special)

## Abilities

Characters may have named abilities which are described below:

* **Taunt**: When an adjacent enemy attaacks the target of that attack must be a unit with **Taunt**

