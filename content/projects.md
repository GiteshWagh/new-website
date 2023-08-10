+++
title = "Projects"
slug = "Projects"
+++
--------

# **Project 1 : Stone-Paper-Scissor Game In Python**

```ruby

print("\nWellcom to Stone-Paper-Scissor\n")
import random
list1 = ["Stone","Paper","Scissor"]
computers_choice = random.choice(list1)
print("Choose Stone-Paper-Scissor.")
Players_Choice = input("Enter Your Choice : ")
print("computer choice :",computers_choice)

if (computers_choice == Players_Choice):
    print("!!!Tie!!!")

elif (computers_choice == "Stone" and Players_Choice == "Paper"):
    print("!!!You Won!!!")

elif (computers_choice == "Stone" and Players_Choice == "Scissor"):
    print("!!!Computer Won!!!")

elif (computers_choice == "Paper" and Players_Choice == "Stone"):
    print("!!!Computer Won!!!")

elif (computers_choice == "Paper" and Players_Choice == "Scissor"):
    print("!!!You won!!!")

elif (computers_choice == "Scissor" and Players_Choice == "Stone"):
    print("!!!You Won!!!")

elif (computers_choice == "Scissor" and Players_Choice == "Paper"):
    print("!!!Computer Won!!!")
 

```

********

# **Project 2 : Password Lock System In Python**
````ruby
print("\nSet Your Profile.")
ID = input("Enter Your ID 👉 : ")
password = input("Set The Password 👉 : ")

print("✔ Account Setup is complete ✔")

print("\nLog In Now,")
x = input("Enter ID Here 👉 : ")
y = input("Enter Passcode Here 👉 : ")

if (x == ID):
    print("Wellcome",ID,'👋,')

else:
    print("❌Invalid ID❌")

if(y==password):
    print("✔Correct password. Access Allowed✔")

else:
    print("❌Invalid Password❌")
````
********
# **Project 3 : Snake-Water-Gun Game In Python**
````ruby
import random

print("\nWellcome To Snake-Water-Gun Game !!!\n")


list1 = ["Snake", "Water","Gun"]
Computers_Choice = random.choice(list1)
print("{ Snake-Water-Gun }")
Players_Choice = input("Enter Option : ")
print(f"Computer choose : ",Computers_Choice)

if (Computers_Choice == Players_Choice):
    print("!!!Tie!!!")
   

elif (Computers_Choice == "Snake" and Players_Choice == "Water"):
    print("!!!Computer Won!!!") 

elif (Computers_Choice == "Snake" and Players_Choice == "Gun"):
    print("!!!You Won!!!")



elif (Computers_Choice == "Water" and Players_Choice == "Snake"):
    print("!!!You Won!!!") 

elif (Computers_Choice == "Water" and Players_Choice == "Gun"):
    print("!!!Computer Won!!!")


elif (Computers_Choice == "Gun" and Players_Choice == "Snake"):
    print("!!!Computer Won!!!") 

elif (Computers_Choice == "Gun" and Players_Choice == "Water"):
    print("!!!You Won!!!")

else :
    print("Invalid Input")
````
******

# **Project 4 : Calculator In Python**
````ruby
# 1. Notice For User
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
````

**************************************
