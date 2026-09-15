# ECE 2112 - Programming Assignment 1
### Name: Bernaldez, Charlene A.                                                                      
### Section: 2ECE-B

## Table of Contents
- [Overview](#overview)
- [Function Summary](#function-summary)
- [Problem Specifications & Solutions](#problem-specifications--solutions)
  - [A. Word Rotation Problem](#a-word-rotation-problem)
  - [B. Username Builder Problem](#b-username-builder-problem)
  - [C. Bookend Swap Problem](#c-bookend-swap-problem)
- [Project File Structure](#project-file-structure)
- [Requirements](requirements)
- [How to Run](#how-to-run)
  - [Using Terminal / Command Prompt](#using-terminal--command-prompt)
  - [Using Jupyter Notebook](#using-jupyter-notebook)
- [Edge Cases Handled](#edge-cases-handled)

---

## Overview

This project contains Python solutions for introductory string manipulation and list indexing exercises. The tasks demonstrate fundamental programming concepts including:
* String indexing and slicing
* String cleaning (.lower(), .replace())
* Extended list unpacking (* operator)
* Immutability and pure function design (non-destructive list operations)

---

## Function Summary

| Function | Input Parameters | Return Type | Key Logic |
| :--- | :--- | :--- | :--- |
| rotate_word(text) | text (str) | str | Moves index 0 to end using text[1:] + text[0] |
| make_username(first_name, last_name) | first_name (str), last_name (str) | str | Lowercases, strips spaces, joins with . |
| swap_bookends(items) | items (list) | list | Unpacks using first, *middle, last, swaps endpoints |

---

## Problem Specifications & Solutions

### A. Word Rotation Problem
* *Description:* Accepts a non-empty string and moves its first character to the end while keeping all remaining characters in their original order. Preserves the capitalization of every character.
* *Implementation Code:*
```python
def rotate_word(text):
    """
    Moves the first character of the string to the end.
    Preserves original capitalization.
    """
    if not text:
        return text
    return text[1:] + text[0]

### B. Username Builder Problem
**Description:** Accepts a first name and last name, converts all letters to lowercase, removes all internal and surrounding spaces, and joins them together separated by a single period (`.`).

**Implementation Code:**
```python
def make_username(first_name, last_name):
    """
    Converts names to lowercase, removes spaces, 
    and combines them with a period.
    """
    clean_first = first_name.lower().replace(" ", "")
    clean_last = last_name.lower().replace(" ", "")
    return f"{clean_first}.{clean_last}"

### C. Bookend Swap Problem
**Description:** Accepts a list containing at least two elements. Uses extended sequence unpacking to separate the structure and returns a new list where the first and last elements have exchanged positions while keeping the middle intact without mutating the original list.

**Implementation Code:**
```python
def swap_bookends(items):
    """
    Swaps the first and last elements of a list using extended unpacking
    while preserving the middle elements.
    """
    first, *middle, last = items
    return [last] + middle + [first]

## Prerequisites & Requirements
* **Python 3.x** installed on your system.
* **Jupyter Notebook** (or JupyterLab / VS Code with Jupyter extension) to run the `.ipynb` file.
* *Note: No external Python libraries or packages are required.*


