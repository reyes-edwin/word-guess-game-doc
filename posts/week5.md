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

## Backend 

Aaron
Looked into the user input and figuring out more about how to verify the guess once the user types it in to the game board. Not sure how to lock the user's input to one row of the game board instead of being able to just click on random blocks within the game board and inputting at random spots. Also wanted to figure out how to delete the letters just by hitting the delete key rather than having to click on a tile and deleting it that way. Would be nice to have the game function as close to actual wordle with basic functions like that.

## API
Started using Stoplight.io to make the OpenAPI document for the getWord endpoint. Built the schema for Word responses and connected the document to the live vercel server to send requests and recieve responses. The UI element of building this document has made the process easier and allowed us to add more information than the one built with Swagger Editor. 

View the Stoplight documentation [here](https://402-groupc.stoplight.io/docs/word-guessing-game/YXBpOjUyODc4MzI1-word-guessing-game-api). 

The original file built with Swagger editor can be viewed [here](https://github.com/reyes-edwin/word-guessing-game/blob/main/documentation/openapi.yaml).
