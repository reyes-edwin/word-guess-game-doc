---
title: Check-in week 4
description: Project progress for week 4
date: 2022-04-10
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---

Project update for week 4 found below.

## Frontend
Frontend group finished the keyboard and 6 * 5 grid board. We were able to successfully put them in the center and make it auto adjusted with the website page. We build colors for wrong, wrong location and correct for both and will start working on title and user interaction. We had a copy of script.js from other wordle game and hope we can learn something from it.

## Backend 

Edwin- For this week I created the input buttons and attempted to change the focus once each character. [view project](https://word-guessing-game-seven.vercel.app/)

**Questions**
- How can I change the focus on each character?
- How can the user submit it's guess once all 5 squares are filled?
- Do we need to implement the keywords UI based on the time we got left?

Aaron- Based on feedback from Bryan, I was looking into how we would use word-game-board in order to check how the user is doing on their current guess compared to the correct word. Still not sure how exactly we are going to do that.

Also looked at some other wordle clones in order to see how they were tracking different things and figure out more about what the correct direction was in order to get our world clone up and working.

## API
The API team focused this week on starting the Swagger/OpenAPI spec document for the project. Working off the demo PetStore example in the Swagger Editor and the OpenAPI specification guide, we were able to complete the documentation for the getWord API. This entry contains the request body, responses, and is connected to the word-guess-game Vercel application. It is able to make requests and display the responses. The file was exported as a YAML file and is stored in the [/documentation folder](https://github.com/jforcina20/word-guessing-game/tree/main/documentation) of the word-guess-game repo. 
