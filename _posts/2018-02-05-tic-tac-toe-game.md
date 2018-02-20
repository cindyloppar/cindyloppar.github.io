---
Layout:
Title: "Tic-Tac-Toe Game"
Date: 2018-02-05 14:55
Categories:
---

# Tic-Tac-Toe Game

I had to fulfill the following user story so that I complete the project  
User Story: I can play a game of Tic Tac Toe with the computer.
User Story: My game will reset as soon as it's over so I can play again.
User Story: I can choose whether I want to play as X or O.

## How I solved the Problem

 In the script tag, I declared two variable with an empty string, an array of all the id blocks.
 A function named falsy which is declered and what the function does is to check the value agaisnt the id.
 It's the XButton and OButton functions which a player is allowed to choose between X and O character to play with and alerts the player what they have choose.

function XButton() {
            player = "X";
            secondPlayer = "O";
            alert("You chose to play as X");
        }

        function OButton() {
            player = "O";
            secondPlayer = "X";
            alert("You chose to play as O");
        }

Two functions of the first player and the second player, which will let the player know if they are choosing to play as a one player or two players.

 function onePlayer() {
            playchoice = "one-player";
            alert("You want to play as one play");
        }

        function twoPlayer() {
            playchoice = "two-player";
            alert("You want to play as two player");
        }

A function for all the button one, under the function on the first line I declared a variable named random and used Math.floor and Math.random to pick any id from the array I declared outside as the global scope and check the length.
On the second line of each an every function button then the falsy function comes in and checks between the value and the computer. 
We now get the value of the player id.

  
## Conclusion



