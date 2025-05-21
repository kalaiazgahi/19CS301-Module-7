# 19CS301-Module-7

EX: 7.1   Recursion 

### AIM: 

To write a Python program to find N^P using recursion (without using the ** operator).

### ALGORITHM:
Step1: Start.

Step 2: Define a recursive function power(base, exponent).

Step3: If exponent is 0, return 1 (base case).

Step 4: Otherwise, return base * power(base, exponent - 1).

Step 5: Read base and exponent as input.

Step 6:Call the recursive function and print the result.

Step 7:Stop.

### PROGRAM:
```
a=int(input())
b=int(input())
def power(a,b):
	if b==0:
		return 1
	elif a==0:
		return 0
	elif b==1:
		return a
	else:
		return a*power(a,b-1)
print(a,"Power",b,":",power(a,b))
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/229c7eb3-e15b-44ae-9c92-85ab71194560)


### RESULT: 

The program successfully calculates N^P using recursion and displays the correct result without using the ** operator.

EXP.No: 7.b Types of Recursion

### AIM: 

To implement indirect recursion to encode an integer to binary, transmit it, decode it back to integer, and repeat the process in decreasing order.

###ALGORITHM:
Step 1: Start

Step 2: Read the number of student names and input them into a list.

Step 3: Sort the list of names alphabetically.

Step 4: Define a recursive function binary_search_recursive(list, left, right, target).

Step 5: In the function, if left > right, return 0 (not found).

Step 6: Find the middle index. 
        
Step 7: Call the recursive function and display the result.

Step 8: Stop

### PROGRAM:
```
def encode(n):
    if(n>0):
        print("Encode", bin(n))
        transmit(n-0)
    else:
        return 0

def transmit(n):
    if(n>0):
        print("Transmit",bin(n))
        decode(n-0)
    else:
        return 0
def decode(n):
    if(n>0):
        print("Decode", n)
        encode(n-1)
    else:
        return 0
n=int(input())      
encode(n)
```
###OUTPUT:


![image](https://github.com/user-attachments/assets/9fe46c9c-7c07-45f6-90dd-171d99fd6b43)

###RESULT: 

The program successfully encodes, transmits, and decodes numbers in decreasing order using indirect recursion until it reaches zero.

EX: 7.3 Taylor Series

### AIM: 

To write a Python program to evaluate sinh(x) for n terms using recursion.

### ALGORITHM:

Step 1: Start

Step 2: Read the values of x and n (number of terms)

Step 3: Define a recursive function to calculate factorial

Step 4: Define a recursive function to calculate sinh(x) using the formula:
        sinh(x) = x + x^3/3! + x^5/5! + ... up to n terms

Step 5: Use recursion to sum the terms

Step 6: Display the result

Step 7: Stop

### PROGRAM:


```from abc import ABC
def fact(i):
    if i==1 or i==0:
        return 1
    else:
        return i*fact(i-1)
def sinh(x,n):
    if n==0:
        return  x
    else:
        return(((pow(x,(2*n+1)))/(fact(2*n+1))) + sinh(x,n-1))
x=int(input())
n=int(input())
print(sinh(x,n))
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/31949ea9-5669-4e83-bb5e-fa4dc7de7aff)


### RESULT: 

The program successfully evaluates sinh(x) using recursion and displays the result up to n terms using the Taylor series expansion.


EXP.No: 7.4   Advance Recursion Problems


### AIM:

To solve the Tower of Hanoi puzzle recursively by moving n disks from peg A to peg C using peg B as auxiliary, following the rules of the game.



###ALGORITHM: 

Step 1: If there is only 1 disk, move it from source to destination.

Step 2: Otherwise, recursively move n-1 disks from source to auxiliary peg.

Step 3: Move the nth (largest) disk from source to destination peg.

Step 4: Recursively move the n-1 disks from auxiliary to destination peg.

###PROGRAM:
```
def TowerofHanoi(n,source,destination,auxiliary ):
	if n==1:
		print ("Move disk 1 from source",source,"to destination",destination)
		return
	TowerofHanoi(n-1,source,auxiliary,destination)
	print ("Move disk",n,"from source",source,"to destination",destination)
	TowerofHanoi(n-1,auxiliary,destination,source)

```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/8d015ee9-2f2d-4bf9-8f47-f05746facb34)


 

### RESULT: 

The program successfully moves all disks from peg A to peg C following the Tower of Hanoi rules, displaying each valid move step-by-step.

EXP.No: 7.5   ASSESSMENT EXAM -VII -SEB


### AIM:

To write a Python program to calculate the sum of factorials from 1! to n! using recursion.

###ALGORITHM: 

Step 1: Start

Step 2: Read input n

Step 3: Define a recursive function factorial(n):

Step 4: Define a recursive function sum_factorials(n):

Step 5: Call sum_factorials(n) and print the result

Step 6: Stop


###PROGRAM:
```
def func(n):
    if n==0:
        return 1
    else:
        return n*func(n-1)
n=int(input())
sum=0
for i in range(1,n+1):
    sum+=func(i)
print(sum)

```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/7c8a3baa-9242-4a55-ab5a-44d29845aa8a)

 

### RESULT: 

The program successfully calculates the sum of factorials from 1 to n using recursion.





