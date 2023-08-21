+++
title = "💻My Projects"
slug = "Projects"
+++
--------

# **Project 1 : Stone-Paper-Scissor Game In Python**
{{< tabgroup align="right" style="code" >}}
  {{< tab name="Python" >}}
```python

print("\nWellcom to Stone-Paper-Scissor\n")
import random
list1 = ["Stone","Paper","Scissor"]
computers_choice = random.choice(list1)
print("Choose Stone-Paper-Scissor.")
Players_Choice = input("Enter Your Choice : ")
print("computer choice :",computers_choice)

if (computers_choice == Players_Choice):
    print("!!!Tie!!!")

elif (computers_choice == "Stone" and Players_Choice == "Paper"):
    print("!!!You Won!!!")

elif (computers_choice == "Stone" and Players_Choice == "Scissor"):
    print("!!!Computer Won!!!")

elif (computers_choice == "Paper" and Players_Choice == "Stone"):
    print("!!!Computer Won!!!")

elif (computers_choice == "Paper" and Players_Choice == "Scissor"):
    print("!!!You won!!!")

elif (computers_choice == "Scissor" and Players_Choice == "Stone"):
    print("!!!You Won!!!")

elif (computers_choice == "Scissor" and Players_Choice == "Paper"):
    print("!!!Computer Won!!!")
 

```
{{< /tab >}}
{{< /tabgroup >}}

********

# **Project 2 : Password Lock System In Python**
{{< tabgroup align="right" style="code" >}}
  {{< tab name="Python" >}}
````python
print("\nSet Your Profile.")
ID = input("Enter Your ID 👉 : ")
password = input("Set The Password 👉 : ")

print("✔ Account Setup is complete ✔")

print("\nLog In Now,")
x = input("Enter ID Here 👉 : ")
y = input("Enter Passcode Here 👉 : ")

if (x == ID):
    print("Wellcome",ID,'👋,')

else:
    print("❌Invalid ID❌")

if(y==password):
    print("✔Correct password. Access Allowed✔")

else:
    print("❌Invalid Password❌")
````
{{< /tab >}}
{{< /tabgroup >}}
********
# **Project 3 : Snake-Water-Gun Game In Python**
{{< tabgroup align="right" style="code" >}}
  {{< tab name="Python" >}}
````python
import random

print("\nWellcome To Snake-Water-Gun Game !!!\n")


list1 = ["Snake", "Water","Gun"]
Computers_Choice = random.choice(list1)
print("{ Snake-Water-Gun }")
Players_Choice = input("Enter Option : ")
print(f"Computer choose : ",Computers_Choice)

if (Computers_Choice == Players_Choice):
    print("!!!Tie!!!")
   

elif (Computers_Choice == "Snake" and Players_Choice == "Water"):
    print("!!!Computer Won!!!") 

elif (Computers_Choice == "Snake" and Players_Choice == "Gun"):
    print("!!!You Won!!!")



elif (Computers_Choice == "Water" and Players_Choice == "Snake"):
    print("!!!You Won!!!") 

elif (Computers_Choice == "Water" and Players_Choice == "Gun"):
    print("!!!Computer Won!!!")


elif (Computers_Choice == "Gun" and Players_Choice == "Snake"):
    print("!!!Computer Won!!!") 

elif (Computers_Choice == "Gun" and Players_Choice == "Water"):
    print("!!!You Won!!!")

else :
    print("Invalid Input")
````
{{< /tab >}}
{{< /tabgroup >}}
******

# **Project 4 : Calculator In Python**
{{< tabgroup align="right" style="code" >}}
  {{< tab name="Python" >}}
````python
# 1. Notice For User
print("""\nUse 'add' for Addition.
Use 'sub' for Substraction.
Use 'multi' for Multiplication.
Use 'div' for Division.
Use 'power' for Power Calculations.\n""")

# 2.Variables And Data
x = input("Enter The 1st Number : ")
y = input("Enter The 2nd Number : ")
o = input("Enter The Operation : ")

# 3.Conditions
if (o == "add"):
    print(float(x) + float(y))

elif (o == "sub"):
    print(float(x) - float(y))

elif (o == "multi"):
    print(float(x) * float(y))

elif (o == "div"):
    print(float(x) / float(y))

elif (o == "power"):
    print(float(x) ** float(y)) 

else:
    print("Invalid Input")
````
{{< /tab >}}
{{< /tabgroup >}}
**************************************

# **Project 5 : Snake Game In Python**
{{< tabgroup align="right" style="code" >}}
  {{< tab name="Python" >}}
```python
import math
import random
import pygame
import random
import tkinter as tk
from tkinter import messagebox

width = 500
height = 500

cols = 25
rows = 20


class cube():
    rows = 20
    w = 500
    def __init__(self, start, dirnx=1, dirny=0, color=(255,0,0)):
        self.pos = start
        self.dirnx = dirnx
        self.dirny = dirny # "L", "R", "U", "D"
        self.color = color

    def move(self, dirnx, dirny):
        self.dirnx = dirnx
        self.dirny = dirny
        self.pos  = (self.pos[0] + self.dirnx, self.pos[1] + self.dirny)
            

    def draw(self, surface, eyes=False):
        dis = self.w // self.rows
        i = self.pos[0]
        j = self.pos[1]
        
        pygame.draw.rect(surface, self.color, (i*dis+1,j*dis+1,dis-2,dis-2))
        if eyes:
            centre = dis//2
            radius = 3
            circleMiddle = (i*dis+centre-radius,j*dis+8)
            circleMiddle2 = (i*dis + dis -radius*2, j*dis+8)
            pygame.draw.circle(surface, (0,0,0), circleMiddle, radius)
            pygame.draw.circle(surface, (0,0,0), circleMiddle2, radius)
        


class snake():
    body = []
    turns = {}
    
    def __init__(self, color, pos):
        #pos is given as coordinates on the grid ex (1,5)
        self.color = color
        self.head = cube(pos)
        self.body.append(self.head)
        self.dirnx = 0
        self.dirny = 1
    
    def move(self):
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
            keys = pygame.key.get_pressed()

            for key in keys:
                if keys[pygame.K_LEFT]:
                    self.dirnx = -1
                    self.dirny = 0
                    self.turns[self.head.pos[:]] = [self.dirnx,self.dirny]
                elif keys[pygame.K_RIGHT]:
                    self.dirnx = 1
                    self.dirny = 0
                    self.turns[self.head.pos[:]] = [self.dirnx,self.dirny]
                elif keys[pygame.K_UP]:
                    self.dirny = -1
                    self.dirnx = 0
                    self.turns[self.head.pos[:]] = [self.dirnx,self.dirny]
                elif keys[pygame.K_DOWN]:
                    self.dirny = 1
                    self.dirnx = 0
                    self.turns[self.head.pos[:]] = [self.dirnx,self.dirny]
        
        for i, c in enumerate(self.body):
            p = c.pos[:]
            if p in self.turns:
                turn = self.turns[p]
                c.move(turn[0], turn[1])
                if i == len(self.body)-1:
                    self.turns.pop(p)
            else:
                c.move(c.dirnx,c.dirny)
        
        
    def reset(self,pos):
        self.head = cube(pos)
        self.body = []
        self.body.append(self.head)
        self.turns = {}
        self.dirnx = 0
        self.dirny = 1

    def addCube(self):
        tail = self.body[-1]
        dx, dy = tail.dirnx, tail.dirny

        if dx == 1 and dy == 0:
            self.body.append(cube((tail.pos[0]-1,tail.pos[1])))
        elif dx == -1 and dy == 0:
            self.body.append(cube((tail.pos[0]+1,tail.pos[1])))
        elif dx == 0 and dy == 1:
            self.body.append(cube((tail.pos[0],tail.pos[1]-1)))
        elif dx == 0 and dy == -1:
            self.body.append(cube((tail.pos[0],tail.pos[1]+1)))

        self.body[-1].dirnx = dx
        self.body[-1].dirny = dy
    
    def draw(self, surface):
        for i,c in enumerate(self.body):
            if i == 0:
                c.draw(surface, True)
            else:
                c.draw(surface)



def redrawWindow():
    global win
    win.fill((0,0,0))
    drawGrid(width, rows, win)
    s.draw(win)
    snack.draw(win)
    pygame.display.update()
    pass



def drawGrid(w, rows, surface):
    sizeBtwn = w // rows

    x = 0
    y = 0
    for l in range(rows):
        x = x + sizeBtwn
        y = y +sizeBtwn

        pygame.draw.line(surface, (255,255,255), (x, 0),(x,w))
        pygame.draw.line(surface, (255,255,255), (0, y),(w,y))
    


def randomSnack(rows, item):
    positions = item.body

    while True:
        x = random.randrange(1,rows-1)
        y = random.randrange(1,rows-1)
        if len(list(filter(lambda z:z.pos == (x,y), positions))) > 0:
               continue
        else:
               break

    return (x,y)


def main():
    global s, snack, win
    win = pygame.display.set_mode((width,height))
    s = snake((255,0,0), (10,10))
    s.addCube()
    snack = cube(randomSnack(rows,s), color=(0,255,0))
    flag = True
    clock = pygame.time.Clock()
    
    while flag:
        pygame.time.delay(50)
        clock.tick(10)
        s.move()
        headPos = s.head.pos
        if headPos[0] >= 20 or headPos[0] < 0 or headPos[1] >= 20 or headPos[1] < 0:
            print("Score:", len(s.body))
            s.reset((10, 10))

        if s.body[0].pos == snack.pos:
            s.addCube()
            snack = cube(randomSnack(rows,s), color=(0,255,0))
            
        for x in range(len(s.body)):
            if s.body[x].pos in list(map(lambda z:z.pos,s.body[x+1:])):
                print("Score:", len(s.body))
                s.reset((10,10))
                break
                    
        redrawWindow()

main()

```
{{< /tab >}}
{{< /tabgroup >}}
