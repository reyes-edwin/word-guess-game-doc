---
title: Check-in week 3
description: Project progress for week 3
date: 2022-04-03
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---

Project update for week 3 found below.

## Frontend

**HTML**

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="app.css" type="text/css" />
    <title>Wordle</title>
  </head>
  <body>
    <div id="root"></div>
    <script src="index.js"></script>
  </body>
</html>
```

**CSS**

```css
body {
  min-height: 100vh;
  background-color: aliceblue;
  margin: 0;
  padding: 0;
}

.header {
  background-color: antiquewhite;
  padding: 5px 30px;
  font-size: 16px;
}
```

## Backend

**Getting A Random Word**

Once the user guesses the Word of the Day a new random word would generate. This could happen on a submit function where the random word overrides the current word. 

```js
 var wordList = await fetch(url).then(res => res.json());
  // filter array to just 5 letter words
  wordList = wordList.filter(item => item.length === 5);

  // Random number between 0 - 8785
  let nums = Math.floor(Math.random() * 8786);

  let randomWord = wordList[nums];
```

Tried to make a "random word" button so that the player could press the button and the correct answer to the game would be a random word from the word-api instead of the daily word. Was able to make the button but every time I tried to pass a function through that would switch the "correct word," it never worked.

**Question:**
- How to correctly wire up some of those back-end elements like correct word to the front-end?
- How can the frontend js get the WOD from the '/api/getWord' directory? 
- Does all the JS have to be done with a lit template? 

## API
The API group began documenting back end endpoints during this work week. Documented the purpose, inputs, and outputs of the getWord.js file. View the documentation [here](https://github.com/jforcina20/word-guessing-game/tree/main/documentation). As more endpoints are documented, they will also be viewable at this link.

Started reading about OpenAPI 3.0 documents and reviewed the HAXcms example. This upcomming week we plan on learning more about the API documentation and begin finalizing and documenting the reamining endpoints.
```
