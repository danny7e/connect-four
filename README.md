# Connect 4 Planning

## Analyze the app's functionality

As a user, I want a feature, because of a reason

MVP
    what is the least amount of work i need to do to release this item


As a user....
- I want there to be 2 players
- I want to be able to take turns
- I want to alternate dropping colored discs into one of seven columns 
- I want to be able to win if I get four in a row: horizontally, vertically, diagnolly
- I want to know who won or if it was a tie
- I want to be able to play again after the game is done

if i have time, these would be great

Bonus
- who goes first
- i want to keep track of how many time i won or lost (scoreboard)
- i want to know how many moves it took to win
- a forfeit button
- a timer on the game
- color of disc


## Think about the overall design (look & feel) of the app

- minimalistic
- purple and orange for discs
- font raleway
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Raleway:wght@200&display=swap" rel="stylesheet">
```

```css
font-family: 'Raleway', sans-serif;
```


## Wireframe and the UI

- High Fidelity
    - Working Demo (almost)
    - Button are clickable 
    - hover effects happen on those button
    - tech demo than a drawing
- Low fidelity
    - drawing of the app
    - layout of the page (pages)
    - where is the header going
    - Where are my messages to the user going
    - Where are my button going
    - does thie feel too crowded? does this feel too empty?


## Pseudocode

1) Define required constants
    1) color constant - hold the values of my disc

2) Define required variables used to track the state of the game
    1) game board - 1 array with 7 nested arrays
    2) turn - 1|| -1
    3) winner var - null || 1 || -1 || 'T'

3) Cache DOM elements
 1) Message place
 2) play again button
 3) Game Board\
 4) Column buttons/ markers


4) Upon loading the app should:
  4.1) Initialize the state variables
        - create 7 nested arrays
        - turn var should be set to 1 (player 1 turn)
        - Winner war should be null

  4.2) Render those values to the page
        - render the board, should only render white circles, no players have gone yet
        - render the message "PURPLE'S Turn"
        - render the play again button,BUT should not be visible on the first load.
  4.3) Wait for the user to interact
    
5) Handle a player clicking a column button
    1) update the board with player move
    2) update the turn variable
    3) check for a winner
    4) Re-render the board with the player move


6) Handle a player clicking the replay button
    1) reset the state vars
    2) Redner the board

7) Check for a winer
    1) check for 4 in a row
    2) offets vertical win I dont want to move the column 0, I want to move down my rows -1


## Identify the applications state

- Gameboard - 1 Array woth 7 nested arrays

```js
let board
```
- turn variable - undefined || 1 || -1
```js
let turn
```
- winner var - null || 1 || -1 || "T"
```js
let winner
```