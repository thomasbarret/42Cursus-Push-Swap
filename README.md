# 42 Cursus - Push Swap

**Push Swap** is a sorting algorithm project where the objective is to sort a stack of integers using only two stacks and a set of basic operations. The challenge is to implement the most efficient algorithm to sort the numbers in the fewest moves, using limited operations such as push, swap, rotate, and reverse rotate.

---

## Table of Contents
- [Requirements](#requirements)
- [Compilation and Usage](#compilation-and-usage)
- [Algorithm Overview](#algorithm-overview)
- [File Structure](#file-structure)
- [Operations](#operations)
- [Libraries](#libraries)
- [Contributing](#contributing)

---

## Requirements

- GCC (GNU Compiler Collection)
- Make
- A Unix-based system (Linux/macOS recommended)

---

## Compilation and Usage

To compile and run the project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/push_swap.git
   cd push_swap
   ```

2. To compile the project:
   ```bash
   make
   ```

3. To check if the sorting works correctly:
   - For Linux:
     ```bash
     ./checker_linux <list_of_numbers>
     ```

   - For macOS:
     ```bash
     ./checker_mac <list_of_numbers>
     ```

   Example:
   ```bash
   ./checker_linux 3 2 1
   ```

4. The checker will verify if the numbers are sorted after executing the moves, which are printed on the console.

---

## Algorithm Overview

The goal of the Push Swap project is to sort a list of integers using two stacks (A and B). The program can perform the following operations:

- **Push (push a value from one stack to the other)**:
  - `pa`: Push the top element of stack B to stack A.
  - `pb`: Push the top element of stack A to stack B.

- **Swap (swap the two topmost elements of a stack)**:
  - `sa`: Swap the top two elements of stack A.
  - `sb`: Swap the top two elements of stack B.
  - `ss`: Perform `sa` and `sb` simultaneously.

- **Rotate (rotate the stack to move the top element to the bottom)**:
  - `ra`: Rotate stack A.
  - `rb`: Rotate stack B.
  - `rr`: Perform `ra` and `rb` simultaneously.

- **Reverse Rotate (rotate the stack in reverse, moving the bottom element to the top)**:
  - `rra`: Reverse rotate stack A.
  - `rrb`: Reverse rotate stack B.
  - `rrr`: Perform `rra` and `rrb` simultaneously.

The goal is to sort the integers with a minimal number of moves. Efficient algorithms involve strategies like quicksort, merge sort, or even more advanced techniques like the median of three pivot strategy.

---

## File Structure

```
.
├── Makefile                  # Makefile to compile the project
├── checker_linux             # Checker program for Linux
├── checker_mac               # Checker program for macOS
└── src
    ├── checker               # Checker logic and implementation
    │   └── checker.c
    ├── function              # Main sorting algorithm functions
    │   ├── args              # Argument parsing and validation
    │   │   ├── check.c
    │   │   └── create.c
    │   ├── calcul            # Algorithm calculation and sorting
    │   │   ├── cost.c
    │   │   ├── id.c
    │   │   ├── max.c
    │   │   ├── median.c
    │   │   ├── min.c
    │   │   ├── mouvement.c
    │   │   ├── push_swap.c
    │   │   ├── sort.c
    │   │   ├── sort_five.c
    │   │   └── sort_three.c
    │   ├── main.c             # Entry point of the program
    │   └── stack              # Stack-related functions (push, pop, rotate)
    │       ├── push.c
    │       ├── reverse.c
    │       ├── rotate.c
    │       ├── stuct.c
    │       └── swap.c
    └── header                 # Header files for the project
        ├── ft_printf         # Custom printf implementation
        ├── get_next_line     # Functionality for reading lines
        ├── libft             # Custom library with utility functions
        └── push_swap.h       # Project's header file
```

---

## Operations

The operations described above are used to manipulate the two stacks. The challenge is to devise an efficient strategy to sort the stack with the fewest number of operations. For example, rather than simply pushing and swapping, you might rotate or reverse rotate to reduce the overall number of operations required.

---

## Libraries

The project includes several libraries for basic utility functions:

- **libft**: A collection of utility functions for memory management, string manipulation, and data structures.
- **ft_printf**: A custom implementation of the `printf` function.
- **get_next_line**: A utility function to read files line by line, useful for parsing input.