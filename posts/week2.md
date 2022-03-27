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