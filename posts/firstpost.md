---
title: Word-Guessing-Game-Doc
description: This a a post on the requirements for our current project
date: 2022-03-19
tags:
  - web
  - microservice
  - webcomponent
layout: layouts/post.njk
---

## Background

For our final Project in IST402, our team decided to create a word-guessing-game. This would be a web-based word game allowing users to guess a random five-letter word. Each user would be given 5-6 attempts to guess the word. For each guess, a letter is marked as either green, yellow, or gray: Green indicates that the letter is correct, and yellow indicates that it is in the answer but not in the correct position. In contrast, gray indicates it is not in the correct position answer. [Project](https://github.com/elmsln/issues/issues/963)

## 11ty repo

You can find the repository powering this 11ty website [here](https://github.com/reyes-edwin/word-guess-game-doc).

## Notes Week 10
**Mockup**
![wordle mockup](/img/wordle.jpg)

When a guess is entered, the results will be colored either grey, orange, or green using SimpleColor

Our team currently believes that upon startup, the component will call the random word API to recieve the inital word. The user will start guessing and after entering a guess, each letter of their entry will be sent to an API endpoint noting which position it is in. The API response will state whether each letter is in the correct spot, in the incorrect spot, or not in the word at all. 