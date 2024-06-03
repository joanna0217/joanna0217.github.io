Ninja Frog's Adventure
======

It's a game for those who think learning English is boring, this game contains the vocabularies, explanations, and sentence example. The game background is similar to Mario. If you like the operation of Mario, you gonna like it!

Demo video
----
- [Youtube-Ninja Frog's Adventure](https://youtu.be/aX6GnJbLGo0)

Features
------
- Cute charactor
- Simple gameplay operation 
- Help you build up vocabularies 

Game Explanation
------
Your initiate blood is zero, you need to touch the health package to read through the hint(contain example and sentences)  
Keep run right can end game 
- Level Ⅰ complete: look through all hint
- Level Ⅱ complete: 
- Level Ⅲ complete:

Method
------
- Type your name to get into the python game
-  right & left: press right & left
- Jump: space
- accelarate :shift

------
Some feature code
-----
- Charactor (Continuous action photos)
~~~python
for image in images:
        # print(join(path, image))
        sprite_sheet = pygame.image.load(join(path, image)).convert_alpha()
        sprites = []
sprite_sheet=pygame.transform.smoothscale(sprite_sheet, (384, 32))
            for i in range(sprite_sheet.get_width() // new_width):
                surface = pygame.Surface((new_width, new_height), pygame.SRCALPHA, 32)
surface.blit(sprite_sheet, (0, 0), rect)
 #sprites.append(surface)
~~~
