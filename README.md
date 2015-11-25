# Python-Sine-Wave-as-Rotation

## Sine Wave as Rotation
####Using python turtle graphics.
Nothing fancy, just part of my learning process. Could be a useful teaching tool.

	import turtle
	import math
	# turtleSet makes the code a bit more compact
	def turtleSet(name, shape, speed, color, pen, pos_x, pos_y):
	    name.ht()
	    name.up()
	    name.shape(shape)
	    name.speed(speed)
	    name.color(color)
	    name.pensize(pen)
	    name.setposition(pos_x, pos_y)
	    name.down()
	    name.st()
	wn = turtle.Screen()
	background = turtle.Turtle()
	background.speed(0)
	background.up()
	background.goto(325, 325)
	background.down()
	background.right(90)
	background.fillcolor("red")
	background.begin_fill()
	for i in range(4): # Draw a 650 x 650 square
	    background.forward(650)
	    background.right(90)
	background.end_fill()
	height = 200 #amplitude
	period = 25 # Period, but without any specific unit.
	circle = turtle.Turtle()
	turtleSet(circle, 'circle', 10, "green", 2, height, 0)
	circle.left(90)
	sine = turtle.Turtle()
	turtleSet(sine, 'circle', 10, "black", 2, -325, 0)
	sine.st()
	sine.left(45)
	line = turtle.Turtle()
	turtleSet(line, 'circle', 10, "blue", 2, -286, 0)
	line.left(90)
	time = turtle.Turtle()
	turtleSet(time, 'arrow', 10, "yellow", 2, -325, 0)
	time.right(0)
	for i in range(650):
	    x = height*math.cos(i/period)
	    y = height*math.sin(i/period)
	    sine.goto(i-325, y)
	    circle.goto(x, y)
	    line.goto(-286, y)
	    time.goto(i-325, 0)
	wn.exitonclick()

