Leaderboard
=====================


A Bebo component to quickly add a leaderboard into your HTML5 game. **NOTE: Leaderboard is scoped to group and app, so the leaderboard from one game won't interfere with another, and won't interfere with the same game on another group.***


Installation
-----------------------------------

**Link to source file**::

    <head>
      <script src="https://widgets.bebo.com/leaderboard.min.js"></script>
    </head>

You know have a variable Leaderboard that you can reference in your Javascript, with all the functionality built in as methods. Sorting and updating is done automatically, just use the methods below!

Leaderboard.getLeaderboard()
-----------------------------------

`Leaderboard.getLeaderboard(callback);`

Returns an array of the current leaderboard::
    
    Leaderboard.getLeaderboard(function(err,data){
      if (err){
        console.error(err);
        return;
      };
      console.log(data);
    });


Leaderboard.setScore()
-----------------------------------

`Leaderboard.setScore(integer)`

Adds the current user's score to the leaderboard. If new score is lower than saved score, the higher score will be preserved::

    Leaderboard.setScore(5)

Leaderboard.getHighScore()
-----------------------------------

`Leaderboard.getHighScore(callback)`

Returns the highest score set on the server, regardless of user::

    Leaderboard.getHighScore(function(err,data){
      if (err){
        console.error(err);
        return;
      };
      console.log(data);
    });

Leaderboard.getPersonalScore()
-----------------------------------

`Leaderboard.getPersonalScore(callback)`

Returns **your** personal highscore::
    
    Leaderboard.getPersonalScore(function(err,data){
      if (err){
        console.error(err);
        return;
      };
      console.log(data);
    });

Leaderboard.getLeaderboard()
-----------------------------------

`Leaderboard.getLeaderboard(callback)`

Returns an array with all the leaderboard entries::

    Leaderboard.getLeaderboard(function(err,data){
      if (err){
        console.error(err);
        return;
      };
      console.log(data);
    });


Leaderboard.setOnHighscore()
-----------------------------------

`Leaderboard.setOnHighscore(function)`

Sets a function to be executed every time a new highscore is set::

    function newHighscore(entry){
      console.log("New highscore set!",entry.score);
    };

    Leaderboard.setOnHighscore(newHighscore);

Leaderboard.setOnScore()
-----------------------------------

`Leaderboard.setOnScore(function)`

Sets a function to be executed every time a new score is set::

    function newScore(entry){
      console.log("New score set!",entry.score);
    };

    Leaderboard.setOnScore(newScore);


Feedback
------------

Got an idea on how to improve it or questions? Email johnny.dallas@bebo.com!