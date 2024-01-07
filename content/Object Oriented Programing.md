---
{"dg-publish":true,"permalink":"/object-oriented-programing/","title":"Object Oriented Programing"}
---

# Object Oriented Programing

# [[Python\|Python]]
```python
class thing:
	x = 0
	y = 0
	#Function that runs when the object is constructed
	def __init__(self, att):
		self.x = x
		self.y = y
	#Function that runs when the object is deconstructed
	def __del__(self):
		print(self, ": I'm deconstructed")

	#Function that runs when the object is constructed
	def __init__(self, att):
```

# Inheritance
- Inheritance is to create a class that extends the capability of another parent class
```python
class thing:
	x = 0
	y = 0

class ball(thing):
	speed = 1;
```