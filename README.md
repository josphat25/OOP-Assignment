# OOP-Assignment
## Assignment 1: Design Your Own Class! 🏗️
### 1.Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).
### 2.Add attributes and methods to bring the class to life!
### 3.Use constructors to initialize each object with unique values.
### 4.Add an inheritance layer to explore polymorphism or encapsulation.

We'll create a class for a Superhero, and then extend it with a child class using inheritance.

class Superhero:

    def __init__(self, name, power, city):
    
        self.name = name
        
        self.power = power
        
        self.city = city

    def describe(self):
    
        return f"{self.name} protects {self.city} using {self.power}!"

    def use_power(self):
    
        return f"{self.name} uses {self.power} to fight crime!"
# Child Class: Speedster (inherits from Superhero)
class Speedster(Superhero):

    def __init__(self, name, city, max_speed):
    
        super().__init__(name, "Super Speed", city)
        
        self.max_speed = max_speed

    def use_power(self):
    
        return f"{self.name} zooms through {self.city} at {self.max_speed} km/h!"


## Activity 2: Polymorphism Challenge! 🎭

### Create a program that includes animals or vehicles with the same action (like move()). However, make each class define move() differently (for example, Car.move() prints "Driving" 🚗, while Plane.move() prints "Flying" ✈️).
Another Child Class: Telepath

class Telepath(Superhero):

    def __init__(self, name, city, mind_range):
    
        super().__init__(name, "Mind Control", city)
        
        self.mind_range = mind_range

    def use_power(self):
    
        return f"{self.name} controls minds within {self.mind_range} meters!"

        Polymorphism in Action:

        heroes = [
        
    Speedster("FlashFire", "Metroville", 1200),
    
    Telepath("MindMist", "NeuroCity", 500),
    
    Superhero("IronStorm", "Steel Harbor", "Magnetic Manipulation")
    
]

for hero in heroes:

    print(hero.use_power())

    Output:

FlashFire zooms through Metroville at 1200 km/h!

MindMist controls minds within 500 meters!

IronStorm uses Magnetic Manipulation to fight crime!



