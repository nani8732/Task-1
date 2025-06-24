# Task-1
#Calculator.py
#Calculator
def add(a,b):
    return a+b
def subtract(a,b):
    return a-b
def multiply(a,b):
    return a*b
def divide(a,b):
    if(b==0):
        return "Error : Division by zero!"
    else:
        return a/b
def calculator():
    print("Welcome to CLI Calculator!")
    while True:
        print("\nSelect Operation")
        print("\n1.Addition")
        print("\n2.Subtraction")
        print("\n3.Multiplication")
        print("\n4.Division")
        print("\n5.Exit")
        choice=input("Enter your choice(1-5):")
        if choice == '5':
            print("Exiting calculator. Goodbye!")
            break
        if choice in ['1', '2', '3', '4']:
            try:
                num1 = float(input("Enter first number: "))
                num2 = float(input("Enter second number: "))
            except ValueError:
                print("Invalid input! Please enter numbers.")
                continue
            if choice=='1':
                print("Result:",add(num1,num2))
            elif choice=='2':
                print("Result:",subtract(num1,num2))
            elif choice=='3':
                print("Result:",multiply(num1,num2))
            elif choice=='4':
                print("Result:",divide(num1,num2))
        else:
            print("Invalid choice. Please select a valid option.")

if __name__ == "__main__":
    calculator()
