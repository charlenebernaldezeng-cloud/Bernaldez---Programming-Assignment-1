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
* Code:
  
def rotate_word(text):

    # Store the given text in a string variable
    string = text

    # Move the first character to the end
    return string[1:] + string [0]
    string = input ("Enter a word: ")
    print(rotate_word(string))

### B. Username Builder Problem
* *Description:* Accepts a first name and last name, converts all letters to lowercase, removes all spaces from both names, and joins them using a single period (.).
* Code:

### C.  Bookend Swap Problem
* *Description:* Accepts a list containing at least two elements. Uses extended sequence unpacking to separate the structure and returns a new list where the first and last elements have exchanged positions while keeping the middle intact without mutating the original list.
* Code:







