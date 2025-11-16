# python-calculator-internship
def ask_operation():                #function define
    print("welcome to multi operator calculator")                      
    print("choose a type of operation:")
    print("1.arithmetic")
    print("2.comparison")
    print("3.logical")
    choice = input("enter your choice (1/2/3):")    #asking user to choice operation
    return choice
def arithmetic_operator(a,b,operator):        #function define
    if operator == '+':                       #using control flow statement
        return a + b
    elif operator == '-':
        return a - b
    elif operator == '*':
        return a * b
    elif operator == '/':
        return a / b 
    else:
        return "invalid operator"
def comparison_operator(a,b,operator):        # function define
    if operator == '==':                      #using control flow statement
        return a == b
    elif operator == '>':
        return a > b
    elif operator == '<':
        return a < b
    elif operator == '>=':
        return a >= b
    elif operator == '<=':
        return a <= b
    else:
        return "invalid comparison operator"
def logical_operator(a,b,operator):             #function define
    if operator == 'and':                       #using control flow statement
        return a and b
    elif operator == 'or':
        return a or b
    elif operator == 'not':
        return not a
    else:
        return "invalid logical operator"
choice = ask_operation()                    # Function Calling
if choice == '1':       #arithmetic operator
   a = int(input("enter first number: "))        #asking user to takr two numbers and operator
   b = int(input("enter a second number: "))
   operator = input("enter a operator (+, -, *, /, %, //): ")
   result = arithmetic_operator(a,b,operator)      #calling arithmetic operator
   print("result:", result)
elif choice == '2':      #comparison opetaor
    a = int(input("enter a first number: "))           #asking user to take two numbers and operator
    b = int(input("enter a second number: "))
    operator = input("enter a operator (==,!=, <, >, <=, >=): ")
    result = comparison_operator(a, b, operator)    #calling comparison operator
    print("result:",result)
elif choice == '3':     #logical operator
    a = int(input("enter a first number: "))            #asking user to take two numbers and operator
    b = int(input("enter a second number: "))                           
    operator = input("enter a logical operator (and, or, not): ")   
    result = logical_operator(a, b, operator)        #calling logical operator
    print("result:",result)
else:
    print("invalid choice")
