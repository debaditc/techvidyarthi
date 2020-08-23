---
title: "OOPs Concepts in nutshell"
date: 2020-08-22T11:31:55-04:00
weight : 3
tags: ["python", "class","object","oop"]
draft: false
---

### Features of OOP

- **Abstraction**   :   Act of hiding unnecessary information and showing relevant informaion. 
    
    **Real life example**
        
        [Watching TV and setup procedures are in TV manual. How TV internally works is part of data abstraction.]
        
- **Encapsulation** :   Wrapping up of data and operations in single unit.

    **Real life example**
        
        [Consider an ATM machine , it has both money (data) and ATM services (functions) integarted to ATM machine.]
        


- **Inheritance**   :   Act of inheriting features from parent class.
    
    **Real life example**
        
        [Grand parents -> Parents -> us -> our children 😃 ]
        

- **Polymorphism**  :   Process of representing one form in multiple forms

     **Real life example**
        
        [Consider behaiviour of a person : mother/father to their childern , wife/husband to their spouse , daughter/son to their parents , employee to a company , customer to a shopkeeper ,etc. At the end , its just a person]
        


- **Object** : Instance of class . It is a bundle of data and behaiviour


- **Class** : Its a blueprint of creating objects


### Simple Class and Object implementation in Python 

```python
class Startrek:
    shipname="StarShip Enterprise"
    
    # __init__ is a constructor which initializes the value | self is an instance - it can be named anything
    def __init__(self,name,dept,rank):
        self.name = name
        self.dept = dept
        self.rank = rank
    
    # method to print the data 
    def printfeatures(self):
        return f"Name - {self.name} | Dept - {self.dept} | Rank - {self.rank}"

# initiatizing objects to class Startrek
emp1=Startrek("Picard","Starship","Captain")
emp2=Startrek("Will Ryker","Starship","1st Officer")
emp3=Startrek("Daenna Troi","Starship","Counselor")
emp4=Startrek("Worf","Security","Lieutenant")
emp5=Startrek("La Forge","Engineering","Lieutenant")
emp6=Startrek("Data","Engineering","Commander")
emp7=Startrek("Crusher","Medical","Chief Medical officer")

# call the menthod from the class
print(emp1.printfeatures())
print(emp2.printfeatures())
print(emp3.printfeatures())
print(emp4.printfeatures())
print(emp5.printfeatures())
print(emp6.printfeatures())
print(emp7.printfeatures())


>>
Name - Picard | Dept - Starship | Rank - Captain
Name - Will Ryker | Dept - Starship | Rank - 1st Officer
Name - Daenna Troi | Dept - Starship | Rank - Counselor
Name - Worf | Dept - Security | Rank - Lieutenant
Name - La Forge | Dept - Engineering | Rank - Lieutenant
Name - Data | Dept - Engineering | Rank - Commander
Name - Crusher | Dept - Medical | Rank - Chief Medical officer

```

### Inheritance in Python 


```python

class Starship: 
       
    # Constructor 
    def __init__(self, name): 
        self.name = name 
   
    # To get name 
    def getName(self): 
        return self.name 
   
    # To check if this person is working in Starship
    def isWorking(self): 
        return False
   
   
# Inherited or Subclass (Note Starship in bracket) 
class Employee(Starship): 
   
    def isWorking(self): 
        return True
    
emp = Starship("Romulan")  # An Object of Starship 
print(emp.getName(), emp.isWorking()) 
   
emp = Employee("Picard") # An Object of Employee 
print(emp.getName(), emp.isWorking()) 


>>
Romulan False
Picard True

```