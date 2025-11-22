# SimpleScript2 – Public Compiler Project

A Java-based mini-compiler created for the Programming Languages course.  
This project implements the front-end stages of a compiler for a simplified language called **SimpleScript**, including scanning, LL(1) parsing, and CSV-driven grammar validation.

---

## Overview

SimpleScript2 demonstrates the essential components of compiler construction:

- **Lexical Analysis** (tokenizing source code)
- **Syntax Analysis** using **LL(1) parsing**
- **Grammar validation** via First/Follow sets
- **CSV-based parsing tables**
- **Error detection and reporting**

This public version is cleaned and published for portfolio, academic, and reference use.

---

## Features

### 1. Lexical Analysis (Scanner)
- Reads and tokenizes `.simp` source files.
- Supports:
  - Identifiers  
  - Keywords  
  - Operators  
  - Numbers  
  - Symbols and delimiters  
- Produces a token stream used by the parser.

### 2. Syntax Analysis (LL(1) Parser)
- Uses LL(1) table-driven parsing.
- References:
  - `LL1_parsing_table.csv`
  - `first_follow_sets.csv`
  - `parsing_table.csv`
- Detects:
  - Unexpected tokens  
  - Mismatched rules  
  - Invalid productions  

### 3. Grammar Tables (CSV)
Grammar definitions and parsing tables are stored as `.csv` files to keep parsing rules modular and easy to update.

### 4. Sample Output
Includes `output.txt`, showing the parser’s processing and accepted/rejected sequences.

---

## Project Structure
SimpleScript2-Public/
│
├── lib/src/               # Source code (scanner, parser, utilities)
├── scanner/               # Scanning module
├── LL1_parsing_table.csv  # LL(1) parsing table
├── first_follow_sets.csv  # First & Follow sets
├── parsing_table.csv      # Grammar rules
├── output.txt             # Sample compilation output
└── README.md              # Project documentation

---

## How to Run

### Requirements
- Java 8+  
- Any IDE (IntelliJ IDEA recommended) or terminal with `javac`

## How to Run

1. Open the project in your IDE or navigate to `/lib/src/`.
2. Compile all Java files:
3. Run the main compiler:
4. Provide a .simp source file to test.
5. Example SimpleScript Input

let a;
a = 5;
while (a < 10) {
  a = a + 1;
}

