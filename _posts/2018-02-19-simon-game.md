---
Layout:
Title:
Date:
Gategories:
---

# Simon Game

I was given a project to fulfill the following user stories for the simon game:

 I am presented with a random series of button presses.
 Each time I input a series of button presses correctly, I see the same series of button presses but with an additional step.
 I hear a sound that corresponds to each button both when the series of button presses plays, and when I personally press a button.
 If I press the wrong button, I am notified that I have done so, and that series of button presses starts again to remind me of the pattern so I can try again.
 I can see how many steps are in the current series of button presses.
 If I want to restart, I can hit a button to do so, and the game will return to a single step.
 I can play in strict mode where if I get a button press wrong, it notifies me that I have done so, and the game restarts at a new random series of button presses.
 I can win the game by getting a series of 20 steps correct. I am notified of my victory, then the game starts over.
Hint: Here are mp3s you can use for each button: 
https://s3.amazonaws.com/freecodecamp/simonSound1.mp3, 
https://s3.amazonaws.com/freecodecamp/simonSound2.mp3, 
https://s3.amazonaws.com/freecodecamp/simonSound3.mp3, 
https://s3.amazonaws.com/freecodecamp/simonSound4.mp3.

## How i solved the problem.

I assigned currentGame and player to empty array. When the game begins there is an empty array to push colors which are supposed to be in that empty array.

I assigned possible colors which are the ones to flash when there is a next level.

I assigned an object of sounds and lastly I assigned strict to be false.  

The first function is the fucntion which display colors in the array I declared as my global scope. The first line in the function I assinged a variable which will randomly choose colors without any order and multiplied it by any possible color in the array of colors I created globally.
On the second line I pushed the possible random colors into currentGame(the empty array which is globally declared).
On the third line I said document dot get element by id which was count inside html and should be equal to current game dot length.
Lastly I called the second function so that after the first three lines are executed it can also be executed.

function startGame() {

    var randomColor = Math.floor(Math.random() * possibilities.length);
    currentGame.push(possibilities[randomColor]);
    document.getElementById("count").innerHTML = currentGame.length;

    showMoves()

  }

  The second function flashes the colors after the colors where displayed in the first function. In the showMoves function I had a setInterval function the first line will flash out the color which was displayed first in the current game which will flash out as the background.
  A had another function which is setTimeout function, the function turns back the box into its original color, in half a second.
  therefore I appended the starting point which was n assinged to zero. An if statement which will compare and check if n is strcikly equal to current game dot length the color should countinue to next level and flash out from the from the begin to the last index in one and half second then clears the interval.

 function showMoves() {

    const showTileFor = 1000;
    var n = 0;
    var displayColors = setInterval(function () {
      document.getElementById('btn_' + currentGame[n]).style.background = currentGame[n];

      setTimeout(function () {
        document.getElementById('btn_' + currentGame[n - 1]).style.background = "white";

      }, 500);
      n++;
      if (n === currentGame.length) {
        clearInterval(displayColors);
      }

    }, showTileFor * 1.1);

  }

  On the third function it was for player. I compared if the length of the player and the current game is the same and again I compared if the strings are of the same length.
  If strict is on and the player clicks the wrong color combination, it should alert the player and there start from the begining. An else statement if a player clicked wrong color combination it should alert the player that wrong move and should flash back the color combination the player got wrong and move one the the next level after the player got the right color combination.
  An if statement alerting the player that they won if they get count is equal to 20 else to alert the player to the next level as the player gets the right color combination.

  function players(id) {
    player.push(id);
    if (currentGame.length === player.length) {
      if (currentGame.toString() !== player.toString()) {
        if (strict) {
          alert('Try again! ...From scratch!');
          currentGame = [];
          player = [];
          startGame();
        } else {
          alert('Wrong move! Try again!');
          player = []
          showMoves();
        }
      } else {
        console.log('Good Move!');
        startGame();
        player = [];
          if (count == 20) {
            alert('You won! Congrats.');
          } else {
            alert('Next round!');
          }    
      }
    }
  }

  Conclusion

  Lastly I have a function which works for the restart button and the moment the player clicks on that button the page reloads.

   function newGame() {
    window.location.reload();
  }