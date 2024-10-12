# ft_printf - Custom printf Implementation

## Introduction
This project is a custom implementation of the standard `printf` function in C. The goal was to reproduce the behavior of `printf` from the C Standard Library, focusing on formatted output. Implementing `ft_printf` from scratch allowed me to dive into the intricacies of variadic functions, formatting specifiers, and buffer management.

## What I Did
The `ft_printf` function can handle various format specifiers such as:
- **%c** for characters
- **%s** for strings
- **%p** for pointers
- **%d** and **%i** for integers
- **%u** for unsigned integers
- **%x** and **%X** for hexadecimal numbers
- **%%** for printing a literal percent sign

### Key Aspects of the Implementation:
1. **Variadic Functions**: I implemented `ft_printf` using `va_list` to handle a variable number of arguments. This required a strong understanding of how to traverse argument lists and pass them to the appropriate formatting functions.

2. **Format Parsing**: The core of `ft_printf` is parsing the format string, identifying specifiers, and converting arguments accordingly. I wrote auxiliary functions to handle each specifier type, ensuring code modularity and reuse.

3. **Buffer Management**: I optimized memory usage by avoiding unnecessary dynamic memory allocation.

4. **Edge Case Handling**: I accounted for edge cases such as:
   - Null pointers passed to `%s` or `%p`.
   - Overflow situations for integer and unsigned conversions.
