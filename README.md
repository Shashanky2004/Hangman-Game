# Hangman-Game
This Hangman API is built to intelligently guess letters in a Hangman game by leveraging n-gram probabilities. N-grams are sequences of letters, and this code uses unigrams, bigrams, trigrams, fourgrams, and fivegrams to estimate the likelihood of a letter occurring in a word of a given length.
The API is initialized with a dictionary of words, from which it constructs the n-gram models. It keeps track of guessed and incorrect letters throughout the game. When making guesses, it recalibrates its n-gram models if the last guess was incorrect and the number of remaining tries is low.

The guessing process starts with a partially revealed word, where correctly guessed letters are shown, and blanks are used for unrevealed letters. The code iteratively applies n-gram analysis to make educated letter guesses. It calculates probabilities for each letter to appear in the blanks and updates these probabilities with each guess, adjusting them based on the n-gram models.

The game continues until it's either won (all letters are correctly guessed) or lost (too many incorrect guesses). The code allows you to specify whether to use a word from the training or test dictionary and provides options for verbosity in the game.

Overall, this API demonstrates a methodical approach to Hangman by leveraging linguistic patterns in n-gram probabilities to maximize the chances of guessing the correct word within the given number of tries.
ere's a brief overview of the main methods and their functionalities in your code:

__init__: This is the constructor method. It initializes several data structures, loads the dictionary of words, builds n-grams, and sets up other game-related variables.

guess: This method takes the current state of the word (with correctly guessed letters and blanks) and returns the best guess for the next letter based on n-gram probabilities.

build_n_grams: This method builds n-gram dictionaries (unigrams, bigrams, trigrams, fourgrams, and fivegrams) from the provided dictionary of words.

recalibrate_n_grams: This method updates the n-gram dictionaries and the word dictionary to remove words containing incorrectly guessed letters.

Methods like fivegram_probs, fourgram_probs, trigram_probs, bigram_probs, and unigram_probs: These methods calculate letter probabilities for different n-gram levels and update the probabilities iteratively for the best guess.

start_game: This method initiates a game of Hangman. It allows you to specify whether to use a random word from the training or test dictionary, as well as other game settings. The game progresses with guesses based on the n-gram probabilities.

Overall, your code implements a Hangman playing strategy that adapts its guesses based on n-gram analysis. It recalibrates its n-grams when incorrect guesses are made and attempts to maximize the likelihood of guessing the word correctly. If you have any specific questions or need further assistance with this code, please let me know!
