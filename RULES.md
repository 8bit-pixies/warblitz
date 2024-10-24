# Warband Lite Core (Warblitz)

## Object of the Game

Warband-Lite is a 2-player expandable grid-based skirmish game in which players take on the role of battling commanders. They will call forth mighty warriors, maneuver them about the battlefield, and play powerful events in an effort to destroy their opponent’s commanders.

## Component Overview

### Dice

* Multiple six sided dice.

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

Players will alternate taking turns until a player has won the game by destroying their opponent's commander. On a player's turn they must complete the following 5 phases:

1. Beginning
2. Deploy, Move & Attack

After the active player completes all phases, it becomes the opponents turn

### Phase 1: Beginning

At the beginning of their turn, the active player:
* Remove and discard all ATK, DEF, WLD, SPC tokens owned by the active player both in play and being held

Unless specified Boost tokens are not removed from play.

Next, any abilities that trigger at the beginning of a turn are resolved.

The player then rolls Nd6 and any additional draw d6 dice to determine tokens distributed for this turn. Where N is 1, 2, 3 on turns 1, 2, 3 respectively and 3 dice thereafter. The result of the dice are determined using the following table

- 1-2: Defend (DEF) token
- 3-4: Attack (ATK) token
- 5: Wildcard (WLD) token
- 6: Special (SPC) token

The DEF token prevents a would from being applied, whilst the ATK token provides an extra hit dice. The WLD token can be used as either a DEF or ATK token. The SPC token can be used as either a DEF or ATK token or consumed to replace one roll of the unit's attack with the "Special" result. Abilities activated in this way are not considered an additional effect.

The player then may choose to assign DEF or ATK tokens to the units. The player may assign tokens to only their own unit on the battlefield, they player may not assign more than one DEF and ATK token to a single unit, the player may not assign more than one SPC token to a single unit. Note during the course of a players turn, a unit may result in holding more than one token!

**Example**

A player rolls 3d6 and gets 3, 5, 6 (ATK, WLD, SPC). Assuming only their commander is on the battlefield, they may assign one of the following combinations:

* ATK, SPC
* DEF(via WLD), SPC
* ATK(via WLD), SPC
* ATK(via ATK, WLD or SPC)
* DEF(via WLD or SPC)

An INVALID assignment is if all three tokens are assigned, i.e.

* ATK, DEF(via WLD), SPC

#### Upgrades

During the beginning phase the player may choose to perform an upgrade for relics, events or units. All upgrades cost 4 tokens per an upgrade and provide the ability for the player to access elite options for the chosen upgrade path. The first upgrade also provides the player with one additional draw dice per turn. Subsequent upgrades provide the player with one additional draw dice for the next turn only. 

**Example 1: Performing their first upgrade**

On turn 3 a player has saved up one BST token and has 3 draw dice at the beginning of their turn. After drawing 3 tokens, they use the 3 tokens and the BST token to trigger an upgrade for their unit technology path. 

On the next turn they now have 4 draw dice available and the ability to deploy Elite units. 

**Example 2: Subsequent upgrades**

It is now further into the game, and the player already has the Elite unit tech path enabled. At the beginning of their turn they have 4 draw dice. After drawing 4 tokens, they decide to use the 4 tokens to upgrade their relics. 

On the next turn they now have 4 draw dice and 1 temporary draw dice availity and the ability to deploy Elite relics. 

### Phase 2a: Deployment

Deploy up to two units from your available reserves to the battlefield. To deploy a unit pay its cost by consuming a number of tokens equal to the unit's cost. Tokens consumed in this way are treated to be equivalent to 1 cost. The deployed unit is then place it on an empty space in the last three ranks of the battlefield, but not in front of an enemy. If the unit is deployed next to their commander then the unit may be adjacent to an enemy, otherwise it may not be adjacent to an enemy. Units may not move or attack on the same turn in which they are deployed.

**Example**

```
+-----+
|.|.|A|
|.|@|.|
|.|.|.|
+-----+
```

The unit `@` is deployed behind the enemy so this is a VALID deployment.

```
+-----+
|.|.|.|
|.|@|.|
|.|.|A|
+-----+
```

The unit `@` is deployed infront the enemy so this is a INVALID deployment.

```
+-----+
|.|.|.|
|.|.|.|
|.|@|A|
+-----+
```

The unit `@` is deployed adjacent the enemy so this is a INVALID deployment.

```
+-----+
|.|.|.|
|.|K|.|
|.|@|A|
+-----+
```

The unit `@` is deployed adjacent the enemy and also adjacent to their commander so this is a VALID deployment.

#### Adjacency

A card or space is adjacent to another one if they share an edge. Diagonals are not adjacent.

```
+-----+
|.|Y|.|
|Y|@|Y|
|.|Y|.|
+-----+
```

### Phase 2b: Move & Attack

Select 3 different units you control on the battlefield. These three units may:

* Move up to 2 spaces each. Units can only move into or through empty, adjacent spaces, and additionally
* Perform an attack

#### Moving

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

#### Attacking

To attack with a unit, follow these steps in order:

1. Declare a Target: Melee units (MEL) can target any adjacent card. Ranged units (RNG) can target any card up to 3 clear straight spaces away.
2. Roll: Roll a number of dice equal to the attacking unit's strength. If there is a SPC token assigned to the unit, consume the token and remove one of the unit's attack dice before rolling. Treat the removed dice to be a Special roll.
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

**Damaging and Destroying Unit**

To add damage to a unit, place damage tokens on it. A unit's life is reduced by 1 for each damage it has. If a unit's life ever reaches 0, that unit is destroyed and removed from the game. Gain 1 BST token each time a unit you control destroys an ENEMY unit.

**The Cost of Inaction**

Add 1 damage to your commander at the end of your Attack Phase if you did not target any enemy cards with an attack this turn.

### Event & Relic Cards

To play an event or relic card, pay its cost, resolve its effects, and then discard it. These cards cannot be played while a game effect is being resolved, e.g. during deployment, moving, attacking, or when resolving an event, ability or other effect.

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

Units of the same common unit class (i.e. MEL, RNG, Special) are to be the same. 

The events and relics selection are:

* 2 Epic Events
* 6 Common Events (2x three different Common Events)
* 1 Epic Relic
* 2 Common Relics (2 different relics)

## Abilities

Characters may have named abilities which are described below:

* **Taunt**: When an adjacent enemy attaacks the target of that attack must be a unit with **Taunt**

