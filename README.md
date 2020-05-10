# DrawPy
Hello and welcome to DrawPy!
This is a simple graphics package for python based on pygame, so you need pygame to run this.
This package is meant for graphics and basic games and GUI's.
Here is a little example to get you started. For more, run example_drawing() or example_animation():
    
    from DrawPy import *


    def main():
        screen = Window((500, 500), "MyWindow")  # Creates the window
        screen.circle(BLACK, [250, 250], 250, 0)  # Draws a circle centered at (250, 250) with a radius of 250
        draw()  # Flips the drawings on to the screen
        done()  # Waits to close the window


    main()
-----------------------------------------------------------
run the help() function for more help
Please Enjoy!
