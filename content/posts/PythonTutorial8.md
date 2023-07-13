+++
authors= "Gitesh Wagh"
title = " Project 2: Calculator - Python Tutorials For Beginners #8"
date = "2023-07-13"
categories = "Python Programming"
tags = [
  "Programming", 
  "Coding",
  "python",
  "PythonTutorial"
]
+++
{{< notice info >}}
About This Project:-
The given code is Python code. I make a calculator with the help of Python programming language. This is the second project of the Python programming series. 

Used Concepts:-
1. Functions
2. Variables
3. Datatypes
4. If-Else Statements
5. Operators
6. Type Casting

The project is divided into three parts. According to their work. 
1. Notice For User:- This part contains a notice for a user to use the calculator.
2. Variables and Data:- This part contain three variables and the number and operation provided by the user.
3. Conditions:- This part contains If-Else statements. These conditions are logic of the script.
{{< /notice >}}

Code:-
{{< tabgroup align="right" style="code" >}} {{< tab name="Python" >}}
```ruby
# 1.Notice For User
print("""\nUse 'add' for Addition.
Use 'sub' for Substraction.
Use 'multi' for Multiplication.
Use 'div' for Division.
Use 'power' for Power Calculations.\n""")

# 2.Variables And Data
x = input("Enter The 1st Number : ")
y = input("Enter The 2nd Number : ")
o = input("Enter The Operation : ")

# 3.Conditions
if (o == "add"):
    print(float(x) + float(y))

elif (o == "sub"):
    print(float(x) - float(y))

elif (o == "multi"):
    print(float(x) * float(y))

elif (o == "div"):
    print(float(x) / float(y))

elif (o == "power"):
    print(float(x) ** float(y)) 

else:
    print("Invalid Input")
```
{{< /tab >}} {{< /tabgroup >}}