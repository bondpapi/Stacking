# Stacking
This Python program determines whether it's possible to stack a row of cubes into a vertical pile following specific stacking rules.

## Overview

This Python program determines whether it's possible to stack a row of cubes into a vertical pile following specific stacking rules. At each step, you can only pick the leftmost or rightmost cube from the remaining row. The stacked pile must maintain non-decreasing cube sizes from top to bottom.

## Problem Description

You are given a horizontal row of n cubes, each with a specific side length. Your task is to create a new vertical pile of cubes adhering to the following rules:

### Stacking Rule:

- If cube i is placed on top of cube j, then the side length of cube i must be greater than or equal to the side length of cube j.

### Selection Constraint:

- At each step, you can only pick the leftmost or rightmost cube from the remaining row to place on the pile.

# The program should output "Yes" if it's possible to stack all cubes following these rules; otherwise, it should output "No".

## Examples

## Input:
2

5

1 2 3 8 7

5

1 2 3 7 8

## Output:
No

Yes

## Explanation:
# First Test Case: 
- After selecting 7 and then 1, both remaining options (2 and 8) are larger than 1, making it impossible to stack correctly.

# Second Test Case:
- By selecting cubes in the order 8, 7, 3, 2, 1, the stacking rules are satisfied.

# Solution Approach

The problem can be efficiently solved using a two-pointer approach:

1. Initialization:
    - Set two pointers, left at the start of the list and right at the end.
    - Initialize a variable top to keep track of the last placed cube size, starting with infinity.

2. Iteration:
    - At each step, compare the leftmost and rightmost cubes.
    - Choose the larger of the two to place on the pile (to maximize the chance of adhering to the stacking rule).
    - If the chosen cube is larger than top, the stacking is invalid ("No").
    - Update top with the size of the placed cube and move the corresponding pointer.

3. Termination:
    - If all cubes are placed successfully following the rules, output "Yes".

This approach ensures that at each step, the best possible cube is chosen to maximize the feasibility of future placements.

# Getting Started

## Prerequisites
Python 3.x installed on your system.

## Installation
Clone the Repository:

git clone https://github.com/bondpapi/Stacking

cd stacking

## Install Dependencies:  
This script uses only standard Python libraries, so no additional installations are required.

# Usage

1. Run the script: 
    python stacking.py

2. Provide Input: The program reads input from the standard input. You can input manually or redirect from a file.

### Input Format

#### First Line:
    An integer T, the number of test cases.

#### For Each Test Case:
    - First Line: An integer n, the number of cubes.
    - Second Line: n space-separated integers representing the side lengths of the cubes.

## Time and Space Complexity

- Time Complexity: O(n) per test case, where n is the number of cubes. Each cube is processed exactly once.

- Space Complexity: O(n) for storing the list of cube side lengths.

# Constraints
- 1 <= T < 5
- 1 < n <= 10^5
- 1 < sideLength < 2^31

# Author
MICHAEL BOND

Email: bondpapi@yahoo.com
