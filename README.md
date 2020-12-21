# Dobble Game using Python

A Dobble game was created using object oriented concepts in Python. Dobble is a fast-paced matching game that's fun for all the family. It works by finding same symbols for 2 cards. This game can be played between 2 teams. Appropriate validation checks were also added here.

Description:

1. This program has 2 classes: DobbleDeck and DobbleCard.
2. This program also has method viz. start_dobble_game().

## DobbleDeck class

This class contains a constructor which creates a deck of cards, checks it's validity and starts the game by prompting an input from the user only if the deck is valid. DobbleDeck class has an instance variable called deck which contains all the cards as DobbleCard instances.

This class has thirteen methods:

1. add_card() - This method adds a card into the deck.
2. remove_card() - This method removes the last used card while playing the game. For example, between card 1 and card 2, card 1 will be removed and card 2 will be used for the next round.
3. play_card() - This method prints out card for every round.
4. choose_cards() - This methods chooses two cards at random from the deck, checks their validity by calling validate_cards() method and returns the emoji id list.
5. validate_cards() - This method checks the validity of two cards i.e. two cards chosen at random should never be same and these random cards should not be the same as used in the previous rounds.
6. create_deck() - This method is used to create deck of 57 cards.
7. check_validity() - This method checks if deck is valid or not by comparing cards using linear search. It has kwargs as method argument. Due to this, it can work in two ways. If verbose is equal to True, then it prints out all the sets which are getting compared. If verbose is equal to False, then it does not prints any of the sets.
8. generate_emojis() - This method creates a dictionary containing key as integer id and value as emoji.
9. get_input() - This method prompts the user for the total number of rounds to play.
10. is_rounds_input_valid() - This method checks if total rounds input from user is valid or not. It is internally called by get_input() method.
11. start_game() - This method starts the game based on total rounds to be played.
12. get_winner_input() - This method prompts the user to choose a winner between A and B and increments the score accordingly.
13. is_winner_input_valid() - This method checks if winner input is valid or not. It is internally called by get_winner_input() method.


## DobbleCard class
This class contains a constructor which when invoked, creates an instance variable called card. Variable card is a dictionary consisting of card_no as key and value containing emoji ids. The instance of this class is created in the add_card() method of the DobbleDeck class.

## start_dobble_game() method
This method starts the execution of the program. It creates an instance of DobbleDeck class by calling the constructor.