# Project README: User Info Program

## 1. Overview

This is a four-file Python application designed as an exercise in **modular programming** and **data handling**. The program collects a user's name and age, validates the input, performs a unique conversion into binary format, and then saves and retrieves a personalized message from a text file.

The primary goal of this structure is to demonstrate effective use of imports and separation of concerns by isolating different tasks into dedicated Python files.

## 2. Features

The application executes the following sequence of operations:

  * **User Interface:** Provides friendly welcome and exit messages.
  * **Input Handling:** Collects and enforces strict validation rules for both name (must not be empty) and age (must be a valid number).
  * **Data Conversion:** Converts the user's name (text) into a space-separated ASCII binary string (e.g., `01001000 01101001`). Converts the user's age (number) into its native Python binary representation (e.g., `0b10111`).
  * **File Management:** Saves the combined message to a file named `user_message.txt` and then reads the contents back to the console to confirm successful saving.
  * **Error Handling:** Uses `try...except` blocks to gracefully manage potential errors during file operations and input validation.

## 3. Project Structure (The Modular Approach)

The program is divided into four distinct files. This organization ensures that functions are grouped by their responsibility, making the code easier to manage, test, and reuse.

| File Name | Role (The Department) | Key Functions |
| :--- | :--- | :--- |
| **`main_program.py`** | **The Controller (Boss)** | `get_user_info()`: Manages program flow and orchestrates all function calls. |
| **`helper_functions.py`** | **The Logic (Worker)** | `validate_input()`, `convert_to_binary()`, `create_message()` |
| **`file_manager.py`** | **The I/O (Secretary)** | `save_message()`, `read_message()` (includes `try/except` for file errors). |
| **`greetings.py`** | **The UX (Receptionist)** | `show_intro()`, `show_exit_message()` |

## 4. How to Run the Program

1.  **Prerequisites:** You must have a working Python 3 environment installed.
2.  **Setup:** Ensure all four Python files (`main_program.py`, `helper_functions.py`, `file_manager.py`, and `greetings.py`) are located in the **same directory**.
3.  **Execution:** Open your terminal or command prompt, navigate to the project directory, and run the main file:

<!-- end list -->

```bash
python3 main_program.py
```

4.  **Interaction:** The program will prompt you for your name and age. It will continue looping until valid input is provided for both fields.

## 5. Key Learning Outcomes

This project reinforces several fundamental programming concepts:

  * **Function Definition and Call:** Correctly defining functions with parameters and calling them with appropriate arguments.
  * **Modular Programming:** Understanding the `from X import Y` mechanism and why breaking code into modules is beneficial.
  * **Looping and Validation:** Using `while True` loops with `break` to force continuous input until validation criteria are met.
  * **String Formatting:** Using f-strings and character manipulation (`ord()`, `format()`) to achieve specific data transformation requirements.

Would you like me to help you start writing the code for the **`file_manager.py`** functions, which need to handle file saving and reading with `try/except` blocks?
