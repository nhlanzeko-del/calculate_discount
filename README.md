# Discount Calculator

A Python program that calculates the final price of an item after applying a discount, if applicable.

## Features
- Calculates discounted price for discounts of 20% or more
- Returns original price for discounts below 20%
- Interactive user input for price and discount percentage
- Clear output showing the final price

## How It Works
1. The `calculate_discount()` function:
   - Takes `price` and `discount_percent` as parameters
   - Applies discount only if 20% or higher
   - Returns the final price
2. The main program:
   - Prompts user for original price and discount percentage
   - Calls `calculate_discount()`
   - Prints the final price

## Code Example
```python
def calculate_discount(price, discount_percent):
    if discount_percent >= 20:
        return price * (1 - discount_percent/100)
    return price

original_price = float(input("Enter the original price: "))
discount = float(input("Enter the discount percentage: "))
final_price = calculate_discount(original_price, discount)

print(f"Final price: ${final_price:.2f}")
