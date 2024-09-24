# githubproject1
Assignment 3
2024/09/16
Muthukuda Wijesuriya Arachchige Shasika Wijesuriya
1) Write a lambda expression to get the product of two numbers.
Run test for expression(5,6)
Output: 30
# writing a lambda expression :
product = lambda first_num,second_num:first_num*second_num

# Using the given values in the question :
result = product(5,6)
result
30
2)Write a function to get the area of a circle from the radius.
Hint: remember to import the right modul for being able to calculte the area of the circle.
Run test for function(10)
Output: 314.1592653589793
# importing the math module to get the pi value:
import math

# Using of math module:
def circle_area(Radius):
    return math.pi*Radius**2

# Calculating the area of the circle with the given radius value:
area_of_circle = circle_area(10)
print(area_of_circle)
    
314.1592653589793
3)Build a simple calculator which can: add, subtract, multiply, divide.
Hint: solve by writing a function that takes as argument two numbers and the operation and returns the desired output.
Run test for function(2,5,’d’)
Output: 0.4
def simple_calculator(first_num,second_num,math_operation):
    if math_operation == 'a' : # Math operation - addition
        return first_num + second_num
    elif math_operation == 's' : # Math operation - substraction
        return first_num - second_num
    elif math_operation == 'm': # Math operation - multiplication
        return first_num * second_num
    elif math_operation == 'd': # Math operation - division
        if second_num != 0:
            return first_num/second_num
        else :
            return "Error : Division from 0 is not valid"
    else :
        return " Invalid, maths operation"

# Testing the function with th given values:
final_result = simple_calculator(2,5,'d')

# Printing the result :
print(final_result)
0.4
4) Define a class named Rectangle which can be constructed by a length and width. The Rectangle class has a method which can compute the area.
Run test for r = Rectangle(5,10)
r.area()
Output: 50
# Creating the new class for Rectangle:
class Rectangle:
    def __init__(self, length,width):
        self.length = length
        self.width = width

# Constructing the method of computing area :
    def area(self):
        return self.length * self.width

# Testing the class :
r = Rectangle(5, 10)
final_result = r.area()

# printing the rsult :
print(final_result)
    
50
5) Define a class named Shape and its subclass Square. Shape objects can be consrtucted by name and length has an area function wich return 0.
Square subclass has an init function which take a length and name as argument and has an area method and a describe method what prints the name of the Shape.
Print the area from Square class.
Run test for: s = Square('square',5)
print(s.area())
print(s.describe())
Output: The area is: 25
This is a: square
# Creating a new base class for shape :
class shape:
    def __init__(self, name, length):
     self.name = name
     self.length = length

# Creatng the areea function which returns "0" :
    def area(self):
        return 0 

# Creating the subclass for square:
class Square(shape):
    def __ini__(self, name, length):
        super().__init__(name,length)

# Calculating the area of the square:
    def area(self):
        return self.length ** 2

    def describe(self):
        return f"This is a: {self.name}" 
        
# Testing the class :
s = Square('square', 5)
print(f"The area is:\n{s.area()}")
print(s.describe())
The area is:
25
This is a: square
