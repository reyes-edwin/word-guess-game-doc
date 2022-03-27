---
title: Check-in week 2
description: Project progress for week 2
date: 2022-03-27
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---

Project update for week 2 found below. 

## Frontend 

## Backend
**WordGuessingGame.js**

Week 2 consisted of trying to fetch all of the words from the 'Random Word API.' Our main goal was to iterate and gather all five-letter words through the array based on the calendar date. We first attempted to use a for loop to loop through the array and then use an if-statement to log all five-letter words. This method worked, but as we generated seed values to get a position on the word, we had to create a new array and push the words into it. This approach ended up failing because, for each word, there was an array containing 8k + plus words. So imagine having 8k words containing 8k inside the array. That's a considerable number. 

A new approach was to use the array filter and filter all the words that contained five letters. 

`const greaterArr = arr.filter((item) => item.length === 5);`

**api/getWord.js**

We moved all of our frontend's js code to our backend and generated a seed value to get the word's position based on the calendar date. When our front end asks for a word of the day, our backend can find it. 

[View the current word of the day](https://word-guessing-game-seven.vercel.app/);

**Next Steps** 

The next step would be the following. 
- getting a new random word
- POST API endpoint that checks the current user guess and   returns which squares are correct
- Storing # of attempts (on any guess, store)
- Storing # of winners (on the correct solution, store)
- A parameter that returns a word of the size in question
READ get success vs. attempts data for the word in question.

**Questions for week 3**

- How would we generate a new word if the seed value corresponds to the current date? 
- How can we implement the check uses? 

## API 
**Retrieve word of the day - User Flow Diagram**
![date userflow](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ncee6258qmk12x6y00kg.png)

**Check word guesses - User Flow Diagram**
![guess userflow](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xv87d50x80k0iblqbr67.png)

**Data Structures**
getWord
```json
{
  "status": 200,
  "detail": {
    "date" : "03/27/2022",
    "wordSize" : 5,
    "wordOfDay" : "Arise",
    "numAttempts" : 1,
    "numCorrect" : 0,
  }
}
```
For this structure, we are assuming the automatic response will be the current date. For a randomized word from the past, the request should include the desired date, for example `/api/getWord?date=01/01/2020`.

checkGuess
```json
{
  "status": 200,
  "detail": {
    "date" : "03/27/2022",
    "guessOne" : "green",
    "guessTwo" : "grey",
    "guessThree" : "grey",
    "guessFour" : "grey",
    "guessFive" : "green",
  }
}
```
For this structure, we are assuming the game will send each letter individually, for example `/api/checkGuess?letterOne=a&letterTwo=w` etc. 