# "Hog" - Dice Game
Implementation of the game "Hog" and identifying strategies. 

To play the game with the GUI, run from the terminal: 
```
python3 hog_gui.py
```

## Rules
In Hog, two players alternate turns trying to be the first to end a turn with at least 100 total points. On each turn, the current player chooses some number of dice to roll, up to 10. That player's score for the turn is the sum of the dice outcomes. However, a player who rolls too many dice risks:

### Sow Sad. 
If any of the dice outcomes is a 1, the current player's score for the turn is 1.
In a normal game of Hog, those are all the rules. To spice up the game, we'll include some special rules:

### Piggy Points. 
A player who chooses to roll zero dice scores k + 4 points, where k is the absolute value of the tens digit minus the ones digit in the opponent's score. If the opponent's score is only one digit, assume the tens digit is 0. You may not assume that the score is under 100.

### More Boar. 
After the points for the turn are added to the current player’s score, the current player takes an extra turn if the minimum digit of the current player's score is strictly smaller than the minimum digit of the opponent's score and the maximum digit of the current player's score is strictly larger than the maximum digit of the opponent's score. You may not assume that the scores are under 100. The More Boar calculation should be done on the current player's score after the points from the current turn are added. More Boar can be activated multiple times in a row for the same player.

Source: https://cs61a.org/proj/hog/
