Space Invaders
======

It's the game about shooting and matching!

Features
-----
  - Shooting the special food to be more fun 
  - Satisfy deleting

Game Explanation
-----
 - Arbitrarily shoooting food on top 
 - When some special food come down,shoot them and you will get a surprise

Method
----
 - First goes to player code,player keypoint is: left/right movement
 - 
 - Enemy Code


~~~python
class Enemy(Sprite):
    def on_create(self):
        self.scale=1
        self.rotation=180
        self.image=get_random_file_from_directory('food/')
        self.index=0
        self.x=1200
        self.y=500
        self.add_tag('enemy')
        self.is_dying = False
    def on_update(self, dt):
        target=waypoints[self.index]
        self.point_toward(target)
        self.move_forward(5)

        if self.distance_to(target) < 9 :
            self.index +=1

        if self.index>9:
            self.delete()
        
        if self.is_dying:
            self.rotation+=5
            self.scale+=5
~~~
 
  - Bullet Code
  
~~~python
  class Bullet(Sprite):
    def on_create(self):
        
        self.scale=50
        self.add_tag('bullet')
        self.rotation=90

    def on_update(self, dt):
        self.move_forward(10)
        if self.is_touching_window_edge():
            self.delete()
        for sprite in self.get_touching_sprites_with_tag('enemy'):
            sprite.delete()
            self.delete()
            self.timer=0
        for se in self.get_touching_sprites_with_tag('specialenemy'):
            se.delete()
            self.delete()
            for enemy in window.get_sprites_with_tag('enemy'):
                if enemy.image.replace('.png','') in se.image :
                    enemy.is_dying=True
                    Scheduler.wait(1,enemy.delete)
~~~       
   
Resources
-----

  - [pycat/python](https://www.python.org/)
  - [visual studio code](https://code.visualstudio.com/)
