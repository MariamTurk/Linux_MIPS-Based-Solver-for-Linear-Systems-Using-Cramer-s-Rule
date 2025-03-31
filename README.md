# MIPS-Based Solver for Linear Systems Using Cramer’s Rule

This project is a MIPS Assembly implementation that reads linear equation systems (2-variable and 3-variable), solves them using **Cramer's Rule**, and outputs the results either to the screen or to a file based on user input. It is part of a systems programming and assembly language project conducted at Birzeit University.

## 📌 Features

- 📁 **File Input**: Reads systems from a text file containing multiple equations.
- 🧠 **Equation Parsing**: Detects and validates formats for 2-variable and 3-variable linear systems.
- 🧮 **Cramer’s Rule Solver**: Solves systems using determinant-based logic for accurate results.
- 🖥️ **Output Options**: Choose to print results on screen or write them to an output file.
- 📊 **Result Formatting**: Displays variable values (X, Y, Z) with fractional representation when needed.
- 🔄 **Menu Interface**: User-driven interaction with options to solve, export, or exit.

---

## 🧾 Input Format
Each system is defined by 2 or 3 equations (depending on the number of variables). Example for a 3-variable system:
2x + 3y - z = 4
-1x + 5y + 2z = 10
4x - 2y + 3z = 6

Separate systems are split by empty lines.

---

## ⚙️ How It Works
The user selects to read a file from the menu.

The file is parsed, checking for equation structure and extracting coefficients.

For each system:

The determinant det(A) is computed.

Determinants det(A1), det(A2), det(A3) are computed by replacing columns.

Results are calculated as:

X = det(A1)/det(A)

Y = det(A2)/det(A)

Z = det(A3)/det(A) (if 3-variable)

Outputs are stored in an in-memory buffer.

The user can then choose to:

Display results on screen.

Export results to a text file.

---


## 🛠️ Usage
This project is intended to be run on MIPS simulators such as QtSPIM. To test:

Open main.asm in QtSPIM.

Assemble and Run the code.

Use the menu to interact (input file, choose output, etc.)

---

## 🔄 Sample Menu
Choose an option:
1 - Read input file
2 - f or F for output to file
3 - s or S for screen output
4 - e or E to exit
Choice:

---

## 📌 Notes
The program handles invalid inputs and formatting errors gracefully.

Supports integer and fractional outputs.

Cramer's Rule will fail gracefully on singular systems (i.e., zero determinant).




