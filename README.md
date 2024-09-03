# calculator-in-python
# a simple calculator but result is only printed after = is input
# easy calculator tested lmk if u find any errors ,my first repostires
def addition(num1, num2):
    return num1 + num2


def subtraction(num1, num2):
    return num1 - num2


def multiplication(num1, num2):
    return num1 * num2


def division(num1, num2):
    if num2 == 0:
        return "Error: Division by zero is not allowed."
    return num1 / num2


    while True:
        try:
            print("Enter the first number:")
            numb1 = float(input("> "))
            break
        except ValueError:
            print("Invalid input. Please enter a numeric value.

    while True:
        print(" + \n - \n x \n / \n =")
        ari_operation = input("> ").strip().lower()

        if ari_operation == "=":
            print(f"Result: {numb1}")
            break

        try:
            print("Enter the next number:")
            numb2 = float(input("> "))
        except ValueError:
            print("Invalid input. Please enter a numeric value.")
            continue

        if ari_operation == "+":
            numb1 = addition(numb1, numb2)
        elif ari_operation == "-":
            numb1 = subtraction(numb1, numb2)
        elif ari_operation == "x":
            numb1 = multiplication(numb1, numb2)
        elif ari_operation == "/":
            result = division(numb1, numb2)
            if isinstance(result, str):
                print(result)
            else:
                numb1 = result
        else:
            print("Invalid operation. Please choose from +, -, x, or /.")
