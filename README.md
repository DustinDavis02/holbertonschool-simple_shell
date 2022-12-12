# 0x17. C - Simple Shell

---

## Descriptions:information_source:

In this project we were tasked on making our own simple UNIX shell that can interpreter simple commands. This program must have the same output as sh (/bin/sh) as well as the exact same error output. The only difference is when we print an error, the name of the program must be your argv[0].

---

## Instructions:information_source:

Write a simple UNIX command interpreter.
* Compiling the program:
`gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh`

* Interactive mode:
```
$ ./hsh
($) /bin/ls
hsh main.c shell.c
($)
($) exit
$
```

* Non-interactive mode:
```
$ echo "/bin/ls" | ./hsh
hsh main.c shell.c test_ls_2
$
$ cat test_ls_2
/bin/ls
/bin/ls
$
$ cat test_ls_2 | ./hsh
hsh main.c shell.c test_ls_2
hsh main.c shell.c test_ls_2
$
```

---

## Requirements:fountain_pen:

- All the files will be compiled on Ubuntu 20.04 LTS 
- This program will be compiled in gcc, using the flags `-Wall -Werror -Wextra -pedantic -std=gnu89`
- All your files should end with a new line
- A README.md file, at the root of the folder of the project is mandatory
- Your code should use the Betty style. It will be checked using [betty-style.pl](https://github.com/holbertonschool/Betty/blob/master/betty-style.pl) and [betty-doc.pl](https://github.com/holbertonschool/Betty/blob/master/betty-doc.pl)
- Your shell should not have any memory leaks
- No more than 5 functions per file
- All our header files will include guards
- Use system calls only when you need to [(why?)](https://www.quora.com/Why-are-system-calls-expensive-in-operating-systems)

---

## Files:file_folder:

File|Descriptions
---|---
[shell.h](./shell.h)|Header file
[shell.c](./shell.c)|Entry point & executes the shell
[non_interactive.c](./non_interactive.c)|gets command line through argument of main
[exec_build.c](./exec_build.c)|Print variable global environment
[get_environment.c](./get_environment.c)|Gets variable environment
[file_execute.c](./file_execute.c)|Validates if the filename exists in the directory
[creator_process.c](./creator_process.c)|Creates a child process and exectutes
[line_reader.c](./line_reader.c)|Reads a line
[get_line.c](./get_line.c)|Gets command line through getline in interactive mode
[strings.c](./strings.c)|Will copy and concatenates strings and return a string to buffer and the length
[strcmp_function.c](./strcmp_function.c)|Compares two strings
[memory_allo.c](./memory_allo.c)|Allocates memory & fills with bytes
[exit.c](./exit.c)|Successful exit

## Tasks:scroll:

### 0. README, man, AUTHORS
* Write a [README](https://github.com/DustinDavis02/holbertonschool-simple_shell/blob/main/README.md)
* Write a [man](https://github.com/DustinDavis02/holbertonschool-simple_shell/blob/main/man_1_simple_shell) for your shell.
* You should have an [AUTHORS](https://github.com/DustinDavis02/holbertonschool-simple_shell/blob/main/AUTHORS) file at the root of your repository, listing all individuals having contributed content to the repository.

### 1. Betty would be proud
* Write a beautiful code that passes the Betty checks

### 2. Simple shell 0.1
* Write a UNIX command line interpreter.
* Your Shell should:
	- Display a prompt and wait for the user to type a command. A command line always ends with a new line.
	- The prompt is displayed again each time a command has been executed.
	- The command lines are simple, no semicolons, no pipes, no redirections or any other advanced features.
	- The command lines are made only of one word. No arguments will be passed to programs.
	- If an executable cannot be found, print an error message and display the prompt again.
	- Handle errors.
	- You have to handle the “end of file” condition (Ctrl+D)
### 3. Simple shell 0.2
* Handle command lines with arguments

### 4. Simple shell 0.3
* Handle the PATH

### 5. Simple shell 0.4
* Implement the exit built-in, that exits the shell
* Usage: exit
* You don’t have to handle any argument to the built-in exit
### 6. Simple shell 1.0
* Implement the env built-in, that prints the current environment

---

# Authors:bookmark:
* Dennis Agbemenu - [dagbeme1](https://github.com/dagbeme1)
* Dustin Davis - [DustinDavis02](https://github.com/DustinDavis02)