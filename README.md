# Snake-Game
## Author : Samruddhi Randive

The console based python application for one of the most famous games : snake game.

### Step 1 : Create the Screen:

To create the screen using Pygame, you will need to make use of the display.set_mode() function. Also, you will have to make use of the init()  and the quit() methods to initialize and uninitialize everything at the start and the end of the code. The update() method is used to update any changes made to the screen. There is another method i.e flip() that works similarly to the update() function. The difference is that the update() method updates only the changes that are made (however, if no parameters are passed, updates the complete screen) but the flip() method redoes the complete screen again.

### CODE:
```
import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
pygame.display.update()
pygame.quit()
quit()
```
### output:
<img src= "https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/display1-Snake-Game-in-Python-Edureka.png" >


But when you run this code, the screen will appear, but it will immediately close as well. To fix that, you should make use of a game loop using the while loop before I actually quit the game as follows:

```
import pygame
pygame.init()
dis=pygame.display.set_mode((400,300))
pygame.display.update()
pygame.display.set_caption('Snake game by Edureka')
game_over=False
while not game_over:
    for event in pygame.event.get():
        print(event)   #prints out all the actions that take place on the screen
 
pygame.quit()
quit()

```
When you run this code, you will see that the screen that you saw earlier does not quit and also, it returns all the actions that take place over it. I have done that using the event.get() function. Also, I have named the screen as “Snake Game by Edureka” using the display.set_caption() function.

<img scr ="https://d1jnx9ba8s6j9r.cloudfront.net/blog/wp-content/uploads/2019/10/display2-Snake-Game-in-Python-Edureka.png">




