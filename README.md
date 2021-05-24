# Snake-Game
## Author : Samruddhi Randive

The console based python application for one of the most famous games : snake game.

### step1 : Create the Screen:

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

