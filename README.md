# 0x17. C - Simple Shell

---

## Descriptions:information_source:

In this project we were tasked on making our own simple UNIX shell that can interpreter simple commands. This program must have the same output as sh (/bin/sh) as well as the exact same error output. The only difference is when we print an error, the name of the program must be your argv[0].

---

# Instructions:information_source:

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

# Requirements:fountain_pen:


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

## File|Descriptions
---|---
[shell.h](./shell.h)| Header file
[shell.c](./shell.c)| Entry point & executes the shell
 [memory_allo.c](./memory_allo.c)| allocates memory & fills with bytes
[exit.c](./exit.c)| successful exit

# Tasks:scroll:




# List of allowed functions and system calls:books:
* access (man 2 access)
* chdir (man 2 chdir)
* close (man 2 close)
* closedir (man 3 closedir)
* execve (man 2 execve)
* exit (man 3 exit)
* _exit (man 2 _exit)
* fflush (man 3 fflush)
* fork (man 2 fork)
* free (man 3 free)
* getcwd (man 3 getcwd)
* getline (man 3 getline)
* getpid (man 2 getpid)
* isatty (man 3 isatty)
* kill (man 2 kill)
* malloc (man 3 malloc)
* open (man 2 open)
* opendir (man 3 opendir)
* perror (man 3 perror)
* read (man 2 read)
* readdir (man 3 readdir)
* signal (man 2 signal)
* stat (__xstat) (man 2 stat)
* lstat (__lxstat) (man 2 lstat)
* fstat (__fxstat) (man 2 fstat)
* strtok (man 3 strtok)
* wait (man 2 wait)
* waitpid (man 2 waitpid)
* wait3 (man 2 wait3)
* wait4 (man 2 wait4)
* write (man 2 write)

---

---
# Authors:scroll:
* Dennis Agbemenu - [dagbeme1](https://github.com/dagbeme1)
* Dustin Davis - [DustinDavis02](https://github.com/DustinDavis02)