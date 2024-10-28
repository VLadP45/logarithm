# logarithmimport math

def calculate_logarithm(number, base=math.e):
    """
    Calculate the logarithm of a number to a specified base.

    Parameters:
    - number (float): The number to calculate the logarithm of (must be > 0).
    - base (float): The base of the logarithm. Default is the natural logarithm (base e).

    Returns:
    - float: The calculated logarithm.
    """
    if number <= 0:
        raise ValueError("Number must be greater than 0.")
    if base <= 0 or base == 1:
        raise ValueError("Base must be greater than 0 and not equal to 1.")
    
    return math.log(number, base)

# Example usage:
number = float(input("Enter the number: "))
base = float(input("Enter the base (default is e): "))

log_value = calculate_logarithm(number, base)
print(f"The logarithm of {number} with base {base} is: {log_value}")
