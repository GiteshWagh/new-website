+++
authors= "Gitesh Wagh"
title = " Match Cases - Python Tutorials For Beginners #7"
date = "2023-07-06"
categories = "Python Programming"
tags = [
  "Programming", 
  "Coding",
  "python",
  "PythonTutorial"
]
+++
{{< notice question >}}
# What is If-Else statement ?
Match Cases is a method for writing conditions in Python programming. Here, We create conditions related to the value of a variable. In If-Else statements, we define the condition with the help of conditional operators. But, Here, In Match Cases the value of the variable is a condition. In Match Cases we write, What will happen when the value of a variable is 1,  2, 3, etc... This is only for example you will create a condition on any value of variable.

```ruby

                  Methods For Creating Conditions
                               |
                               |
      | ---------------------------------------------|
      |                                              |
      |                                              |
      |                                              |
If-Else Statements                               Match Cases
                    
```
{{< /notice >}}

```ruby
# Conditions
# Match cases in python

# Methods of writing condition :- 1] If-Else Statement
#                                 2] Match Cases 

x = input("Enter the number : ")
# variable x with input system

match x:
    # Condition 1
    case '1':
        print("The value is 1")

    # Condition 2
    case '2':
        print("The value is 2")

    # Condition 3
    case '3':
        print("The value is 3")

    # Condition 4
    case '4':
        print("The value is 4")

    # Else Condition
    case _:
        print("other value")
```

*********************
# Watch Video Tutorial On Youtube:-
{{< youtube A-WbED_fMtY >}}
