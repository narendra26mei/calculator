# calculator
a simple calculator
# Simple Calculator in Python

while True:
    print("\n===== PYTHON CALCULATOR =====")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Modulus")
    print("6. Power")
    print("7. Exit")

    choice = input("Enter your choice (1-7): ")

    if choice == "7":
        print("Thank you for using the calculator!")
        break

    if choice in ["1", "2", "3", "4", "5", "6"]:
        try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))

            if choice == "1":
                result = num1 + num2
                print("Result =", result)

            elif choice == "2":
                result = num1 - num2
                print("Result =", result)

            elif choice == "3":
                result = num1 * num2
                print("Result =", result)

            elif choice == "4":
                if num2 == 0:
                    print("Error: Cannot divide by zero.")
                else:
                    result = num1 / num2
                    print("Result =", result)

            elif choice == "5":
                if num2 == 0:
                    print("Error: Cannot find modulus with zero.")
                else:
                    result = num1 % num2
                    print("Result =", result)

            elif choice == "6":
                result = num1 ** num2
                print("Result =", result)

        except ValueError:
            print("Invalid input! Please enter numbers only.")

    else:
        print("Invalid choice! Please select 1 to 7.")