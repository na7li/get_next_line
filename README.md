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

## 🔧 Function Prototype

### Mandatory Part
```c
char *get_next_line(int fd);
```

### Bonus Part
The bonus part allows the program to read from multiple file descriptors without interference.
Same prototype:
```bash
char *get_next_line(int fd);
```

But now it must handle multiple file descriptors simultaneously without mixing their states.

---

## HOW TO USE
#### 1º - Clone the repository
```git
https://github.com/na7li/get_next_line.git
```

#### 2º - Enter the project folder
```bash
cd get_next_line/
```

#### 3º - Compile the mandatory or bonus files
> The program should always be compiled with the flags below.
```bash
[Flags] -Wall -Wextra -Werror
[Mandatory] cc [Flags] main.c get_next_line.c get_next_line_utils.c
[Bonus] cc [Flags] main.c get_next_line_bonus.c get_next_line_utils_bonus.c
```

#### 3º - BUFFER_SIZE can be specified at compilation to override the default BUFFER_SIZE
> get_next_line should be able to compile with and without the -D BUFFER_SIZE=[SIZE] flag.
```bash
[Flags] -Wall -Wextra -Werror -D BUFFER_SIZE=[SIZE] 
[Mandatory] cc [Flags] main.c get_next_line.c get_next_line_utils.c
[Bonus] cc [Flags] main.c get_next_line_bonus.c get_next_line_utils_bonus.c
```

#### 4º - Execution with one or multiple file descriptors/standard input
```bash
./a.out [text.txt]
./a.out [text1.txt] [text2.txt]
```
