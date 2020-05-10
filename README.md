# DrawPy
Hello and welcome to DrawPy!  
This is a simple graphics package built on pygame so you need pygame to run this.   
To start using this, run the following command in a terminal with python and pip installed: 
 
    pip install DrawPy  
There are 3 basic formats to using DrawPy.
  
Format 1, for basic graphics and animations:  

    from DrawPy import *
    
    screen = Window((500, 500), "MyWindow")  # Creates the window
    screen.circle(BLACK, [250, 250], 250, 0)  # Draws a circle centered at (250, 250) with a radius of 250
    draw()  # Flips the drawings on to the screen
    done()  # Waits to close the window
Format 2, for more complex graphics and animations. Also suitable for simple games:

    from DrawPy import *
    """Animates a circle moving around a screen"""
    screen = Window(caption="Moving circle")  # Creates the window

    # Set the speed of the circle
    x_change = 5
    y_change = 5
    # Set the initial position of the circle
    x_pos = 50
    y_pos = 50

    # Main loop, used for animations and some games
    while not check_quit():  # Loop until the user closes the window
        screen.circle(BLACK, [x_pos, y_pos], 25, 0)  # Draws the circle
        x_pos += x_change  # Moves the position of the circle
        y_pos += y_change
        # Causes the circle to bounce if it touches the edge
        if x_pos >= 475:
            x_change = -1 * abs(x_change)
        if x_pos <= 25:
            x_change = abs(x_change)
        if y_pos >= 675:
            y_change = -1 * abs(y_change)
        if y_pos <= 25:
            y_change = abs(y_change)
        draw()  # Flips the circle to the screen
        frame_rate(60)  # Sets a frame rate of 60 fps
        screen.clear()  # Clears the screen
    quit()  # Quits the program
Format 3, more advanced and for event based graphics, animations, and games:

    from DrawPy import *
    # Used mainly for games or animation that handle events.
    screen = Window((500, 700), "My Window", BLUE)  # Creates the screen

    def default():  # Sets the default function
        screen.ellipse(BLACK, [0, 0, 500, 700], 1)

    def on_click():  # Sets an on click function
        screen.ellipse(BLACK, [0, 0, 500, 700], 0)

    screen.register(screen.DEFAULT, default)  # Registers the functions
    screen.register(MOUSEBUTTONDOWN, on_click)
    screen.go()  # Runs the code
For more help, run the help() function.  
## Enjoy!

