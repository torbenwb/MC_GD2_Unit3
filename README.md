# MC_GD2_Unit3

This is the Unit Project from GD2 Unit 3. In this unit students learn how to work with Scriptable Objects to create a collectible card game.

## Installation

To install this project, clone the repository to your local machine and open using Unity HUB. This project was built using Unity version 2021.3.16f1.

## Usage Instructions

This project is designed for education purposes. While building this project students learn how to use scriptable objects to store content data and to create an event system. Students also learn how to design and implement simplified card game mechanics, as well as some basic custom editor scripting.

The instruction sequence for this project is as follows:

* Scriptable Objects - covers using scriptable objects as content containers, and game board layout and interactions.
* Card Game Player - covers the design and implementation of the `Player` class, capable of drawing, discarding, and playing cards.
* Card Game Enemy - covers the design and implementation of the `Enemy` and `Creature` classes.
* Card Effects - covers the implementation of distinct card effects as well as game state management systems.

### Scriptable Objects

This project makes use of several different types of scriptable objects.

* `Card_SO`: represents a unique type of card and contains card data including name, description, cost, image, and effects.
* `Creature_SO`: represents a unique creature type. Contains creature's attack strength, health, and image.
* `Deck_SO`: represents a deck of cards. Cards are represented by the nested `CardType` class which contains a unique card type (`Card_SO`) and the quantity of that card type.
* `GameEvent`: represents a reusable game event. Notifies encapsulated `GameEventListener` when event is raised.

### Board and Board Items

The `Board` and `BoardItem` scripts implement control over the layout of items on the board. These items may be anything but in this project board items are used to represent the cards in the player's hand and the enemy's creatures on the board.

### Creature and Card

The `Creature` and `Card` scripts derive from `BoardItem` and are used to represent an instance of `Creature_SO` add `Card_SO` respectively.

### Player and Player Controller 

* `Player` implements the core card game abilities of a player: draw, discard, and play card.
* `PlayerController` parses user input and passes commands to `Player`.

### Enemy

The `Enemy` class implements a simple computer controlled player which manages multiple creatures.


