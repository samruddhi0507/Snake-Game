# Snake-Game
## Author : Samruddhi Randive

The console based python application for one of the most famous games : snake game.

### Step 1 : Create the Screen:

To create the screen using Pygame, you will need to make use of the display.set_mode() function. Also, you will have to make use of the init()  and the quit() methods to initialize and uninitialize everything at the start and the end of the code. The update() method is used to update any changes made to the screen. There is another method i.e flip() that works similarly to the update() function. The difference is that the update() method updates only the changes that are made (however, if no parameters are passed, updates the complete screen) but the flip() method redoes the complete screen again.

#### CODE:
```
import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
pygame.display.update()
pygame.quit()
quit()
```
#### OUTPUT:
<img src= "https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/display1-Snake-Game-in-Python-Edureka.png" >


But when you run this code, the screen will appear, but it will immediately close as well. To fix that, you should make use of a game loop using the while loop before I actually quit the game as follows:

#### CODE:
```
import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
pygame.display.update()
pygame.display.set_caption('Snake game by samruddhi randive ')
game_over=False
while not game_over:
    for event in pygame.event.get():
        print(event)   #prints out all the actions that take place on the screen
 
pygame.quit()
quit()

```
 When you run this code, you will see that the screen that you saw earlier does not quit and also, it returns all the actions that take place over it. I have done that using the event.get() function. Also, I have named the screen as “Snake Game by samruddhi Randive ” using the display.set_caption() function.
 
#### OUTPUT:

 <img src ="https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/display2-Snake-Game-in-Python-Edureka.png">

 Now, you have a screen to play your Snake Game, but when you try to click on the close button, the screen does not close. This is because you have not specified that your screen should exit when you hit that close button. To do that, Pygame provides an event called “QUIT” and it should be used as follows:
 
 #### CODE:
 ```
 
 import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
pygame.display.update()
pygame.display.set_caption('Snake game by Edureka')
game_over=False
while not game_over:
    for event in pygame.event.get():
        if event.type==pygame.QUIT:
            game_over=True
 
pygame.quit()
quit()

```


So now your screen is all set. The next part is to draw our snake on the screen which is covered in the following topic.

### Step no 2 : Create the Snake

To create the snake, I will first initialize a few color variables in order to color the snake, food, screen, etc. The color scheme used in Pygame is RGB i.e “Red Green Blue”. In case you set all these to 0’s, the color will be black and all 255’s will be white. So our snake will actually be a rectangle. To draw rectangles in Pygame, you can make use of a function called draw.rect() which will help yo draw the rectangle with the desired color and size.

#### CODE:
```

import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
 
pygame.display.set_caption('Snake game by samruddhi randive')
 
blue=(0,0,255)
red=(255,0,0)
 
game_over=False
while not game_over:
    for event in pygame.event.get():
        if event.type==pygame.QUIT:
            game_over=True
    pygame.draw.rect(dis,blue,[200,150,10,10])
    pygame.display.update()
pygame.quit()
quit()

```
#### OUTPUT :
 <img src ="https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/creating-the-snake-Snake-Game-in-Python-Edureka.png">
 
 As you can see, the snakehead is created as a blue rectangle. The next step is to get your snake moving.
 
### Step no 3 : Moving the Snake

To move the snake, you will need to use the key events present in the KEYDOWN class of Pygame. The events that are used over here are, K_UP, K_DOWN, K_LEFT, and K_RIGHT to make the snake move up, down, left and right respectively. Also, the display screen is changed from the default black to white using the fill() method.

I have created new variables x1_change and y1_change in order to hold the updating values of the x and y coordinates.
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
