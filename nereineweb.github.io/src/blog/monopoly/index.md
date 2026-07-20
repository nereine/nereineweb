# A Python-Based Monopoly Game

## Project Overview

This project presents a simplified, text-based implementation of the Monopoly board game using Python. It was developed as an educational programming exercise to demonstrate how fundamental concepts in software development can be applied to the design of a turn-based game.

The program allows multiple players to roll dice, move around a virtual board, purchase properties, pay rent, receive rewards, pay taxes, and remain in the game until only one financially solvent player remains. Although the implementation does not reproduce every rule of the original board game, it provides a functional foundation that can be extended in future development.

## Project Objectives

The principal objectives of this project are:

1. To apply object-oriented programming principles in a practical context.
2. To represent players, properties, and game rules through appropriate data structures.
3. To develop a turn-based system controlled by conditional statements and loops.
4. To incorporate random events through dice rolls and special board spaces.
5. To produce readable, modular, and maintainable Python code.

## System Design

The program is organised around three principal classes:

### `Property`

The `Property` class represents a purchasable space on the board. Each property contains:

- A property name
- A purchase price
- A rental value
- An owner, if the property has been purchased

### `Player`

The `Player` class stores and manages information relating to each participant, including:

- Player name
- Current cash balance
- Position on the board
- List of owned properties
- Dice-rolling and movement behaviour

### `MonopolyGame`

The `MonopolyGame` class controls the overall operation of the game. Its responsibilities include:

- Creating the board and players
- Managing the order of play
- Processing property purchases and rental payments
- Applying the effects of special spaces
- Identifying bankrupt players
- Determining the winner

This structure separates the main areas of responsibility and makes the program easier to understand, test, and expand.

## Key Features

- Support for multiple players
- Randomised two-dice movement
- Financial rewards for passing `GO`
- Property purchasing and ownership
- Rental payments between players
- Chance and Community Chest events
- Income tax payments
- Bankruptcy detection
- Automatic identification of the final winner

## Technical Requirements

The project requires:

- Python 3.11 or later
- A command-line terminal
- No third-party Python packages

The game uses only modules included in the Python Standard Library.

## Installation and Execution

Clone the repository:

```bash
git clone https://github.com/nereine/python-monopoly-game.git
```

Enter the project directory:

```bash
cd python-monopoly-game
```

Run the program:

```bash
python3 monopoly.py
```

When prompted, enter the number of players and each player's name. Players then take turns by pressing Enter to roll the dice and responding to property-purchase questions.

## Program Logic

During each turn, the active player rolls two six-sided dice. The resulting value determines how many spaces the player moves. The program then identifies the space and applies the relevant rule.

If the player lands on an unowned property, the program offers the option to purchase it. If another player owns the property, rent is transferred from the active player to its owner. Special spaces may produce rewards, penalties, or informational outcomes. A player whose cash balance reaches zero is declared bankrupt and removed from the game. The process continues until one player remains.

## Limitations

The current version is intentionally simplified and does not yet include:

- The complete official board
- Property colour groups
- Houses and hotels
- Property auctions
- Mortgages and property trading
- Complete jail rules
- Extra turns for rolling doubles
- Official Chance and Community Chest cards
- Graphical or online multiplayer functionality

These limitations define potential areas for future development rather than defects in the current educational implementation.

## Future Development

Possible extensions include:

1. Developing a graphical interface with Pygame.
2. Implementing the complete board and more detailed rules.
3. Introducing computer-controlled players.
4. Adding save and load functionality.
5. Creating automated unit tests.
6. Supporting local-network or online multiplayer games.
7. Recording game statistics for later analysis.

## Conclusion

This project demonstrates how Python can be used to model a rule-based system through classes, collections, loops, conditional logic, and random-number generation. The resulting application is a playable text-based game and a foundation for more advanced software development. Its modular structure also allows additional rules and interface features to be introduced progressively.

## Disclaimer

This is an independent, non-commercial educational project inspired by the general mechanics of a property-trading board game. It is not affiliated with, authorised by, or endorsed by Hasbro. Monopoly and its associated names and elements are trademarks of their respective owners.

## Author

**GitHub:** [@nereine](https://github.com/nereine)