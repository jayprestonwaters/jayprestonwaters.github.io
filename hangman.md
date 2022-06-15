---
layout: default
title: Hangman Game
permalink: /hangman/
---

# Hangman Game
![playing1](https://user-images.githubusercontent.com/55026784/163106022-9f8f92a0-19a0-4e47-a5e7-72959a573eab.png)

## Gameplay

Player guesses letters, and is prompted if the letter is correct or incorrect. The game is over when the player guesses all the letters in the word, or when all body parts of the Hangman have been drawn.

![playing2](https://user-images.githubusercontent.com/55026784/163106222-3d6f27d7-18ff-4d9f-8cba-d22b31829123.png)

## Scoring

Scores are based on the amount of letters correctly guessed before losing, and the size of the word. If all letters are correctly guessed, the game counts as a win.

## Logic

The game is played asynchronously, without the need to refresh the page between guesses. It uses websockets with Razor pages, and makes use of click events for gameplay functionality.

```
sendButton.onclick = function () {
    if (!socket || socket.readyState !== WebSocket.OPEN) {
        alert("socket not connected");
    }
    var data = sendMessage.value;
```
...

<h2 align="center">
  <a href="https://github.com/jayprestonwaters/CS3750_Projects">Download the code!</a>
</h2>

<h3 align="center">
    <a href="https://jayprestonwaters.github.io/">Home</a>
</h3>
