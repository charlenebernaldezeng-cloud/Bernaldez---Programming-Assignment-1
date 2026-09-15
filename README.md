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
* Code:*
```python
def rotate_word(text):
    """
    Moves the first character of the string to the end.
    Preserves original capitalization.
    """
    if not text:
        return text
    return text[1:] + text[0]


## Prerequisites & Requirements
* **Python 3.x** installed on your system.
* **Jupyter Notebook** (or JupyterLab / VS Code with Jupyter extension) to run the `.ipynb` file.
* *Note: No external Python libraries or packages are required.*


