![gameDemo](https://github.com/user-attachments/assets/d6e53703-74c1-4992-8224-7bbebb443950)

'''
Resources used: 

Adding music
https://pythonprogramming.net/adding-sounds-music-pygame/

Multiline comments
https://stackoverflow.com/questions/7696924/how-do-i-create-multiline-comments-in-python

Adding text to the screen
https://stackoverflow.com/questions/20842801/how-to-display-text-in-pygame

[1]
I started by importing pygame as pg and then imported
exit from the sys library.

[2]
Next, I initialized pygame, display, and font. Later, I 
inititialized the mixer as well.

[3]
After that, I created a screen using the 
pygame.set_mode() function and plugged in 
two constants for the Width and Height.
Then, I set a caption with the pygame.set_caption() function

[4]
I set three variables: 
1. run, for the game loop
2. clock, for the tick rate later on
3. FPS, to use in the clock object later on

[5]
I started the main game loop and set an 
event-handler to check for the user clicking 
the exit button and telling the program to exit
if that button is pressed.

[6]
Created a constant rgb variable for the 
background color

[7]
Filled the screen with the background color, 
updated the display, and then I plugged in the 
FPS into the clock object to set the game to 
60 frames per second

[8]
Loaded in my song and stored it into a CONSTANT
called SONG

*Issue: couldn't load song - No file 'very stressed.wav' found in working directory* 
**Solution: used /gameDev to enter the current folder.

[9]
Plays the song 

[10]
I captured every key being pressed and stored it into a changing variable called keys. Then I did [11], and came back to [10], 
and checked if the spacebar was being pressed. If it is, then the terminal will print "jump"

[11]
I created a CONSTANT variable and set it equal to a spacebar input

[12]
Drew a red sqaure that is 50 by 50 at the bottom of the screen which is the screen the height minus the height of the 
square. The red square is also in the middle of the bottom which is the screen width divided by 2.

[13]
I created some variables to 'vary' the player's position and then plugged those variables into the square 
stuff at [12]

[14a]
Created two more controls, left and right

[14b]
If the left arrow is pressed, then move the player to
the left and visa versa

[15]
Added a movement speed variable to control the player's
left and right movement. Then, I plugged that variable into
the [14b] step

[16]
I defined the numbers I'm going to use to check for
the left and right boundries.

[17]
I created variables to be used for the player's width
and height and plugged them in to [12]

[18]
square color variable

[19]
Created an inbounds function to check if the player
is inbounds or not

*Issue: The left and right bounds are freezing the player's
movement when you hit the boundries

**Solution: Create an if statement that nudges the player 
back into the game ONLY IF the player is not in bounds.

[20]
Added a fix to the boundry issue from [19] 

[21]
Made square color green when spacebar is pressed

[22]
Added a second square and gave it a different color, and
placed it at the top of the screen

[23]
Drew a circle

[24]
Made the variables for the circle to position, size,
and color the circle.

[25]
The ball moves now.
Also, the ball stays in the center of the paddles

*Issue: Can't get the circle to stop when it hits the bottom
of the top paddle. Ball keeps going too far.

**Solution: Used the mouse.get_pos() function to deduce
that I needed to use the ball radius because the 
check was using the center point on default.

[26]
Created a variable to use to switch the ball's 
direction at a certain point

[27]
Created two messages for the ball going up or down

[28]
Added in a score variable and prepared a font

[29]
Rendered the score font to the screen

[30]
When the ball hit either paddle, the score goes up by 1
point

*Issue: When updating the score, the number jumps up
by 2 instead of one like it should.

**Solution: When rendering the score, I turned the score
into an integer and set the score increment to a decimal,
forcing the score to round up to 1 each time.

*Issue: The ball was phasing through the top paddle 
if the ball speed was increased.
**Solution: Set the ball speed to a slower speed with 15 
being the best speed
'''
