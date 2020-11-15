# Building a Calculator Using Functions

This small project will be a demonstration on using the power of functions to build an effective calculator that can perform simple math equations quickly.

### 1.) Arithmetic Functions

Addition Function


```python
def add(num1, num2):
    return num1 + num2
```

Subtraction Function


```python
def subtract(num1, num2):
    return num1 - num2
```

Multiplication Function


```python
def multiply(num1, num2):
    return num1 * num2
```

Division Function


```python
def divide(num1, num2):
    return num1 / num2
```

### 2.) Create Command Line Interface


```python
# Print menu 
print('Please select operation -\n' \
        '1. Add\n' \
        '2. Subtract\n' \
        '3. Multiply\n' \
        '4. Divide\n')
 
select = input('Select operations from 1, 2, 3, 4 :')
 
number_1 = int(input('Enter first number: '))
number_2 = int(input('Enter second number: '))

# Based on the operation, pass the numbers to function
# Print the output
if select == '1':
    print(number_1, '+', number_2, '=',
                    add(number_1, number_2))
 
elif select == '2':
    print(number_1, '-', number_2, '=',
                    subtract(number_1, number_2))
 
elif select == '3':
    print(number_1, '*', number_2, '=',
                    multiply(number_1, number_2))
 
elif select == '4':
    print(number_1, '/', number_2, '=',
                    divide(number_1, number_2))
# Print 'Invalid input' if an unexpected character is seen in input
else:
    print('Invalid input')
```

    Please select operation -
    1. Add
    2. Subtract
    3. Multiply
    4. Divide
    
    Select operations from 1, 2, 3, 4 :4
    Enter first number: 4
    Enter second number: 5
    4 / 5 = 0.8


### 3.) Use a `while` loop to add "continue" ability


```python
cont = 'y'

# Check for input after each iteration
while cont == 'y':

        # Run code from previous step
        
        select = input('Select operations from 1, 2, 3, 4 :')
     
        number_1 = int(input('Enter first number: '))
        number_2 = int(input('Enter second number: '))
 
        if select == '1':
            print(number_1, '+', number_2, '=',
                    add(number_1, number_2))
 
        elif select == '2':
            print(number_1, '-', number_2, '=',
                    subtract(number_1, number_2))
 
        elif select == '3':
            print(number_1, '*', number_2, '=',
                    multiply(number_1, number_2))
 
        elif select == '4':
            print(number_1, '/', number_2, '=',
                    divide(number_1, number_2))
            
        #Ask user for input if he/she wants to repeat 
        
        cont = input('Continue? y/n:')
        if cont == 'n':
            break
```

    Select operations from 1, 2, 3, 4 :1
    Enter first number: 5
    Enter second number: 6
    5 + 6 = 11
    Continue? y/n:y
    Select operations from 1, 2, 3, 4 :2
    Enter first number: 7
    Enter second number: 6
    7 - 6 = 1
    Continue? y/n:n

