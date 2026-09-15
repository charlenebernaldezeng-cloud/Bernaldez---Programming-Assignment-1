# ECE 2112 - Programming Assignment 1
### Name: Bernaldez, Charlene A.                                                                      
### Section: 2ECE-B

## Table of Contents
- [Overview](#overview)
- [Function Summary](#function-summary)
- [Problems & Solutions](#problem--solutions)
  - [A. Word Rotation Problem](#a-word-rotation-problem)
  - [B. Username Builder Problem](#b-username-builder-problem)
  - [C. Bookend Swap Problem](#c-bookend-swap-problem)
- [Project File Structure](#project-file-structure)
- [Requirements](requirements)
- [How to Run](#how-to-run)
  - [Using Terminal / Command Prompt](#using-terminal--command-prompt)
  - [Using Jupyter Notebook](#using-jupyter-notebook)

---

## Overview

This repository features Python-based solutions for exercises involving basic string manipulation, sequence indexing, and list unpacking, highlighting programming concepts such as:
* String slicing and indexing techniques
* Manipulating strings using built-in methods (`.lower()`, `.replace()`)
* Sequence manipulation via  list unpacking (`*` operator)
* Construction of functions returning specified results

---

## Function Summary

| Function | Input Parameters | Return Type | Key Logic |
| :--- | :--- | :--- | :--- |
| rotate_word(text) | text (str) | str | Moves index 0 to end using text[1:] + text[0] |
| make_username(first_name, last_name) | first_name (str), last_name (str) | str | Lowercases, strips spaces, joins with . |
| swap_bookends(items) | items (list) | list | Unpacks using first, *middle, last, swaps endpoints |

---

## Problems & Solutions

### A. Word Rotation Problem
* *Description:* Accepts a non-empty string and moves its first character to the end while keeping all remaining characters in their original order. Preserves the capitalization of every character.

   Code:
  
def rotate_word(text):

    # Store the given text in a string variable
    string = text

    # Move the first character to the end
    return string[1:] + string [0]
    
    # Ask the user to enter a word
    string = input ("Enter a word: ")
    
    #Display the rotated word
    print(rotate_word(string))

### B. Username Builder Problem
* *Description:* Accepts a first name and last name, converts all letters to lowercase, removes all spaces from both names, and joins them using a single period (.).

  Code:

      def make_username (first_name, last_name):
    
      # Convert the first name to lowercase and remove spaces
      first_name = first_name.lower().replace(" ", "")

      # Convert the last name to lowercase and remove spaces
      last_name = last_name.lower().replace(" ", "")

      # Join the processed first and last names using one period
      return first_name + "." + last_name

      # Ask user to enter First Name
      first_name = input("Enter first name: ")

      # Ask user to enter last Name
      last_name = input("Enter last name: ")

      # Display username
      print(make_username(first_name, last_name))

### C.  Bookend Swap Problem
* *Description:* Accepts a list containing at least two elements. Uses extended sequence unpacking to separate the structure and returns a new list where the first and last elements have exchanged positions while keeping the middle intact without mutating the original list.

 Code:

      def swap_bookends(items):

      # Check if the list has at least two elements
      if len(items) < 2:
        return "Error: Please enter at least two elements."

      # "first element, middle elements, and last element
      first, *middle, last = items

      # Return the new list with the first and last elements swapped
      return [last] + middle + [first]

      # Ask the user to enter the elements
      items = input("Enter elements separated by spaces: ").split()

      #Check the number of elements and display the result
      print(swap_bookends(items))

  ## Project File Structure
```text
Bernaldez---Programming-Assignment-1/
│
├── ECE2112_PA1.ipynb        # Main Jupyter Notebook containing solutions and tests
└── README.md                # Project documentation

```
## How to Run

### Using Terminal / Command Prompt
1. Clone or download the repository to your local machine.
2. Open your terminal or command prompt and navigate to the project directory:
   ```bash
   cd path/to/Bernaldez---Programming-Assignment-1
3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook

4. Open `ECE2112_PA1.ipynb` from the browser interface and run all cells sequentially (`Cell > Run All`).

### Using Jupyter Notebook / VS Code
1. Open the project folder in your preferred IDE (e.g., Visual Studio Code).
2. Open `ECE2112_PA1.ipynb`.
3. Ensure your Python kernel is active and execute the cells from top to bottom.
   







