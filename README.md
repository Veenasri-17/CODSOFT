def calculator():
    print("Simple Calculator")
    print("Select an operation to perform:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")

    # Getting user input for operation
    choice = input("Enter your choice (1/2/3/4): ")

    # Validating choice
    if choice in ['1', '2', '3', '4']:
        # Taking input for numbers
        try:
            num1 = float(input("Enter the first number: "))
            num2 = float(input("Enter the second number: "))
        except ValueError:
            print("Invalid input. Please enter numeric values.")
            return

        # Performing the calculation based on the user's choice
        if choice == '1':
            result = num1 + num2
            operation = '+'
        elif choice == '2':
            result = num1 - num2
            operation = '-'
        elif choice == '3':
            result = num1 * num2
            operation = '*'
        elif choice == '4':
            if num2 == 0:
                print("Error! Division by zero.")
                return
            result = num1 / num2
            operation = '/'

        # Displaying the result
        print(f"The result of {num1} {operation} {num2} = {result}")
    else:
        print("Invalid choice. Please select a valid operation.")
calculator()
