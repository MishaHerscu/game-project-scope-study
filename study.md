# Game Project Scope Study

## Required Readings

-   [Game Project](https://github.com/ga-wdi-boston/game-project)
-   [Game API](https://github.com/ga-wdi-boston/game-project-api)
-   [What is a User Story](http://searchsoftwarequality.techtarget.com/definition/user-story)

## Deliverables

After reading the `game-project` prompt and the `game-project-api` documentation
please do the following and be prepared to share and discuss during our next
class.

Submit detailed answers to these in this file via a pull request.

-   A wireframe of what your game project will look like.

[Wireframe File](https://github.com/MishaHerscu/game-project-scope-study/blob/response/TicTacToeWireframe.bmpr)

-   The data structure you plan to use.

I plan to have data structures in a "model" file that mirror the structure of
the API output i.e. the current game will look like this:

{
  "id": 1,
  "cells": ["o","x","o","x","o","x","o","x","o"],
  "over": true,
  "player_x": {
    "id": 1,
    "email": "and@and.com"
  },
  "player_o": {
    "id": 3,
    "email": "dna@dna.com"
  }
}

The "View" i.e. the DOM elements will be updated based on changes to this model.

-   How you will take the markup of the game board and represent it in JS

I will make a table and have an id for every cell that corresponds to the
array of cells in the game object. Then I can easily change the .text() of
the cells using jQuery.

-   How you plan to approach this project.

First, I am going to try to get a dummy website to look at using HTML
and some CSS, though I really won't spend much time making it pretty yet.

Then I'll try to get it so that I can interact with the board.

I will also be trying to get the AJAX to work with the back end API.

Then I'll try to put together the two sides and have the AJAX calls change
the model, and finally have the model change the DOM.

-   4-8 user stories for your game project.

This is the rubric for the user stories:
As a <role>, I want <feature> so that <reason>.

My stories:
1. As a first user, I want to be able to create an account, login, and start a game, so
that I can play with friends.
2. As another user I want to be able to sign in and join a game so that I can
play against a friend.
3. As someone playing a game, I want the board to prevent me from selecting
a place where someone already went so that the game adheres to the rules.
4. As a user, I want to be able to play someone over the web, so that I can
play someone remotely.

-   How you plan to keep your code modular.

I am going to try to have strict separation of concerns. I think I will have:
- an html file for showing the website
- a css or scss file for styles
- a index.js file for some scripts to run when the page loads
- an events.js file to add event handlers and those functions
- an api.js file for ajax calls
- a ui.js file for interface changes
- a gameLogic.js file for running the game
- a gameModel.js file for storing the actual state of the current game

-   What creative spin will you add to your project.

I don't want to think too much about this until I have the basic functionality
working. That said, I think letting people choose their own markers would be
cool.

-   How you will use version control to backup / track your project.

I am just going to commit every change I make seperately so that I never run
the risk of having multiple changes that interact and make debugging a
nightmare.

-   Do you plan to attempt any of the bonuses.

Yes, I'll probably try to make it so people can play over the web. I may also
try to make an arbitrarily large board as an option. However, I really want to
focus on getting the basics to work first before I think too much about this.
