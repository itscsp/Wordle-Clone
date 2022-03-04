# Functional Requirements

## GamePlay

6 tries to guess a 5-letter word from

### Pick a Solution word
    x store solution word in "word" variable
    x when game is loaded, word variable assign by solution word
    x this solution word is get from words.txt file


### Making a guess

Detect keypress

 - if keypress is a letter
  x update "letters" attribute
    x update tile markup based on "letters" value

- if keypress is backspace key
    - delete last letter in "letters"
        - update tile markup based on "letters"

x Don't run update function if "letters" length = 4

### Submit guess

    x Pressing Enter will submit guess

    x Compare each letter with the corresponding letter in solution word
    x Update the state / color of the letter
        - if all letters are "correct" / green, game is won

Store solution words in JSON object / array

>> Typing in the letter will display in the tile
>> Backspace will delete letters
>> Enter will submit guess

guess must be real word, "in word list"

Guess colors(data-state):
    - gray: "absent," letter not in word
    - yellow: "present," letter in word, but in wrong position
    - green: "correct," letter in word and in right position

Hard Mode: present or correct letters must be used in subsequent guesses

Guess are saved in Local Storage

# Design

Tiles 5x6
Virtual keyboard

## Interactions

When typing a letter:
    - border of the tile changes to light grey
    - blinking in animation with letters changes
    - backspace with remove letter, border changes back to dark grey

    when submiting guess:
        - Tiles will flip up and background color will change based on guess
        - Slight delay between eacch tile flipping
        - blackground color changes when tile is flat, i.e can't see it from



hello hi my name is c