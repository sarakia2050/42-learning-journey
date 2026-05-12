*This project has been created as part of the 42 curriculum by fkia.*

# Libft

## Description

Libft is a custom C library created as part of the 42 curriculum.

The goal of this project is to reimplement several standard C library functions from scratch and to create additional utility functions that can be reused in future C projects.

This project helped me practice important C concepts such as memory management, pointers, strings, file descriptors, Makefiles, static libraries, and linked lists.

The final result of the project is a static library called `libft.a`.

The library is organized into three main parts:

- **Part 1 – Libc functions:** reimplementations of standard C library functions.
- **Part 2 – Additional functions:** extra utility functions useful for future projects.
- **Part 3 – Linked list functions:** functions used to create and manipulate singly linked lists.

## Instructions

### Compilation

To compile the library, open a terminal in the root directory of the project and run:

```bash
make
```

This command creates the static library:

```bash
libft.a
```

Available Makefile rules:

| Command | Description |
|---------|-------------|
| `make` | Compiles the source files and creates `libft.a`. |
| `all` | Default rule; same behavior as `make`. |
| `clean` | Removes all object files `.o`. |
| `fclean` | Removes all object files `.o` and the library `libft.a`. |
| `re` | Runs `fclean` and then recompiles the library. |
| `bonus` | Compiles the bonus linked-list functions and adds them to `libft.a`. |

Example usage:

```bash
make
make bonus
make clean
make fclean
make re
```

### Usage

Include the header file in your C files:

```c
#include "libft.h"
```

Then compile your program by linking it with the library:

```bash
cc your_file.c -L. -lft -o your_program
```

## Library Description

This library contains reimplementations of standard C functions and additional helper functions.

The functions are divided into the following groups:

- character checking functions;
- string manipulation functions;
- memory manipulation functions;
- conversion functions;
- file descriptor output functions;
- linked list functions.

## Functions Description

### Part 1 – Libc Functions

| Function | Description |
|----------|-------------|
| `ft_isalpha` | Checks if a character is an alphabetic letter. |
| `ft_isdigit` | Checks if a character is a decimal digit from `0` to `9`. |
| `ft_isalnum` | Checks if a character is either alphabetic or numeric. |
| `ft_isascii` | Checks if a character belongs to the ASCII table. |
| `ft_isprint` | Checks if a character is printable, including space. |
| `ft_strlen` | Returns the length of a string, not including the null terminator. |
| `ft_memset` | Fills a block of memory with a specific byte value. |
| `ft_bzero` | Sets a block of memory to zero. |
| `ft_memcpy` | Copies memory from one area to another, but does not handle overlap. |
| `ft_memmove` | Copies memory safely, even if the source and destination overlap. |
| `ft_strlcpy` | Copies a string into a destination buffer with size protection. |
| `ft_strlcat` | Appends a string to another string with size protection. |
| `ft_toupper` | Converts a lowercase letter to uppercase. |
| `ft_tolower` | Converts an uppercase letter to lowercase. |
| `ft_strchr` | Finds the first occurrence of a character in a string. |
| `ft_strrchr` | Finds the last occurrence of a character in a string. |
| `ft_strncmp` | Compares two strings up to a given number of characters. |
| `ft_memchr` | Searches for a byte in a block of memory. |
| `ft_memcmp` | Compares two blocks of memory byte by byte. |
| `ft_strnstr` | Searches for a substring inside a string within a limited length. |
| `ft_atoi` | Converts a string to an integer. |
| `ft_calloc` | Allocates memory for an array and initializes it to zero. |
| `ft_strdup` | Allocates memory and creates a duplicate of a string. |

### Part 2 – Additional Functions

| Function | Description |
|----------|-------------|
| `ft_substr` | Creates a new substring from a string, starting at a given index and with a maximum length. |
| `ft_strjoin` | Creates a new string by joining two strings together. |
| `ft_strtrim` | Creates a copy of a string with specific characters removed from the beginning and the end. |
| `ft_split` | Splits a string into an array of strings using a delimiter character. |
| `ft_itoa` | Converts an integer into a string. |
| `ft_strmapi` | Applies a function to each character of a string and creates a new string with the results. |
| `ft_striteri` | Applies a function to each character of a string, allowing direct modification. |
| `ft_putchar_fd` | Writes a character to a given file descriptor. |
| `ft_putstr_fd` | Writes a string to a given file descriptor. |
| `ft_putendl_fd` | Writes a string followed by a newline to a given file descriptor. |
| `ft_putnbr_fd` | Writes an integer to a given file descriptor. |

### Part 3 – Linked List Functions

| Function | Description |
|----------|-------------|
| `ft_lstnew` | Creates a new linked-list node. |
| `ft_lstadd_front` | Adds a new node at the beginning of a linked list. |
| `ft_lstsize` | Counts the number of nodes in a linked list. |
| `ft_lstlast` | Returns the last node of a linked list. |
| `ft_lstadd_back` | Adds a new node at the end of a linked list. |
| `ft_lstdelone` | Deletes one node and frees its content using the function `del`. |
| `ft_lstclear` | Deletes and frees an entire linked list and sets the list pointer to `NULL`. |
| `ft_lstiter` | Iterates through a linked list and applies a function to each node's content. |
| `ft_lstmap` | Creates a new linked list by applying a function to each node's content. |

## Resources

The following resources were used during the learning process:

- `man 3 <function_name>` for understanding the behavior of standard C library functions.
- 42 subject PDF for the official project requirements.
- Francinette tester: https://github.com/xicodomingues/francinette
- LibftTester: https://github.com/Tripouille/libftTester
- Makefile Tutorial: https://makefiletutorial.com/
- CS50 materials for reviewing C concepts.
- Tutorials and documentation about linked lists in C.

## AI Usage

AI tools such as ChatGPT, Claude, Gemini, duck.ai, and CS50 AI were used only as learning and support tools during this project.

AI was used to:

- understand difficult concepts;
- clarify compiler errors;
- review the behavior of some C functions;
- understand linked lists;
- improve the structure and clarity of this README file.

AI was not used to copy final C source code without understanding.

The purpose of using AI was to support the learning process, improve explanations, and better understand the project requirements.

## Notes

All functions are implemented in C and compiled with the following flags:

```bash
-Wall -Wextra -Werror
```

The library is created using `ar` and stored in the root directory as:

```bash
libft.a
```