# pythonwk3
def calculate_discount(price, discount_percent):
    """
    :param price: (float) The original price of the item.
    :param discount_percent: (float) The discount percentage applied.
    :return: (float) The final price after applying the discount (if applicable).
    """

    # Check if the discount percentage is 20% or higher
    if discount_percent >= 20:
        # Calculate the discount amount by taking the given percentage of the price
        discount_amount = (discount_percent / 100) * price

        # Subtract the discount amount from the original price to get the final price
        final_price = price - discount_amount

        # Return the discounted price
        return final_price
    else:
        # If the discount is less than 20%, return the original price with no discount applied
        return price


# Prompting the user for the original price of the item
price = float(input("Enter the original price of the item: "))  
# Convert the input from string to float to allow calculations

# Prompting the user for the discount percentage
discount_percent = float(input("Enter the discount percentage: "))  

# Call the function with user inputs and store the result
final_price = calculate_discount(price, discount_percent)

# Display the result to the user
if discount_percent >= 20:
    # If the discount was applied, show the new price after discount
    print(f"The final price after {discount_percent}% discount is: ${final_price:.2f}")
else:
    # If no discount was applied, simply display the original price
    print(f"No discount applied. The original price is: ${price:.2f}")
