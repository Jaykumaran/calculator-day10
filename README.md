# calculator-day10
print('''
 _____________________
|  _________________  |
| |              0. | |
| |_________________| |
|  ___ ___ ___   ___  |
| | 7 | 8 | 9 | | + | |
| |___|___|___| |___| |
| | 4 | 5 | 6 | | - | |
| |___|___|___| |___| |
| | 1 | 2 | 3 | | x | |
| |___|___|___| |___| |
| | . | 0 | = | | / | |
| |___|___|___| |___| |
|_____________________|

Welcome to Calculator

''')


def add(n1,n2):
  return n1+n2
def subtract(n1,n2):
  
  return n1-n2
def multiply(n1,n2):
  return n1*n2
def divide(n1,n2):
  return n1/n2
operation={"+":add,"-":subtract,"*":multiply,"/":divide}
def calculator():
  n1=float(input("enter first number:"))
  for symbol in operation:
    print(symbol)
  should_continue=True
  while should_continue:
    operation_symbol=input("pick an operation: ")
    n2=float(input("enter next number: "))
    calculation_func=operation[operation_symbol]
    answer= calculation_func(n1,n2)
    print(f"your answer is {answer} ")
   
    input1=input("should continue calculation with previous answer.type 'y'or 'n' ")
    if input1=="y":
      n1=answer
    else:
      should_continue=False
      print(answer)
      calculator()
calculator()
    
    OUTPUT:

 _____________________
|  _________________  |
| |              0. | |
| |_________________| |
|  ___ ___ ___   ___  |
| | 7 | 8 | 9 | | + | |
| |___|___|___| |___| |
| | 4 | 5 | 6 | | - | |
| |___|___|___| |___| |
| | 1 | 2 | 3 | | x | |
| |___|___|___| |___| |
| | . | 0 | = | | / | |
| |___|___|___| |___| |
|_____________________|

Welcome to Calculator


enter first number:4.5
+
-
*
/
pick an operation: /
enter next number: 2
your answer is 2.25
