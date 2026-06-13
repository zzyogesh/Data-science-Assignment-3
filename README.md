# Data-science-Assignment-3

# Q.1.Create a class named Student with attributes: 
#  name  
#  age  
#  course  
# Create an object and print all the details. 

class Student:
    name="Yogesh"
    Age="20"
    course="python"
std=Student()
print(std.name)
print(std.Age)
print(std.course)

# Q.2. Create a class named Car with attributes: 
#  brand  
#  model  
#  price  
#  Create two objects and display their details.

class Car:
    def __init__(self,brand,model,price):
        self.brand=brand
        self.model=model
        self.price=price
std=Car("Toyota","fortuner",2500000)
std1=Car("hundai","i20",800000)
print(std.brand)
print(std.model)
print(std.price)
print(std1.brand)
print(std1.model)
print(std1.price)

# 3. Create a class named Employee and use a constructor (__init__) to  initialize: 
#  employee_id  
#  name  
#  salary  
#  Print the employee details.
 
class Employee:
    def __init__(self,employeeid,name,salary):
        self.employeeid=employeeid
        self.name=name
        self.salary=salary
emp=Employee(101,"Yogesh",50000)
print(emp.employeeid)
print(emp.name)
print(emp.salary)

# 4. Create a class named Rectangle with attributes: 
#  length  
#  width  
# Create a method to calculate and print the area of the rectangle.

class Rectangle:
    def __init__(self,length,width):
        self.length=length
        self.width=width
    def calculate_area(self):
        area=self.length*self.width
        print(area)
rect=Rectangle(5,10)
rect.calculate_area()    

# 5. Create a class named Circle with an attribute radius. 
#     Create a method that calculates and prints the area of the circle.

class Circle:
    def __init__(self,radious):
        self.radious=radious
    def calculate_area(self):
        area=3.14*self.radious
        print("Area is circle is:",area)

c=Circle(5)
c.calculate_area()


# 6. Create a class named BankAccount with: 
#  account_holder  
#  balance  
#  Create methods: 
#  deposit(amount)  
#  withdraw(amount)  
#  Display the updated balance after each transaction. 

class BankAccount:
    def __init__(self,account_holder,balance):
        self.account_holder=account_holder
        self.balance=balance
    def deposit(self,amount):
        self.balance += amount
        print(f"Deposited {amount}.Updated balance:{self.balance}")
    def withdraw(self,amount):    
        if amount<=self.balance:
            self.balance -= amount
            print(f"withdraw {amount}.Updated balance:{self.balance}")
        else:
            print("insufficient balance")


account=BankAccount("Yogesh kumar",10000)
account.deposit(500)
account.withdraw(700)

# 7. Create a class named Animal with a method sound(). 
#  Create a child class Dog that overrides the sound() method and prints "Bark". 


class Animal:
    def sound(self):
        print("animal sounds")
class Dog(Animal):
    def sound(self):
        print("bark")    

A= Animal()
A.sound()

d=Dog()
d.sound()


# 8. Create a class named Person with attributes: 
#  name  
#  age  
#  Create a child class Student with an additional attribute: 
#  roll_number  
# Display all the details using an object of the Student class. 


class Person:
    def __init__(self,name,age):
        self.name=name
        self.age=age
class Student(Person):
    def __init__(self, name, age, roll_number):
        super().__init__(name, age)
        self.roll_number=roll_number 
    def display_details(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")
        print(f"Roll Number: {self.roll_number}") 

std = Student("Yogesh", 22, "25ebkcs212")
std.display_details()

# 9. Create a class named Calculator with methods: 
#  add()  
#  subtract()  
#  multiply()  
#  divide()  
#  Take two numbers as input and perform all operations.


class Calculator:
    def __init__(self,num1,num2):
        self.num1=num1
        self.num2=num2
    def add(self):
        print("Addition:",self.num1+self.num2)
    def substract(self):
        print("substract:",self.num1-self.num2)
    def multiply(self):
        print("multiply:",self.num1*self.num2)
    def divide(self):
        print("divide:",self.num1/self.num2)    

calc=Calculator(10,5)
calc.add()
calc.substract()
calc.multiply()
calc.divide()

# 10. Create a class named LibraryBook with attributes:  
# ● book_name  
# ● author  
# ● price  
# Create a method display_book_info() that prints all book details. Create    
# at least three book objects and display their information
    
class LibraryBook:
    def __init__(self, book_name, author, price):
        self.book_name = book_name
        self.author = author
        self.price = price

    def display_book_info(self):
        print(f"Book Name: {self.book_name}")
        print(f"Author: {self.author}")
        print(f"Price: {self.price}")


book1 = LibraryBook("Python Basics", "John Smith", 450)
book2 = LibraryBook("Data Structures", "Jane Doe", 600)
book3 = LibraryBook("Machine Learning", "Andrew Ng", 800)

book1.display_book_info()
book2.display_book_info()
book3.display_book_info()
