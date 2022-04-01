# Hangman.js
A versatile package to do all things hangman.

Installation: ```npm i hangman-gamejs```

**Usage:**
- Command line example:
  ```
const Hangman = require("hangman-gamejs")
const game = new Hangman();
while(game.state === "PLAYING"){
  console.log(game.wordProgress)
  game.guess(prompt("Guess"))
}
console.log("GAME " + game.state + "!")
  ```
- It can also be used in other cases, such as discord bots!

**Classes:**
There is only one class, which is the default export!

*HangmanGame:*

Attributes:
- Settings: A JSON of data

**Settings:**
- lives: (integer) Amount of tries a user has until they use, set to 26 for no way to lose.
- state: (string) State of the game, one of "PLAYING", "WON", "LOST" (Reccomended not to change this)
- chosenWord: (string) The word the user has to guess, can be changed when making new game to force set the word
- guessed: (array) List of guessed letters or words (Reccomended not to change this)
- wordProgress: (string) The word progress the user has made, including blanks as _ (Reccomended not to change this)
- wordList: (JSON) JSON of data to determine where to pull words from

Wordlist
- customWords: (array or false) List of your own words to add to the hangman list
- dictionaryWords: (boolean) List of every word in the dictionary

(Note: The game will pull a random word out of all of the types, so it is reccomended not to put words that exist when the dictionary option is enabled)
