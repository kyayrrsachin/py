Q5----------------------------------------------
---Sales per week

sales_per_week = [15000, 20000, 25000, 30000]

-- Calculate total sales

total_sales = sum(sales_per_week)

-- Calculate commission
c
ommission = total_sales * 0.05 if total_sales >= 50000 else 0

-- Determine remarks

if total_sales >= 80000:
    
    remarks = "Excellent"

elif total_sales >= 60000:
   
    remarks = "Good"

elif total_sales >= 40000:
  
    remarks = "Average"

else:
  
    remarks = "Work Hard"

-- Output results

print("Total Sales:", total_sales)

print("Commission:", commission)

print("Remarks:", remarks)

---------------------Q6

num = int(input("Enter a number to compute its factorial: "))

if num < 0:
   
    print("Factorial is not defined for negative numbers.")

else:
    
    result = 1
    
    for i in range(1, num + 1):
        
        result *= i
   
    print("Factorial of", num, "is:", result)

Q7--------------------------

n = int(input("enter the nth term: "))

-- Initialize the first two terms

a, b = 0, 1

-- Calculate the Fibonacci sequence up to the nth term

for _ in range(n - 1):
   
    a, b = b, a + b

--Print the nth term

print(f"The {n}th term of the Fibonacci sequence is:", b)



Q8----------------------------------------
--Input number

number = 12345

-- Calculate reverse of the number

reverse = int(str(number)[::-1])

-- Calculate sum of digits

digit_sum = sum(int(digit) for digit in str(number))

-- Output results

print("Original number:", number)

print("Reverse:", reverse)

print("Sum of digits:", digit_sum)



Q9-----------------------------

import math

-- Input numbers

num1 = 12

num2 = 15

-- Calculate LCM

lcm = (num1 * num2) // math.gcd(num1, num2)

--Calculate HCF

hcf = math.gcd(num1, num2)

 --Output results

print("Least Common Multiple:", lcm)

print("Highest Common Factor:", hcf)


Q10------------------------------------

number = 17

if number <= 1:
    
    print(number, "is not a prime number")

else:
    
    prime = True
    
    for i in range(2, int(number**0.5) + 1):
        
        if number % i == 0:
            
            prime = False
           
            break
   
    if prime:
        
        print(number, "is a prime number")
   
    else:
       
        print(number, "is not a prime number")

----------------------Q-11

import math 

def series(x,n):
    sum= 1
    term= 1
    y=2

    for i in range(1,n): 
        fct= 1
        for j in range(1,y+1):
            fct= fct*j

        term= term*(-1)
        m=term*math.pow(x,y)/fct
        sum=sum+m
 
    return sum

x= 9
n=10
print('%.4f'% series(x,n))

-------------------------Q-12

str1= input("enter the first string: ")
str2= input("enter the first string: ")


match_count = 0


for char in str1:
    if char in str2:
        match_count +=1

print("number of matching characters:", match_count)

----------------------------------Q-13

string= input("enter a string: ")

print("reversed string: ",string[::-1])

---------------------------------Q-14

string= input("enter a string: ")

if string == string[::-1]:
    print("the string is palindrome")
else:
    print("the string is not a palindrome")

--------------------------Q-15

def matrix_operation(matrix1, matrix2, operation):
    if len(matrix1) != len(matrix2) or len(matrix1[0]) != len(matrix2[0]):
        return "Matrices are not compatible for the operation"
    
    result = []
    for i in range(len(matrix1)):
        row = []
        for j in range(len(matrix1[0])):
            row.append(operation(matrix1[i][j], matrix2[i][j]))
        result.append(row)
    
    return result

# Example matrices
matrix_a = [[1, 2, 3],
            [4, 5, 6],
            [7, 8 ,9]]
            
matrix_b = [[9,8,7],
            [6,5,4],
            [3,2,1]]

# Calculate and print sum
print("Sum of matrices:")
print(matrix_operation(matrix_a, matrix_b, lambda x, y: x + y))

# Calculate and print product
print("\nProduct of matrices:")
print(matrix_operation(matrix_a, matrix_b, lambda x, y: x * y))





