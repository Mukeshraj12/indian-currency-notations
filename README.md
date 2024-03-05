# indian-currency-notations

def convert_to_indian_currency_notation(number):
    # Convert the number to a string
    num_str = str(number)

    # Calculate the length of the string
    length = len(num_str)

    # Initialize variables for result and counter
    result = ''
    count = 0

    # Iterate through each character in reverse order
    for char in reversed(num_str):
        # Add a comma after every 2 digits and reset counter
        if count == 2:
            result += ','
            count = 0

        # Append the current character to the result
        result += char
        count += 1

    # Reverse the result string to get the correct order
    result = result[::-1]

    return result

        # Get input from the user
 input_number = int(input("Enter an integer: "))

        # Convert and display the result
 output = convert_to_indian_currency_notation(input_number)
 print(f"input: {input_number}")
 print(f"output: {output}")

Sample input: 504678
Sample output: 5,04,67
