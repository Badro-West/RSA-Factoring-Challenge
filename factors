import sys

def factorize(number):
    for i in range(2, number):
        if number % i == 0:
            return f"{number}={i}*{number // i}"
    return f"{number}={number}*1"

if len(sys.argv) != 2:
    print("Usage: factors <file>")
    sys.exit(1)

input_file = sys.argv[1]

try:
    with open(input_file, 'r') as file:
        lines = file.read().splitlines()
except FileNotFoundError:
    print(f"File '{input_file}' not found.")
    sys.exit(1)

for line in lines:
    try:
        number = int(line)
        if number <= 1:
            print(f"Skipping invalid number: {number}")
        else:
            result = factorize(number)
            print(result)
    except ValueError:
        print(f"Skipping invalid input: {line}")


