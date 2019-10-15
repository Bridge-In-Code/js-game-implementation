# js-game-implementation

Author: Aaron Ferris

## Overview:
This repository is for exploring creating basic card objects and their methods to play bridge.

Most of this is code challenges.

## File Structure / Pushing Standards

Origin  <= Stage <= Feature Branch

Ideally you would not commit your own pushes to Origin from stage. Hopefully this gets to that point. Exceptions are always there, so please put a note in whatever message so it gets seen.

Any open source work will be commited to stage, not to origin.

## Current Objects

### Card
  * An object representation of a playing card 
  * Has properties of a suite and number
### Hand
  * Representation of a bridge hand.
  * Organizes cards into 4 suites, in the order Clubs, Spades, Diamonds, Hearts.
  * Includes a function to count points
    * There are many methods to counting points, and many different theories to how/when to weight certain conditions
    * Basic high-card points are implemented
    * Potential for short/long suite counting.
    * May be a method in the game
  * Each Hand has a next that is by default empty
  * Each hand has a partner that is by default empty
  * Has a method to set the partner and the next
### Deck
  * Representation of a standard 52 card deck of playing cards, no jokers
  * Upon creation has 13 cards, each organized into their suites
  * Has a method to shuffle the deck
    * Utilizes a stack
    * Utilizes individual card object
### Game
  * Represents a game of bridge
    * 4 hand objects, named north, east, south, and west
