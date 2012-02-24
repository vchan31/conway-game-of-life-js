Conway's Game of Life in Javascript/Canvas
==========================================

How to Run
----------

**See `examples` folder for some demoes of how to run.**

Create new GameOfLife object, and pass it the grid size, cell size, 
a canvas ID, and an array containing the starting cells:

    var game = new GameOfLife(grid_width, grid_height, cell_width, cell_height, "life");

Here's a sample with parameters:

    // Must be same size as game dimensions 
    //  (10 x 10 in this case)
    var starting_cells = [
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0],
      [0,0,0,0,0,0,0,0,0,0]
    ],
    params = {
      canvas_id:    "life",
      grid_width:   100,
      grid_height:  100,
      cell_width:   10,
      cell_height:  10,
      init_cells:   starting_cells
    },
    game = new GameOfLife(params);


Advance the game to the next step:

    game.step();


To run this as an animation, just set an interval to call game.step(). In this
example, it will update every second, but you can modify it to use any millisecond value:

    var interval = setInterval(game.step, 1000);

You can stop the animation by calling clearInterval:

    clearInterval(interval);
