This contains a description of tests, allowed functions, and system calls for a simple UNIX command interpreter

# Project Title

A brief description of what this project does and who it's for


## Authors

- [@Masaku12](https://github.com/Masaku12)
- [@CzarProCoder](https://github.com/CzarProCoder)



# Documentation

[Documentation](https://linktodocumentation)

# Learning Objectives

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General
- Who designed and implemented the original Unix operating system
- Who wrote the first version of the UNIX shell
- Who invented the B programming language (the direct predecessor to the C programming language)
- Who is Ken Thompson
- How does a shell work
- What is a pid and a ppid
- How to manipulate the environment of the current process
- What is the difference between a function and a system call
- How to create processes
- What are the three prototypes of main
- How does the shell use the PATH to find the programs
- How to execute another program with the execve system call
- How to suspend the execution of a process until one of its children terminates
- What is EOF / “end-of-file”?

# Copyright - Plagiarism

You are tasked to come up with solutions for the tasks below yourself to meet with the above learning objectives.
You will not be able to meet the objectives of this or any following project by copying and pasting someone else’s work.
You are not allowed to publish any content of this project.
Any form of plagiarism is strictly forbidden and will result in removal from the program.

# Requirements

## General

Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
Your shell should not have any memory leaks
No more than 5 functions per file
All your header files should be include guarded
Use system calls only when you need to (why?)
Write a README with the description of your project
You should have an AUTHORS file at the root of your repository, listing all individuals having contributed content to the repository. Format, see Docker.

## GitHub
*There should be one project repository per group. If you and your partner have a repository with the same name in both your accounts, you risk a 0% score. Add your partner as a collaborator.*

# More Info
## Output
Unless specified otherwise, your program must have the exact same output as sh (/bin/sh) as well as the exact same error output.
The only difference is when you print an error, the name of the program must be equivalent to your argv[0] (See below)
Example of error with sh:

$ echo "qwerty" | /bin/sh
/bin/sh: 1: qwerty: not found
$ echo "qwerty" | /bin/../bin/sh
/bin/../bin/sh: 1: qwerty: not found
$
Same error with your program hsh:

$ echo "qwerty" | ./hsh
./hsh: 1: qwerty: not found
$ echo "qwerty" | ./././hsh
./././hsh: 1: qwerty: not found

# List of allowed functions and system calls

<ul> 
<li> access (man 2 access) </li>
<li> chdir (man 2 chdir) </li>
<li> close (man 2 close) </li>
<li> closedir (man 3 closedir) </li>
<li> execve (man 2 execve) </li>
<li> exit (man 3 exit) </li>
<li> _exit (man 2 _exit) </li>
<li> fflush (man 3 fflush) </li>
<li> fork (man 2 fork) </li>
<li> free (man 3 free) </li>
<li> getcwd (man 3 getcwd) </li>
<li> getline (man 3 getline) </li>
<li> getpid (man 2 getpid) </li>
<li> isatty (man 3 isatty) </li>
<li> kill (man 2 kill) </li>
<li> malloc (man 3 malloc) </li>
<li> open (man 2 open) </li>
<li> opendir (man 3 opendir) </li>
<li> perror (man 3 perror) </li>
<li> read (man 2 read) </li>
<li> readdir (man 3 readdir) </li>
<li> signal (man 2 signal) </li>
<li> stat (__xstat) (man 2 stat) </li>
<li> lstat (__lxstat) (man 2 lstat) </li>
<li> fstat (__fxstat) (man 2 fstat) </li>
<li> strtok (man 3 strtok) </li>
<li> wait (man 2 wait) </li>
<li> waitpid (man 2 waitpid) </li>
<li> wait3 (man 2 wait3) </li>
<li> wait4 (man 2 wait4) </li>
<li> write (man 2 write) </li>
</ul>

# Compilation
Your shell will be compiled this way:

gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh