# Quiz—— Recursion and Running from the Command line

## Group 1 (Yuyang Han,Xinyi Wang,Yue Shen)

### Question1

What is the output of this code?

def squarer(n):

   if n == 1:
   
       return 2
      
   else:
   
       return squarer(n+1) ** 2 + n

squarer(2)

A.4

B.5

C.6

D.7

Correct Answer: D

When squarer(2) is called, the function will first check the value of n:

n is not equal to 1, so the function will call squarer(n+1) with n+1 = 3.
Now, the inner call to squarer(3) will take place. Again, n is not equal to 1, so the function will call squarer(n+1) with n+1 = 4.
This process will continue, with squarer(n+1) being called repeatedly until n+1 is equal to 1.
When squarer(1) is called, the function checks if n is equal to 1. In this case, it is, so the function returns 2.
Now, the outer call to squarer(2) can continue with the result of the inner call: 2 ** 2 + 3, which evaluates to 7.
Therefore, the output of the code is 7.
So the output of the code when squarer(2) is called is 7.


### Question2
Find the output of the code given below?

s = 0

def sumArray(arr,num):

    for i in range(len(arr)):

        if i == len(arr)-1:

            return num+arr[i]

        else:

            return sumArray(arr[i+1:],num+arr[i])

 

arr = [1,2,0,3,5]

print(sumArray(arr,s))

A.2

B.12035

C.11

D.None of these

Correct Answer: C

The output of the code will be 11.

The function sumArray() takes two parameters, an array arr and a number num. It iterates through the array and recursively calls itself with a slice of the array starting from the next index and the sum of the current number and num.

In the given example, the function is called with the array [1, 2, 0, 3, 5] and initial sum s = 0.

In the first call, it adds the first element 1 to s = 0 and calls the function with the array slice [2, 0, 3, 5] and sum num = 1.

In the second call, it adds the first element 2 to the current sum num = 1 and calls the function with the array slice [0, 3, 5] and sum num = 3.

In the third call, it adds the first element 0 to the current sum num = 3 and calls the function with the array slice [3, 5] and sum num = 3.

In the fourth call, it adds the first element 3 to the current sum num = 3 and calls the function with the array slice [5] and sum num = 6.

In the final call, it adds the only element 5 to the current sum num = 6 and returns the sum 11, which is printed by the print() statement outside the function.

### Question3
How many times does 5 appear in the output of the code given below?
 

def matrix(n):

    if n==1:

        print(“1”)

    else:

        for i in range(1,n):

            print(i,end=” “)

        print()

        matrix(n-1)

 

matrix(5)

A.5

B.3

C.2

D.0

Correct Answer:D

There are no occurrences of the number 5 in the output of the given code. The output consists of several lines, each with increasing numbers from 1 up to the line number minus 1. Here is the full output:

1

1 2

1 2 3

1 2 3 4
