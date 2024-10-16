import streamlit as st
import math

# Scientific Calculator Functions
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    else:
        return x / y

def power(x, y):
    return x ** y

def sqrt(x):
    return math.sqrt(x)

def sin(x):
    return math.sin(math.radians(x))  # Convert degrees to radians

def cos(x):
    return math.cos(math.radians(x))

def tan(x):
    return math.tan(math.radians(x))

def log(x, base=10):
    if x <= 0:
        return "Error! Logarithm undefined for non-positive numbers."
    else:
        return math.log(x, base)

# Streamlit UI
st.title("Scientific Calculator")

# Select Operation
operation = st.selectbox("Select Operation", ["Add", "Subtract", "Multiply", "Divide", "Power (x^y)", "Square Root", "Sine", "Cosine", "Tangent", "Logarithm"])

# For operations with two inputs
if operation in ["Add", "Subtract", "Multiply", "Divide", "Power (x^y)"]:
    num1 = st.number_input("Enter first number", format="%.2f")
    num2 = st.number_input("Enter second number", format="%.2f")

# For operations with one input
else:
    num = st.number_input("Enter a number", format="%.2f")

# Calculate when user presses the button
if st.button("Calculate"):
    if operation == "Add":
        result = add(num1, num2)
    elif operation == "Subtract":
        result = subtract(num1, num2)
    elif operation == "Multiply":
        result = multiply(num1, num2)
    elif operation == "Divide":
        result = divide(num1, num2)
    elif operation == "Power (x^y)":
        result = power(num1, num2)
    elif operation == "Square Root":
        result = sqrt(num)
    elif operation == "Sine":
        result = sin(num)
    elif operation == "Cosine":
        result = cos(num)
    elif operation == "Tangent":
        result = tan(num)
    elif operation == "Logarithm":
        result = log(num)
    
    st.success(f"Result: {result}")
