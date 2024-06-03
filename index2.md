Ninja Frog's Adventure
======

It's a game for those who think learning English is boring, this game contains the vocabularies, explanations, and sentence example. The game background is similar to Mario. If you like the operation of Mario, you gonna like it!

Demo video
----
- [Youtube-Ninja Frog's Adventure](https://youtu.be/aX6GnJbLGo0)

Features
------
- Cute character
- Simple gameplay operation 
- Help you build up vocabularies 

Game Explanation
------
Your initiate blood is zero, you need to touch the health package to read through the hint(contain example and sentences)  
Keep run right can end game 
Encounter enemies and answer questions to get results
- Level Ⅰ complete: look through all hint
- Level Ⅱ complete: Touch the enemy to pop up the answering window, answer questions and get points
- Level Ⅲ complete: Keep going RIGHT Answer all the enemy's question and can Complete the game

Method
------
- Type your name to get into the python game
-  Right & Left: press right & left
- Jump: Space
- Accelarate :Shift
 
------
Some feature code
-----
- main character (Continuous action photos)
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
- Background 
~~~python
game_map = [['0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0'],
            ['0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0'],
            ['0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0'],
            ['0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0'],
            ['0','0','0','0','0','0','0','2','2','2','2','2','0','0','0','0','0','0','0'],
            ['0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0'],
            ['2','2','0','0','0','0','0','0','0','0','0','0','0','0','0','0','0','2','2'],
            ['1','1','2','2','2','2','2','2','2','2','2','2','2','2','2','2','2','1','1'],
            ['1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1'],
            ['1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1'],
            ['1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1'],
            ['1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1'],
            ['1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1','1']]
~~~

- Blood

~~~python
lost_health_width = health_bar_width * (1 - (self.current_health / self.max_health))
lost_health_rect = pygame.Rect(health_bar_x + health_bar_width - lost_health_width, health_bar_y, lost_health_width, health_bar_height)
        pygame.draw.rect(screen, (255,0,0), lost_health_rect)

current_health_width = health_bar_width * (self.current_health / self.max_health)
current_health_rect = pygame.Rect(health_bar_x, health_bar_y, current_health_width, health_bar_height)
        pygame.draw.rect(screen, (0,255,0), current_health_rect)

health_bar_outline_rect = pygame.Rect(health_bar_x, health_bar_y, health_bar_width, health_bar_height)
        pygame.draw.rect(screen, (255,255,255), health_bar_outline_rect, 2)
~~~

- Hint

~~~python
hints = [
    {
        "word": "cushion",
        "meaning": "(v)減輕 (n)軟墊",
        "sentence": "The soft grass cushioned his fall. 柔軟的草地減緩了他摔落時的衝力。."
    },
    {
        "word": "take revenge on ",
        "meaning": "向...報復",
        "sentence": "The policeman swore to take revenge on the rubber who killed his partner.警察發誓他要報復殺了他夥伴的搶匪"
    },
    {
        "word": "habitual",
        "meaning": "習慣性的(慣犯:)",
        "sentence": "My uncle is a habitual gambler who pays regular visit to the local casino.我啊伯是常常跑去當地賭場的賭博慣犯"
    },
    {
        "word": "on the contrary/in contrast ",
        "meaning": "相反!!!/相對!!!",
        "sentence": "He is very outgoing, in contrast,his sister is quite shy.他很外向，相對她妹妹相當害羞"
    },
    {
        "word": "lean",
        "meaning": "傾斜 靠 脂肪少的",
        "sentence": "I eat only lean meat. 我只吃瘦肉 "
    },
    {
        "word": "spare",
        "meaning": "備用 多餘的 挪時間 饒恕",
        "sentence": "The king spared his life.國王饒他一命"
    },
    {
        "word": "pessimistic",
        "meaning": "悲觀:(",
        "sentence": "Pessimistic people always think of the worst.悲觀的人總是先想到壞處"
    },
    {
        "word": "content",
        "meaning": "內容 滿意",
        "sentence": "Eathon seems quite content with the way things are.Eathon 似乎相當安於現狀"
    },
]
~~~~

Resources
-----

  - ([Kenny game assets](https://www.kenney.nl/assets/category:2D))
