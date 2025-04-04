# 📄 get_next_line

**A project from the 1337/42 Common Core Curriculum**

## 📚 Description

The `get_next_line` project is about implementing a function in C that reads a line from a file descriptor, one line at a time, until the end of the file (EOF). Each call to the function returns the next line, including the newline character (`\n`) if there is one.

This project emphasizes memory management, file reading, and handling multiple file descriptors, especially in the bonus part.

## 🧠 Skills Learned

- File descriptors and low-level file I/O
- Memory allocation and management
- Handling buffers efficiently
- Working with static variables
- Managing multiple file descriptors (bonus)
- Understanding edge cases and constraints

---

## ✅ Project Requirements

- **No usage of standard C library functions** (except `read`, `malloc`, and `free`)
- Return one line per call to `get_next_line()`
- Handle reading from multiple file descriptors (bonus)
- Manage memory correctly and avoid leaks

---

## HOW TO USE
#### 2º - Clone the repository
```git
https://github.com/szemmouri/get_next_line.git
```

#### 3º - Enter the project folder
```bash
cd get_next_line/
```

#### 4º - Compile the mandatory or bonus files
> The program should always be compiled with the flags below.
```bash
[Flags] -Wall -Wextra -Werror
[Mandatory] cc [Flags] main.c get_next_line.c get_next_line_utils.c
[Bonus] cc [Flags] main.c get_next_line_bonus.c get_next_line_utils_bonus.c
```

#### 5º - BUFFER_SIZE can be specified at compilation to override the default BUFFER_SIZE
> get_next_line should be able to compile with and without the -D BUFFER_SIZE=[SIZE] flag.
```bash
[Flags] -Wall -Wextra -Werror -D BUFFER_SIZE=[SIZE] 
[Mandatory] cc [Flags] main.c get_next_line.c get_next_line_utils.c
[Bonus] cc [Flags] main.c get_next_line_bonus.c get_next_line_utils_bonus.c
```

#### 6º - Execution with one or multiple file descriptors/standard input
```bash
./a.out [text.txt]
./a.out [text1.txt] [text2.txt]
```

## MANDATORY
- [x] Read from one file descriptor, one line at a time.
- [x] Needs to return the line that was read. If empty or error, return `NULL`.
- [x] Should work as expected reading from a file or standard input.
- [x] Returned line should include the terminating `\n` character, except if it's the end of the file and the line does not end with `\n`.
- [x] The `get_next_line.h` header file should include at least the `get_next_line()` function.
- [x] All adicional functions should be included in `get_next_line_utils.c` file, libft is not allowed.
- [x] To define the buffer size for `read()`, add the option to the compiled file `-D BUFFER_SIZE=[SIZE]`.

## BONUS
- [x] Use only one static variable.
- [x] Manage multiple file descriptors at the same time.
- [x] Bonus files should include a suffix `_bonus.[c/h]`.

## NORMINETTE
> At 42 School, it is expected that almost every project is written following the Norm, which is the coding standard of the school.

```
- No for, do...while, switch, case, goto, ternary operators, or variable-length arrays allowed;
- Each function must be a maximum of 25 lines, not counting the function's curly brackets;
- Each line must be at most 80 columns wide, with comments included;
- A function can take 4 named parameters maximum;
- No assigns and declarations in the same line (unless static);
- You can't declare more than 5 variables per function;
- ...
```

* [42 Norms](https://github.com/42School/norminette/blob/master/pdf/en.norm.pdf) - Information about 42 code norms. `PDF`
* [Norminette](https://github.com/42School/norminette) - Tool to respect the code norm, made by 42. `GitHub`
* [42 Header](https://github.com/42Paris/42header) - 42 header for Vim. `GitHub`
