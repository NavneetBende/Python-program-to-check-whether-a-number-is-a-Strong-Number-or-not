# Python-program-to-check-whether-a-number-is-a-Strong-Number-or-not

Check Whether or Not the Number is a Strong Number in Python
Given an integer input the objective is to check whether or not the given integer input is a Strong Number based on whether is satisfies the condition or not. Therefore, we’ll write a program to Check Whether or Not the Number is a Strong Number in Python Language.

Example
Input : 145
Output : It's a Strong Number
strong number or not in python
Check Whether or Not the Number is a Strong Number in Python Language
Given an integer input, the objective is to check whether or not the given integer input is a Strong number or not using loops and recursion. In order to do so we’ll check if the number satisfies the definition of a Strong number mentioned below

Strong Number
A Number that is equal to the sum of the factorial of it's individual digits is known as Strong Number.
Let's Try and understand it better using an example

Example
Input : 145
Output : It's a Strong Number.
Explanation : Number = 145
145 = 1! + 4! + 5!
145 = 1 + 24 + 120
as the above mentioned condition is satisfied, The given number as an example 145 , is a Strong Number .
Therefore, to solve the above mentioned problem, we have come up with few methods in Python Language. The methods are listed below,

Method 1: Using Simple Iteration
Method 2: Using Recursive Function
Let’s implement the above mentioned methods and learn about them in detail in the upcoming sections.

Check Whether or Not the Number is a Strong Number in Python

Method 1: Using Simple Iteration
Working
In this method we’ll use the concept of loops to check whether the given number is a Strong number or not. To do so we’ll break the number after extracting the last digit of the number with each iteration and keep appending the sum variable with it’s factorial. In the end we check whether or not it matches the original number.

For an integer input as the number, we perform the following

Create a List of all the factorial values from 1 to 9.
Run a While loop until temp == 0.
Extract the Last Digit using Modulo Operator.
Shorten the length of the temp using divide operator.
Append the factorial of the digit in sum variable.
Check if the Sum matches the original string.
Let’s implement the above mentioned logic in Python Language.

Python Code
Run
#Using Iteration
n =145
#save the number in another variable
temp=n
sum=0
f=[0]*10
f[0]=1
f[1]=1
for i in range(2,10): #precomputing the factorial value from 0 to 9 and store in the array.
    f[i]=f[i-1]*i

#Implementation
while(temp):
    r=temp%10 #r will have the vale u of the unit digit
    temp=temp//10
    sum+=f[r] #adding all the factorial

if(sum==n):
    print("Yes", n ,"is strong number")

else:
    print("No" , n, "is not a strong number")
Output
Yes 145 is a strong Number
Method 2: Using Recursive Function
Working
In this method we’ll use recursion to recursively iterate through recursive calls and perform the fore mentioned processes. We set the recursive step call and base case. Keeping in mind all the necessary steps, we declare a recursive function. To know more about recursion, Check out our page, Recursion in Python.

For a given integer input number, we perform the following,

Define a Function check_StrongNumber() which takes a number as an argument.
Set the base case as num == 0.
Set the step recursive call as check_StrongNumber(num//10).
Check of the returned value matches the original number.
Let’s implement the above mentioned Logic in Python Language.

Python Code
Run
#Using Recursion
def Factorial(num):
    if num<=0: return 1 else: return num*Factorial(num-1) sum=0 def check_StrongNumber(num): global sum if (num>0):
        fact = 1
        rem = num % 10
        check_StrongNumber(num // 10)
        fact = Factorial(rem)
        sum+=fact
    return sum
num=145
if (check_StrongNumber(num) == num):
    print("Yes",num,"is a strong Number.")
else:
    print("No",num,"is not a strong Number.")
Output
Yes 145 is strong number
