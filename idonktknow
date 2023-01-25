#! /usr/bin/env python
# -*- coding: utf-8 -*-
import datetime
import sys
import time
import pygame
#from PIL import Image
whiletrue = 0
omega = 6
#open('xyz3.txt', 'w').close()
paddlecoor =[]
ex = 1
paddlehit =[]
#WIDTH, HEIGHT = 1024, 768
# 341 * 256
WIDTH = 1023
HEIGHT = 768
fps = 60
SIZE = 15
BLUE = (0, 70, 225)
score = 0
snake = []
snakeobuch =[]
paddle_w = 50
paddle_h = 50
paddle_speed = 2

paddle_speed_obuch = 2
paddle = pygame.Rect(0,132,SIZE,SIZE)
paddleobuch = pygame.Rect(572,122,SIZE,SIZE)
block_list = []
blocklist2 = []
per = 1.1
pix = 3

# def fon(name):
#     blocklist = []
#     block_list =[]
#     img = Image.open(name)
#     size = w, h = img.size
#     data = img.load()
#     pieces = []
#     for x in range (w):
#         for y in range (h):
#             hex_color = '#' + ''.join([ hex(it)[2:].zfill(2).upper() for it in data[x,y]])
#             #print(hex_color)
#             if hex_color != '#FFFFFF':
#                 x1 = x * pix
#                 y1 = y * pix
#                 pieces.append((x1,y1))

    #blocklist += pieces
    # blocklist = 1
    # block_list = [pygame.Rect(i, j, pix, pix) for i, j in blocklist]
    # background = [pygame.Rect(i, j, pix, pix) for i, j in blocklist]
    # return block_list
######## координаты
pygame.init()
#sc = pygame.display.set_mode((WIDTH, HEIGHT))
sc = pygame.display.set_mode((WIDTH, HEIGHT))

clock = pygame.time.Clock()
ob = pygame.image.load('obuchlow.png').convert()
hellofon = pygame.image.load('hellolow.png').convert()

#img = pygame.image.load('finalfon.png').convert()
look_1 = pygame.image.load('lowfon.png').convert_alpha()
img = pygame.transform.scale(look_1, (1023, 768))
# block_list = (fon(('finalver2.png')))
# background = (fon(('finalver2.png')))
# img = pygame.image.load('fon3.png').convert()
#
# block_list = (fon(('test4.png')))
# background = (fon(('test4.png')))

with open("spisoklow.txt", "r") as file:
    blocklist = eval(file.readline())

block_list = [pygame.Rect(i, j, pix, pix) for i, j in blocklist]



summa = (len(block_list))
font_score = pygame.font.SysFont('Arial', 45, bold=True)
font_end = pygame.font.SysFont('Arial', 66, bold=True)
#snake=[(paddle.x,paddle.y)]
#snakeobuch=[(paddleobuch.x,paddleobuch.y)]
obuch = 0
hello = 0
while hello ==0:
    # pygame.init() will initialize all
    # imported module
    pygame.init()

    clock = pygame.time.Clock()

    # it will display on screen
    screen = pygame.display.set_mode([1024, 768])

    # basic font for user typed
    base_font = pygame.font.SysFont('arial', 36)
    user_text = ''

    # create rectangle
    input_rect = pygame.Rect(10, 725, 10, 40)
    skip_obuch = pygame.Rect(0, 500, 500, 50)
    sinhron = pygame.Rect(820, 750, 150, 25)
    continuetest = pygame.Rect(0, 400, 370, 50)

    # color_active stores color(lightskyblue3) which
    # gets active when input box is clicked by user
    color_active = pygame.Color('lightskyblue3')
    # color_passive store color(chartreuse4) which is
    # color of input box.
    color_passive = pygame.Color('chartreuse4')
    color = color_passive

    active = False
    active1= False
    active2 = False
    active3= False
    while whiletrue ==0:
        for event in pygame.event.get():

            # if user types QUIT then the screen will close
            if event.type == pygame.QUIT:
                pygame.quit()
                sys.exit()

            if event.type == pygame.MOUSEBUTTONDOWN:
                if input_rect.collidepoint(event.pos):
                    active = True
                else:
                    active = False
            if event.type == pygame.MOUSEBUTTONDOWN:
                if skip_obuch.collidepoint(event.pos):
                    active1 = True
                else:
                    active1 = False
            if event.type == pygame.MOUSEBUTTONDOWN:
                if sinhron.collidepoint(event.pos):
                    active3 = True
                else:
                    active3 = False
            if event.type == pygame.MOUSEBUTTONDOWN:
                if continuetest.collidepoint(event.pos):
                    active2 = True
                else:
                    active2 = False
            if event.type == pygame.KEYDOWN:

                # Check for backspace
                if event.key == pygame.K_BACKSPACE:

                    # get text input from 0 to -1 i.e. end.
                    user_text = user_text[:-1]

                # Unicode standard is used for string
                # formation
                else:
                    user_text += event.unicode

        # it will set background color of screen
        #screen.fill((255, 255, 255))
        sc.blit(hellofon, (0, 0))

        if active:
            color = color_active
        else:
            color = color_passive
        if active1:
            hello = 1
            obuch = 1
            whiletrue =1
        if active2:
            hello = 1
            whiletrue = 1

        if active3:
            hello = 1
            whiletrue = 1
            omega = 0

        # draw rectangle and argument passed which should
        # be on screen
        pygame.draw.rect(screen, color, input_rect)
        #pygame.draw.rect(screen, color, skip_obuch)
        #pygame.draw.rect(screen, color, continuetest)
        #pygame.draw.rect(screen, color, sinhron)


        text_surface = base_font.render(user_text, True, (255, 255, 255))

        # render at position stated in arguments
        screen.blit(text_surface, (input_rect.x + 5, input_rect.y + 5))

        # set width of textfield so that text cannot get
        # outside of user's text input
        input_rect.w = max(100, text_surface.get_width() + 10)

        # display.flip() will update only a portion of the
        # screen to updated, not full area
        pygame.display.flip()

        # clock.tick(60) means that for every second at most
        # 60 frames should be passed.
        #print(user_text)
        clock.tick(60)
        #shirina1 = round(summa/20,-1) * pix * pix
#print('shirina is',shirina1)
#shirina = int(shirina1)
#shirina = 1360
Fin = open ( "speedshirina.txt" )
stroka1 = Fin.readline().split()
speed111 = int(stroka1[0])
shirina = int(stroka1[1])
length = int(stroka1[2])
print(speed111, 'this is my speed')
print(shirina, 'this is my shirina')

timerlist = [pygame.Rect(100 + 1 * i, 100 + 1 * j, 1, 1) for i in range(shirina) for j in range(15)]
timerpaddle = pygame.Rect(80,100,SIZE,SIZE)
score1=0
timercoor =[]
scorebefore1=0
timebefore=0
boarder = shirina + 100

while omega == 0:
    if timebefore == 0:
        timebefore = time.time()
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            exit()
    sc.fill(BLUE)
    #sc.blit(img, (0, 0))

    [ pygame.draw.rect(sc, pygame.Color('green'), block) for color, block in enumerate(timerlist)]
    pygame.draw.rect(sc, pygame.Color('darkorange'), timerpaddle)

    if timerpaddle.right < boarder:
        timerpaddle.right += paddle_speed
    timercoor.append((timerpaddle.x, timerpaddle.y))
    timerhit = [pygame.Rect(i, j, SIZE, SIZE) for i, j in timercoor]
    pygame.display.flip()
    if timerpaddle.right > boarder:
        omega = 1
        print('len is',len(timerlist))
        timeafter = time.time()
while len(timerlist) != 0 and omega == 1:
    timeafter2 = time.time()
    for el in timerhit:
        hit_index = el.collidelist(timerlist)
        if hit_index != -1:
            hit_rect = timerlist.pop(hit_index)
            score1 += 1
            if len(timerlist) == 0:
                omega = 2

    if omega == 2 and len(timerlist) == 0:
        dtime = timeafter - timebefore; speed = score1 / dtime
        dtime2 = timeafter2 - timebefore; speed2 = score1/dtime2
        print('dtime is', dtime)
        print('speed is', speed)
        f = open('logs.txt', 'a')
        logs = str(dtime), str(speed)
        f.write(str(logs) +"\n")
        f.close()

obuch_clear = pygame.Rect(558, 38, 130, 28)
obuch_position = pygame.Rect(740, 38, 260, 28)
gotest = pygame.Rect(178, 634, 250, 80)
while obuch == 0:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            exit()
    sc.blit(ob, (0, 0))
    [pygame.draw.rect(sc, pygame.Color('red'), (i, j, SIZE, SIZE)) for i, j in snakeobuch]
    # pygame.draw.rect(screen, color, obuch_clear)
    # pygame.draw.rect(screen, color, obuch_position)
    # pygame.draw.rect(screen, color, gotest)
    #print(paddleobuch.x,paddleobuch.y)
    pygame.draw.rect(sc, pygame.Color('darkorange'), paddleobuch)


    if event.type == pygame.MOUSEBUTTONDOWN:
        if obuch_clear.collidepoint(event.pos):
            snakeobuch = []
        if obuch_position.collidepoint(event.pos):
            snakeobuch=[]
            paddleobuch = pygame.Rect(572, 122, SIZE, SIZE)
    snakeobuch = snakeobuch[-length:]

    # pygame.draw.rect(screen, color, obuch_clear)
    # pygame.draw.rect(screen, color, obuch_position)
    key = pygame.key.get_pressed()
    if key[pygame.K_SPACE]:
        snakeobuch.append((paddleobuch.x, paddleobuch.y))
    #if key[pygame.K_0]:
        #snakeobuch=[]
    #if key[pygame.K_9]:
        #obuch =1
#####
    if event.type == pygame.MOUSEBUTTONDOWN:
        if gotest.collidepoint(event.pos):
            obuch=1

#####
    if key[pygame.K_RSHIFT] and paddleobuch.right < WIDTH:
        paddle_speed_obuch = 4
    else:
        paddle_speed_obuch = 2
    # if key[pygame.K_p] and paddleobuch.right < 1378 and paddleobuch.top > 38 and paddleobuch.left > 878 and paddleobuch.bottom > 736:
    #     paddle_speed_obuch += 0.2
    # if key[pygame.K_o] and paddleobuch.right < 1378 and paddleobuch.top > 38 and paddleobuch.left > 878 and paddleobuch.bottom > 736:
    #     paddle_speed_obuch -= 0.2
    if key[pygame.K_q]and paddleobuch.right < 1002 and paddleobuch.top > 70 and paddleobuch.left > 562 and paddleobuch.bottom > 700:
        paddleobuch.y -= paddle_speed_obuch
        paddleobuch.x -= paddle_speed_obuch
    if key[pygame.K_e] and paddleobuch.right < 1002 and paddleobuch.top > 70 and paddleobuch.left > 562 and paddleobuch.bottom > 700:
        paddleobuch.y -= paddle_speed_obuch
        paddleobuch.x += paddle_speed_obuch
    if key[pygame.K_z]  and paddleobuch.right < 1002 and paddleobuch.top > 70 and paddleobuch.left > 562 and paddleobuch.bottom > 700:
        paddleobuch.y += paddle_speed_obuch
        paddleobuch.x -= paddle_speed_obuch
    if key[pygame.K_x]  and paddleobuch.right < 1002 and paddleobuch.top > 70 and paddleobuch.left > 562 and paddleobuch.bottom > 700:
        paddleobuch.y += paddle_speed_obuch
        paddleobuch.x += paddle_speed_obuch
    if key[pygame.K_LEFT] and paddleobuch.left > 562:
        paddleobuch.left -= paddle_speed_obuch
    if key[pygame.K_d] and paddleobuch.right < 1002:
        paddleobuch.right += paddle_speed_obuch
    if key[pygame.K_UP] and paddleobuch.top > 70 :
        paddleobuch.y -= paddle_speed_obuch
    if key[pygame.K_s] and paddleobuch.bottom < 700:
        paddleobuch.y += paddle_speed_obuch
    if key[pygame.K_1]:
        ex = 0
        timeend = time.time()
        print('time end is', timeend)
    pygame.display.flip()
    clock.tick(fps)




while ex==1 :
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            exit()
    sc.blit(img, (0, 0))
    #sc.fill(BLUE)
    #[pygame.draw.rect(sc, pygame.Color('green'), block) for color, block in enumerate(block_list)]
    #[pygame.draw.rect(sc, pygame.Color('green'), block) for color, block in enumerate(background)]
    [pygame.draw.rect(sc, pygame.Color('red'), (i, j, SIZE, SIZE)) for i, j in snake]
    pygame.draw.rect(sc, pygame.Color('darkorange'), paddle)
    #render_score = font_score.render(f'SCORE: {score}', 1, pygame.Color('orange'))
    #sc.blit(render_score, (5, 5))
    snake = snake[-length:]
    #print(paddle.x,paddle.y)

    #paddlelist = [(paddle.x + i, paddle.y +j) for i in range(SIZE) for j in range(SIZE)]
    #paddledelist = [pygame.Rect(i, j, 1, 1) for i, j in paddlelist]

    # for el in paddledelist:
    #     hit_index=el.collidelist(block_list)
    #     key = pygame.key.get_pressed()
    #
    #     if key[pygame.K_b]:
    #         #[pygame.draw.rect(sc, pygame.Color('purple'), (i, j, 20, 20)) for i, j in snake]
    #
    #         if hit_index != -1:
    #             hit_rect = block_list.pop(hit_index)
    #             score += 1

   ########
    # paddlecoor.append((paddle.x, paddle.y))
    # paddlehit = [pygame.Rect(i, j, SIZE, SIZE) for i, j in paddlecoor]


    #procent = score / summa * 100
    #font_procent = pygame.font.SysFont('Arial', 26, bold=True)
    # font_end = pygame.font.SysFont('Arial', 66, bold=True)
    #font_procent = pygame.font.SysFont('Arial', 26, bold=True)
    # font_end = pygame.font.SysFont('Arial', 66, bold=True)
    #print(summa)
    #render_procent = font_procent.render(f'procent: {procent}', 1, pygame.Color('orange'))
    #sc.blit(render_procent, (30, 35))

    ###########
    key = pygame.key.get_pressed()
    # if key[pygame.K_KP4] and paddle.left > 0:
    #     paddle.left -= paddle_speed
    # if key[pygame.K_KP6] and paddle.right < WIDTH:
    #     paddle.right += paddle_speed
    # if key[pygame.K_KP8] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    # if key[pygame.K_KP2] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    # if key[pygame.K_KP7] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    #     paddle.x -= paddle_speed
    # if key[pygame.K_KP9] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    #     paddle.x += paddle_speed
    # if key[pygame.K_KP1] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    #     paddle.x -= paddle_speed
    # if key[pygame.K_KP3] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    #     paddle.x += paddle_speed
    #     ###
    # if key[pygame.K_p] and paddle.right < WIDTH:
    #     paddle_speed += 0.2
    # if key[pygame.K_o] and paddle.right < WIDTH:
    #     paddle_speed -= 0.2
    if key[pygame.K_RSHIFT] and paddle.right < WIDTH:
        paddle_speed = 4
    else:
        paddle_speed = 2

#####
    # if key[pygame.K_q] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    #     paddle.x -= paddle_speed
    # if key[pygame.K_e] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    #     paddle.x += paddle_speed
    # if key[pygame.K_z] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    #     paddle.x -= paddle_speed
    # if key[pygame.K_x] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    #     paddle.x += paddle_speed
    # if key[pygame.K_LEFT] and paddle.left > 0:
    #     paddle.left -= paddle_speed
    # if key[pygame.K_RIGHT] and paddle.right < WIDTH:
    #     paddle.right += paddle_speed
    # if key[pygame.K_UP] and paddle.right < WIDTH:
    #     paddle.y -= paddle_speed
    # if key[pygame.K_DOWN] and paddle.right < WIDTH:
    #     paddle.y += paddle_speed
    #if key[pygame.K_1]:
    if paddle.x in range(140, 170) and paddle.y in range(490, 514):
        ex=0
        timeend = time.time()
        print('time end is', timeend)
    if key[pygame.K_LEFT] and paddle.left > 0:
        paddle.left -= paddle_speed
    if key[pygame.K_d] and paddle.right < WIDTH:
        paddle.right += paddle_speed
    if key[pygame.K_UP] and paddle.right < WIDTH:
        paddle.y -= paddle_speed
    if key[pygame.K_s] and paddle.right < WIDTH:
        paddle.y += paddle_speed
    ####
    #print((paddle.x, paddle.y))
    #teleport
    #if paddle.x in range (190,240) and paddle.y in range (530,565):

    #     paddle.x = 44
    #     paddle.y = 412
    ####
    #print(paddle.x,paddle.y)
    oscar = (paddle.x,paddle.y)
    if oscar not in snake:
        if key[pygame.K_SPACE]:
            if len(paddlehit) ==0:
                timestart=time.time()
                print('timestart is', timestart)
            snake.append((paddle.x, paddle.y))
            paddlecoor.append((paddle.x, paddle.y))
            paddlehit = [pygame.Rect(i, j, SIZE, SIZE) for i, j in paddlecoor]

    # if key[pygame.K_t]:
    #
    #     if per > 1:
    #         score = 10000
    #         block_list = (fon(('testv1.png')))
    #         background = (fon(('testv1.png')))
    #         snake.clear()
    #         paddle.x = 100
    #         paddle.y = 100
    #
    #     if per > 2:
    #         score = 10000
    #         block_list = (fon(('murat.png')))
    #         background = (fon(('murat.png')))
    #         snake.clear()
    #         paddle.x = 100
    #         paddle.y = 100
    #     per += 1
    #     #print(per)







    #print((snake))


## sum pixels
    pygame.display.flip()
    clock.tick(fps)

scorebefore = -1

#print(len(paddlehit))
while scorebefore < score:
    scorebefore = score + 1
    for el in paddlehit:
        hit_index = el.collidelist(block_list)
        if hit_index != -1:
            hit_rect = block_list.pop(hit_index)
            scorebefore = score
            score += 1

#print(score)
#print(procent)
#f.write(str(print(score)))
#f.close()
# data = []
# with open("speed.txt") as l:
#     for line in l:
#         data.append([float(x) for x in line.split()])
# for el in data:
#     speedtest = el
# print('your speedtest is',speedtest)
#




dtimestartend= timeend - timestart
timescore = summa * 16 / speed111
#timeis = dtimestartend/timescore # наше время / на общее
timeis = timescore/dtimestartend * 100
score = score + 0.0000001
summa = summa + 0.00000001
procent1 = score * 1 / summa * 100
# print('procent1 is', procent1)
# print('summa')
# print(summa)
# print('timescore')
# print(timescore)
# print('dtimes')
# print(dtimestartend)
#print('your time scoore is ', dtimestartend/dtime)
#print('your speed is ',speed,'sec per pixel','your dtime is', dtime)
#print('your speed2 is ',speed,'sec per pixel','your dtime2 is', dtime)
#print('your score time is ', dtimestartend/timescore)
#print('score')
#print(score)
#print('summa')
#print(summa)


while True:
    pygame.init()

    # define the RGB value for white,
    #  green, blue colour .
    white = (255, 255, 255)
    green = (0, 255, 0)
    blue = (0, 0, 128)

    # assigning values to X and Y variable
    X = 1024
    Y = 768

    # create the display surface object
    # of specific dimension..e(X, Y).
    display_surface = pygame.display.set_mode((X, Y))

    #
    # # set the pygame window name
    # pygame.display.set_caption('Show Text')
    #
    # # create a font object.
    # # 1st parameter is the font file
    # # which is present in pygame.
    # # 2nd parameter is size of the font
    # font = pygame.font.SysFont('arial', 36)
    #
    #
    # # create a text surface object,
    # # on which text is drawn on it.
    average = (procent1 + timeis) / 2
    #f.close()
    f = open('results.txt', 'a')
    #showstroka = 'O4ku: -', str(round(procent1,3)),'Time', str(round(timeis,2)), 'Effectivnost', str(round(average,3))
    stroka = 'O4ku: -',str(round(procent1,3)),'Time', str(round(timeis,2)), 'Effectivnost', str(round(average,3))
    #text = font.render(str(stroka), True, green, blue)
    #sc.blit(text, (5, 5))
    datetime_object = datetime.datetime.now()
    totaltext =str(procent1),str(timeis),str(user_text),str('data'),str(datetime_object), str('effectivnost'),str(average)
    f.write(str(totaltext) + "\n")
    f.close()
    #
    #
    ochki = 'O4ku: -',str(round(procent1,3))
    vremya ='Time', str(round(timeis,2))
    effectivnost='Effectivnost', str(round(average,3))
    render_score1 = font_score.render(str(ochki), 1, pygame.Color('orange'))
    render_score2= font_score.render(str(vremya), 1, pygame.Color('orange'))
    render_score3 = font_score.render(str(effectivnost), 1, pygame.Color('orange'))
    # # create a rectangular object for the
    # # text surface object
    # textRect = text.get_rect()
    #
    # # set the center of the rectangular object.
    # textRect.center = (X // 2, Y // 2)
    #
    # # infinite loop
    while True:

        # completely fill the surface object
        # with white color
        # copying the text surface object
        # to the display surface object
        # at the center coordinat
        sc.blit(render_score1, (50, 100))
        sc.blit(render_score2, (50, 300))
        sc.blit(render_score3, (50, 600))

        pygame.display.update()
        # iterate over the list of Event objects
        # that was returned by pygame.event.get() method.
        for event in pygame.event.get():

            # if event object type is QUIT
            # then quitting the pygame
            # and program both.
            if event.type == pygame.QUIT:
                # deactivates the pygame library
                pygame.quit()

                # quit the program.
                quit()
    #
    #         # Draws the surface object to the screen.
    #         pygame.display.update()
    #

#f.close()
