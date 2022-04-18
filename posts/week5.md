---
title: Check-in week 5
description: Project progress for week 5
date: 2022-04-17
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---

Project update for week 5 found below.

## Frontend
Finished up the front end astetic of the site (grid and keyboard and title), and worked on splitting up the the word and comparing to the correct word. still easing off of the template we found but making progress on the on screen keyboard working to mkae sure the color changes after a letter is submitted and compared.

## Backend 

**Edwin**
[view project](https://word-guessing-game-seven.vercel.app/)

- Color updates on each character. Sometimes for duplicated characters the background color is black. Try it out with the word "Zaxes". I'm not quite sure why this is happening. 

- Pulled all the words length of 5 and checked if the list contains the submitted guess word. One thing is how can we do this without generating all the words in the tag? (inspect the element to see). Can we hide this? 
```js
if (!this.allWords.includes(theGuess.toLowerCase())) {
      window.alert('word not in list');
      return;
    }
```

- Started the handles delete function. Every time the user press delete button the character deletes and moves back to the previous
sibling. 

**Next Steps**
1. delete input
2. handle error after 6 attempts
3. Play again button after the game is over
4. restart button

Aaron
Looked into the user input and figuring out more about how to verify the guess once the user types it in to the game board. Not sure how to lock the user's input to one row of the game board instead of being able to just click on random blocks within the game board and inputting at random spots. Also wanted to figure out how to delete the letters just by hitting the delete key rather than having to click on a tile and deleting it that way. Would be nice to have the game function as close to actual wordle with basic functions like that.

## API
Started using Stoplight.io to make the OpenAPI document for the getWord endpoint. Built the schema for Word responses and connected the document to the live vercel server to send requests and recieve responses. The UI element of building this document has made the process easier and allowed us to add more information than the one built with Swagger Editor. 

View the Stoplight documentation [here](https://402-groupc.stoplight.io/docs/word-guessing-game/YXBpOjUyODc4MzI1-word-guessing-game-api). 

The original file built with Swagger editor can be viewed [here](https://github.com/reyes-edwin/word-guessing-game/blob/main/documentation/openapi.yaml).
