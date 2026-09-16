# project7
A simple Python toolkit for daily tasks like date-time, math, random generation, and conversions. It uses a menu-driven interface for quick and easy use.


# 🧰 Multi-Utility Toolkit – Python Modules & Packages Project

A practical **Python Multi-Utility Toolkit** that demonstrates how to organize reusable functionality into separate modules and packages.

This project combines several Python utilities for:

* 📅 Date & Time
* ⏱️ Stopwatch & Countdown
* 🧮 Mathematical Operations
* 💰 Compound Interest
* 📐 Area Calculation
* 🎲 Random Number Generation
* 🔐 Random Password Generation
* 🎯 Random Sampling
* 🔢 OTP Generation
* 🆔 UUID Generation
* 📁 File Handling
* 🌡️ Unit Conversion
* 🔢 Advanced Mathematical Operations

The project is designed around multiple Python files, making it useful for understanding **modular programming, functions, packages, imports, and code reusability**.

---

# 📌 Project Overview

The project creates a menu-driven application called:

```text
Multi-Utility Toolkit
```

Users can select different utilities from the menu.

### Main Workflow

```text
                    Multi-Utility Toolkit
                            │
        ┌───────────────────┼───────────────────┐
        ↓                   ↓                   ↓
   Date & Time            Math               Random
        │                   │                   │
   Date Difference     Basic Operations    Password
   Stopwatch           Advanced Math       Random Number
   Countdown            Interest           Random List
                       Circle Area          OTP
        │
        ├───────────────┐
        ↓               ↓
      UUID          File Handling
        │               │
        └───────┬───────┘
                ↓
        Unit Conversions
```

---

# 🎯 Project Objectives

The main objectives of this project are:

1. Understand Python modules.
2. Understand Python packages.
3. Create reusable functions.
4. Work with built-in Python libraries.
5. Practice date and time operations.
6. Perform mathematical calculations.
7. Generate random values.
8. Generate UUIDs.
9. Work with text files.
10. Perform unit conversions.
11. Create a menu-driven Python application.
12. Understand modular project organization.

---

# 🛠️ Technologies Used

| Technology / Module | Purpose                                |
| ------------------- | -------------------------------------- |
| 🐍 Python           | Main programming language              |
| `datetime`          | Date and time operations               |
| `time`              | Delays, stopwatch and countdown        |
| `math`              | Mathematical calculations              |
| `random`            | Random numbers, passwords and sampling |
| `uuid`              | Unique identifier generation           |
| File Handling       | Saving data to text files              |
| Custom Modules      | Reusable project utilities             |
| Custom Package      | Organizing related functions           |

---

# 📂 Project Structure

```text
Multi-Utility-Toolkit/
│
├── main.py
│
├── datetime_utils.py
├── math_utils.py
├── random_utils.py
├── uuid_utils.py
├── file_utils.py
│
├── mypackage/
│   ├── conversions.py
│   └── advanced_math.py
│
└── output.txt
```

### File Responsibilities

| File                         | Purpose                             |
| ---------------------------- | ----------------------------------- |
| `main.py`                    | Main menu and application execution |
| `datetime_utils.py`          | Date/time utilities                 |
| `math_utils.py`              | Mathematical utilities              |
| `random_utils.py`            | Random value generation             |
| `uuid_utils.py`              | UUID generation                     |
| `file_utils.py`              | File saving functionality           |
| `mypackage/conversions.py`   | Unit conversions                    |
| `mypackage/advanced_math.py` | Square and cube calculations        |
| `output.txt`                 | Stores user-entered data            |

---

# 📅 1. Date & Time Utilities

The `datetime_utils.py` module provides functions for working with dates and time.

```python
import datetime
import time
```

---

## 🕐 Current Date & Time

Function:

```python
def show_current_datetime():
    return datetime.datetime.now().strftime(
        "%Y-%m-%d %H:%M:%S"
    )
```

This returns the current date and time in the format:

```text
YYYY-MM-DD HH:MM:SS
```

Example:

```text
2026-09-16 10:30:45
```

---

# 📆 2. Date Difference

Function:

```python
def date_difference(date1, date2):
```

The function accepts dates in:

```text
YYYY-MM-DD
```

format.

It converts strings into datetime objects:

```python
d1 = datetime.datetime.strptime(
    date1,
    "%Y-%m-%d"
)
```

Then calculates the difference:

```python
abs((d2 - d1).days)
```

### Example

```text
Date 1: 2026-01-01
Date 2: 2026-01-10

Difference: 9 days
```

The use of `abs()` ensures the returned difference is positive.

---

# 📅 3. Date Formatting

Function:

```python
def format_date(
    date,
    format_str="%d-%m-%Y"
):
    return date.strftime(format_str)
```

This converts a datetime object into a specified string format.

Default format:

```text
DD-MM-YYYY
```

---

# ⏱️ 4. Stopwatch

Function:

```python
def stopwatch(seconds=5):
```

The function:

1. Prints that the stopwatch has started.
2. Waits for the specified number of seconds.
3. Prints that the stopwatch has ended.

Implementation:

```python
time.sleep(seconds)
```

Example:

```text
Stopwatch started...
[wait]
Stopwatch ended!
```

---

# ⏳ 5. Countdown

Function:

```python
def countdown(seconds=5):
```

The countdown prints each remaining second and waits one second between values.

Example:

```text
5
4
3
2
1
Time’s up!
```

This demonstrates:

* `while` loop
* `time.sleep()`
* Variable decrement

---

# 🧮 6. Mathematical Utilities

The `math_utils.py` module uses Python's `math` library:

```python
import math
```

It contains several mathematical functions.

---

# ➕ 7. Basic Mathematical Operations

Function:

```python
def basic_operations(a, b):
```

It returns a dictionary containing:

```text
Sum
Difference
Product
Division
```

Implementation:

```python
{
    "sum": a+b,
    "diff": a-b,
    "product": a*b,
    "division": a/b
}
```

Example:

```text
a = 10
b = 5
```

Result:

```text
sum       → 15
diff      → 5
product   → 50
division  → 2
```

---

# 📐 8. Advanced Mathematical Operations

Function:

```python
def advanced_operations(x):
```

The function calculates:

* Sine
* Cosine
* Logarithm
* Factorial

Using:

```python
math.sin(x)
math.cos(x)
math.log(x)
math.factorial(int(x))
```

The result is returned as a dictionary.

---

# 💰 9. Compound Interest

Function:

```python
def compound_interest(
    principal,
    rate,
    time
):
```

Formula used:

```text
Amount = Principal × (1 + Rate / 100) ^ Time
```

Python implementation:

```python
principal * (
    (1 + rate/100) ** time
)
```

This function returns the calculated amount.

---

# ⭕ 10. Circle Area

Function:

```python
def area_circle(radius):
    return math.pi * radius**2
```

Formula:

```text
Area = π × r²
```

The value of π is obtained from:

```python
math.pi
```

---

# 🎲 11. Random Utilities

The `random_utils.py` module uses:

```python
import random
```

It provides different random-generation utilities.

---

# 🔢 12. Random Number

Function:

```python
def random_number(
    start=1,
    end=100
):
```

It generates a random integer between the specified start and end values.

Uses:

```python
random.randint(start, end)
```

---

# 📋 13. Random List

Function:

```python
def random_list(size=5):
```

It creates a list containing random integers.

Example structure:

```text
[24, 81, 7, 55, 92]
```

The values are randomly generated.

---

# 🔐 14. Random Password

Function:

```python
def random_password(length=8):
```

The function creates a random password using:

* Lowercase letters
* Uppercase letters
* Numbers
* Selected special characters

Character set:

```text
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
0123456789
!@#$%
```

The password length defaults to:

```text
8 characters
```

---

# 🎯 15. Random Sampling

Function:

```python
def random_sampling(
    dataset,
    k=3
):
```

It selects `k` random elements from a dataset using:

```python
random.sample(dataset, k)
```

This is useful for demonstrating random selection from existing data.

---

# 🔢 16. Random OTP

Function:

```python
def random_otp():
```

It generates a random six-digit number between:

```text
100000 – 999999
```

Implementation:

```python
random.randint(
    100000,
    999999
)
```

---

# 🆔 17. UUID Generator

The `uuid_utils.py` module uses:

```python
import uuid
```

Function:

```python
def generate_uuid():
    return str(uuid.uuid4())
```

It generates a UUID using `uuid.uuid4()`.

Example format:

```text
xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

UUIDs are useful for creating unique identifiers in applications.

---

# 📁 18. File Handling

The `file_utils.py` module contains:

```python
def save_to_file(filename, data):
```

The file is opened using:

```python
with open(filename, "a") as f:
```

The `"a"` mode means new data is appended to the existing file.

The entered data is written with a new line:

```python
f.write(data + "\n")
```

The function returns:

```text
Data saved successfully!
```

---

# 🌡️ 19. Unit Conversions

The `mypackage/conversions.py` module contains unit conversion functions.

---

## 🚗 Kilometers to Miles

```python
def km_to_miles(km):
    return km * 0.621371
```

Formula:

```text
Miles = Kilometers × 0.621371
```

Example:

```text
10 km → 6.21371 miles
```

---

## 🌡️ Celsius to Fahrenheit

```python
def celsius_to_fahrenheit(c):
    return (c * 9/5) + 32
```

Formula:

```text
°F = (°C × 9/5) + 32
```

Example:

```text
100°C → 212°F
```

---

# 🔢 20. Advanced Math Package

The `mypackage/advanced_math.py` module contains two functions.

### Square

```python
def square(n):
    return n**2
```

Formula:

```text
n²
```

### Cube

```python
def cube(n):
    return n**3
```

Formula:

```text
n³
```

---

# 🧩 21. Custom Package

The project uses a custom package:

```text
mypackage/
```

Inside the package:

```text
mypackage/
├── conversions.py
└── advanced_math.py
```

This demonstrates how related Python functions can be organized into reusable modules.

---

# 🖥️ 22. Main Menu

The application provides the following menu:

```text
--- Multi-Utility Toolkit ---

1. Show Current Date & Time
2. Date Difference
3. Math Operations
4. Generate Random Password
5. Generate UUID
6. Save Data to File
7. Unit Conversions
8. Exit
```

The user's choice is captured using:

```python
choice = input("Enter choice: ")
```

---

# 🔀 23. Menu Control

The program uses:

```python
if
elif
else
```

to determine which utility should execute.

Example:

```python
if choice == "1":
    print(show_current_datetime())
```

For invalid choices:

```python
else:
    print("Invalid choice!")
```

---

# 🔁 24. Continuous Menu

The main application runs inside:

```python
while True:
```

This keeps showing the menu until the user selects:

```text
8. Exit
```

The program then uses:

```python
break
```

to stop the loop.

---

# 🧠 25. Python Concepts Demonstrated

This project covers several important Python concepts.

### Core Python

* Variables
* Functions
* Parameters
* Return values
* Dictionaries
* Lists
* Strings
* Loops
* Conditional statements
* `while` loop
* `break`
* User input

### Modules

```text
datetime
time
math
random
uuid
```

### Custom Modules

```text
datetime_utils.py
math_utils.py
random_utils.py
uuid_utils.py
file_utils.py
```

### Custom Package

```text
mypackage/
```

### File Handling

```python
open()
with open()
write()
```

### Error Handling

The CSV/file loading concept is not used here; the provided toolkit itself does not include exception handling around the menu operations.

---

# 🔄 26. Modular Programming Concept

Instead of keeping every function in one large Python file, the project separates functionality.

```text
Date Functions
      ↓
datetime_utils.py

Math Functions
      ↓
math_utils.py

Random Functions
      ↓
random_utils.py

UUID Function
      ↓
uuid_utils.py

File Function
      ↓
file_utils.py

Conversion Functions
      ↓
mypackage/conversions.py
```

This makes the project easier to organize and reuse.

---

# ▶️ 27. How to Run the Project

## Step 1 — Install Python

Check whether Python is installed:

```bash
python --version
```

---

## Step 2 — Open the Project Folder

Make sure the project structure is maintained:

```text
Multi-Utility-Toolkit/
│
├── main.py
├── datetime_utils.py
├── math_utils.py
├── random_utils.py
├── uuid_utils.py
├── file_utils.py
└── mypackage/
    ├── conversions.py
    └── advanced_math.py
```

---

## Step 3 — Run the Main Program

Open Command Prompt or PowerShell inside the project folder and run:

```bash
python main.py
```

---

# 💻 Example Output

```text
--- Multi-Utility Toolkit ---

1. Show Current Date & Time
2. Date Difference
3. Math Operations
4. Generate Random Password
5. Generate UUID
6. Save Data to File
7. Unit Conversions
8. Exit

Enter choice: 1

2026-09-16 10:30:45
```

Another example:

```text
Enter choice: 3

{'sum': 15,
 'diff': 5,
 'product': 50,
 'division': 2.0}
```

Password example:

```text
Enter choice: 4

Password: A7@kP2#x
```

UUID example:

```text
Enter choice: 5

UUID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```

---

# 📊 Project Feature Summary

| Feature              | Module              |
| -------------------- | ------------------- |
| Current Date & Time  | `datetime_utils.py` |
| Date Difference      | `datetime_utils.py` |
| Date Formatting      | `datetime_utils.py` |
| Stopwatch            | `datetime_utils.py` |
| Countdown            | `datetime_utils.py` |
| Basic Math           | `math_utils.py`     |
| Advanced Math        | `math_utils.py`     |
| Compound Interest    | `math_utils.py`     |
| Circle Area          | `math_utils.py`     |
| Random Number        | `random_utils.py`   |
| Random List          | `random_utils.py`   |
| Random Password      | `random_utils.py`   |
| Random Sampling      | `random_utils.py`   |
| Random OTP           | `random_utils.py`   |
| UUID                 | `uuid_utils.py`     |
| File Saving          | `file_utils.py`     |
| KM → Miles           | `conversions.py`    |
| Celsius → Fahrenheit | `conversions.py`    |
| Square               | `advanced_math.py`  |
| Cube                 | `advanced_math.py`  |

---

# 🚀 Possible Future Improvements

The toolkit can be extended with:

* 📋 More mathematical functions
* 📅 More date calculations
* 🧮 Calculator menu with user-entered numbers
* 🔐 Custom password length input
* 🎲 Custom random-number ranges
* 📁 File reading functionality
* 🗂️ JSON file support
* 📊 CSV file utilities
* 🧹 Better input validation
* ⚠️ Exception handling
* 📝 Logging
* 🖥️ GUI application
* 📦 More reusable packages
* 🧪 Unit testing

---

# 🎯 Portfolio Value

This project demonstrates practical understanding of:

```text
Python
   +
Functions
   +
Modules
   +
Packages
   +
Built-in Libraries
   +
File Handling
   +
Randomization
   +
Date & Time
   +
Mathematical Operations
   +
Menu-Driven Programming
```

It is particularly useful for demonstrating **Python fundamentals, modular programming, and reusable code organization**.

---

# 🏁 Conclusion

The **Multi-Utility Toolkit** is a modular Python project that brings multiple useful utilities together in one menu-driven application.

The project demonstrates how Python's built-in modules can be combined with custom modules and packages to create a structured and reusable application.

### Core Workflow

**Create Modules → Build Functions → Organize Package → Import Utilities → Create Menu → Execute Functions**

---

## 👨‍💻 Project Type

**Python | Modules | Packages | Functions | File Handling | Date & Time | Mathematics | Random Utilities**

---

⭐ If you found this project useful, consider giving the repository a star!
