---
layout: default
title: Number Guessing Game
permalink: /numberguessing/
---

# Number Guessing Game

![playing1](https://user-images.githubusercontent.com/55026784/163063342-cb4f429f-1daf-4e08-b3aa-20d47fa20c68.png)

## Gameplay

Player guesses numbers between 1 and 100, and is prompted to enter lower or higher numbers until the correct number is guessed. The scoring is based on the number of incorrect guesses the user entered before winning.

![playing2](https://user-images.githubusercontent.com/55026784/163062579-dd128970-0da2-4f7a-a3dc-015f727900b8.png)

### Scoring

Once the user guesses the correct number and the game is over, their score is stored in a database. 

A page displaying the top 10 scores for the game is shown upon game completion, and the player can choose to play again by clicking 'New Game'. If the user scored among the top 10, their name is highlighted when this page is displayed.

![playing3](https://user-images.githubusercontent.com/55026784/163063804-595246bc-bf06-43c0-b44c-1995b0102d2d.png)

### Logic

Coded in PHP, this game uses random number generation to generate a target guess.

`  $_SESSION["target"] = rand(1, 100);`

Gameplay validation functionality is achieved through the use of session variables, and storing and referencing those values in a table in a MySQL database over a remote connection.
```
  $sql = "INSERT INTO Games (player, target, score) 
          VALUES ('" . $_SESSION["username"] . "', '" 
                     . $_SESSION["target"] . "', '" 
                     . $_SESSION["score"] . "')";
  $sqlquery = $conn->query($sql);
```
...
```
if($_SESSION["target"] > $_SESSION["guess"]) {
  // higher

  $_SESSION["prompt"] = "Higher";
} else if($_SESSION["target"] < $_SESSION["guess"]) {
  // lower

  $_SESSION["prompt"] = "Lower";
}
```
<h2 align="center">
  <a href="https://jaywatersspr22.epizy.com/">Try it out!</a>
</h2>
