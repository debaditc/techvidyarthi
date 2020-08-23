---
title: "Python : *args vs **kwargs"
date: 2020-08-21T23:58:38-04:00
weight: 3
tags: ["python", "args","kwargs"]
draft: false
---

### *args

It is used to pass variable number of arguments to a function

```python
def printFunc(arg1, *argv): 
    print ("Argument via argv1 :", arg1) 
    for arg in argv: 
        print("Argument via *argv :", arg) 
  
printFunc('Hello', 'this', 'is', 'Debaditya') 

>> First argument : Hello
Argument *argv : this
Argument *argv : is
Argument *argv : Debaditya

```


### **kwargs

It is used to pass variable number of **keyworded arguments** to a function

```python
def printFunc(arg1, arg2, arg3): 
    print("arg1:", arg1 ) 
    print("arg2:", arg2) 
    print("arg3:", arg3) 
      
args = ("This", "is", "Debaditya") 
printFunc(*args) 
  
kwargs = {"arg1" : "This", "arg2" : "is", "arg3" : "Debaditya"} 
printFunc(**kwargs)

```

More contents and details are here [Geeksforgeeks](https://www.geeksforgeeks.org/args-kwargs-python/)