# Project README: User Info Program

## 1\. Overview

This is a four-file Python app. It's a practice activity to learn about **organizing programs** and **working with data**. The program asks for a user's name and age, checks the input, changes the data into a unique computer language (binary), and then saves and loads the final message from a text file.

The main point of this setup is to show how to use **imports** well and keep different tasks separate in their own Python files.


## 2\. What the Program Does

The app runs through these steps:

  * **User Talk:** Gives friendly hello and goodbye messages.
  * **Checking Input:** Collects data and has clear rules for checking it: the name **must not be empty**, and the age **must be a number**.
  * **Changing Data:** Turns the user's name (text) into a series of binary numbers separated by a space (like `01001000 01101001`). It turns the user's age (number) into its normal Python binary form (like `0b10111`).
  * **Managing Files:** Saves the finished message to a file named **`user_message.txt`**. Then, it reads the file's content back onto the screen to prove it saved correctly.
  * **Handling Errors:** Uses **`try...except`** code blocks to nicely deal with possible mistakes that happen when reading or saving files.

## 3\. Project Structure (Breaking it into Parts)

The program is split into four files. This makes sure that similar jobs are grouped together, which makes the code easier to handle, test, and use again.

| File Name | Job (The Team) | Main Tasks (Key Functions) |
| :--- | :--- | :--- |
| **`main_program.py`** | **The Manager (Boss)** | `get_user_info()`: Runs the program steps and tells all the other functions what to do. |
| **`helper_functions.py`** | **The Work (Worker)** | `validate_input()`, `convert_to_binary()`, `create_message()` |
| **`file_manager.py`** | **The Records (Secretary)** | `save_message()`, `read_message()` (includes error handling for files). |
| **`greetings.py`** | **The Welcome (Receptionist)** | `show_intro()`, `show_exit_message()` |

## 4\. How to Start the Program

1.  **Needed Things:** You must have Python 3 installed and working on your computer.
2.  **Setup:** Make sure all four Python files are in the **same folder** (`main_program.py`, `helper_functions.py`, `file_manager.py`, and `greetings.py`).
3.  **Run It:** Open your terminal or command line, go to the project folder, and run the main file:

<!-- end list -->

```bash
python3 main_program.py
```

4.  **Use It:** The program will ask you for your name and age. It will keep asking until you give it correct input for both.


## 5\. Main Things You Learn

This project helps you practice these basic programming ideas:

  * **Making and Using Functions:** Writing functions that need inputs (parameters) and calling them with the right information (arguments).
  * **Modular Programming:** Understanding the **`from X import Y`** command and why it's good to break your code into smaller files.
  * **Repeating Actions and Checking Data:** Using **`while True`** loops with **`break`** to force the user to give valid input before moving on.
  * **Text Formatting:** Using special f-strings and character tools (`ord()`, `format()`) to change data in specific ways.
