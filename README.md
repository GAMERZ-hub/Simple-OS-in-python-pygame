# Simple-OS-in-python-pygame
import time
import menubar2
correctpass=False
if correctpass==True:
    print("logging in","please wait")
print("what do you want your password to be?")
password=input()
print("ok","loading")
time.sleep(2)
print("what is your password? You get two chances")
entered_password=input()
if entered_password == password:
    correctpass=True
else:
    print("wrong password")
    attempt=input()
    if attempt == password:
        correctpass=True
    else:
        exit()
        
import pygame
from pygame.locals import *
pygame.init()
screen=pygame.display.set_mode((600,600))
white=(255,255,255)
black=(0,0,0)
while True:
    menubar2.menu()
    
    for event in pygame.event.get():
        if event.type == QUIT:
            pygame.quit()
            exit()
    pygame.display.update()
