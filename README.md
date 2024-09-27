# pygame
import pygame as pg 
import sys
pg.init()

class Game:
    def _init_(self):
        self.width=600
        self.height=768
        self.win=pg.display.set_mode((self.width,self.height))
        self.bg_img=pg.image.load("bg.png").convert()
        self.gameloop()
    
    def gameloop(self):
        while True:
            for events in pg.event.get():
                if events.type==pg.QUIT:
                    pg.Quit()
                    sys.exit()

            self.win.blit(self.bg_img,(0,0))
            pg.display.update()
            
game=Game()
