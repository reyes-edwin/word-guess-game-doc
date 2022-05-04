---
title: Word Guessing Game Documentation
description: Project documentation for final submission
date: 2022-05-03
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---
# Word Guessing Game Documentation

## What is it?
This game is a clone of the popular game Wordle built with web components. It plays the same as the traditional game: the user gets six attempts to guess a five letter word. There is one word for every day. 

After each guess, the tiles of each letter of their guess will change color to indicate if they are correct. Green tiles mean the letter is correct and in the correct position, yellow tiles mean the letter is in the word but the user has put it in the incorrect position, and grey tiles mean the letter is not in the word. 

After guessing correctly, or running out of guesses, the game ends. The user will have the option to request a new randomly generated word to play again. 

## How does it work?
The app is hosted in Vercel. Upon launch, the game calls the getWord API endpoint to get the current word of the day. The call is formatted as `/api/getWord?myDay=YYYY-MM-DD` and returns a JSON response. Full documentation for this API endpoint is available on Stoplight [here](https://402-groupc.stoplight.io/docs/word-guessing-game). 

After the word has been retrieved, the WordGuessingGame.js file sends the word to the wordGameBoard.js file via the `<word-game-board>` tag. wordGameBoard.js is used to check the user's input into each tile and check if it belongs in the current word. Based on the input in each tile, the wordGameBoard file will use wordTile.js to render the recolored tiles. A status is sent for each tile, correct = green, partial = yellow, and incorrect = grey. 

The user has 6 attempts to guess the word. If they guess the correct word, confetti will appear on their screen. After this, the game sends the number of attempts and winners for the word. If they do not guess the correct word, they will be shown a pop-up telling them they ran out of guesses and what the correct word was. This alert will also show the number of attempts and correct guesses for that word by pulling from the database. 

## How was it built? ##
Read about the process for building this component through the previous weekly check-in posts on this blog [here] (https://reyes-edwin.github.io/word-guess-game-doc/posts/). 