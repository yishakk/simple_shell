#A simple UNIX command interpreter that provides a user interface to access and give orders to the operating system.

Table of Contents
Description
Requirements
How_to_test
Usage
Project_files
Authors
Description
This is a command line interpreter, or shell, in the tradition of the first Unix shell written by Ken Thompson in 1971. This was made as a project for ALX. In this project we apply the knowledge that we have learned in C programming language. Standard functions and system calls employed in simple_shell include:

   access, execve, exit, fork, free, malloc, read, signal, wait, write.
      ```


## Installation

- Clone this repository: `git clone "https://github.com/yishakk/simple_shell.git"`
   - Change directories into the repository: `cd simple_shell`
      - Compile: `gcc -Wall -Werror -Wextra -pedantic *.c -o hsh`
     - Run the shell in interactive mode: `./hsh`
        - Or run the shell in non-interactive mode: example `echo "pwd" | ./hsh`

## How_to_test

The simple_shell is designed to execute commands in a similar manner to sh, however with more limited functionality. The development of this shell is ongoing. The below features will be checked as they become available (see man page for complete information on usage):



## Project_files
| File        | Description |
| ----------- | ----------- |
| `AUTHORS`     | File with names of the owners and authors of this project |
| `README.md`   | Nutshell description of simple_shell project |
| `aux_funs.c`  | Auxiliar functions <br> **signal_exit:** handler for SIGINT signals <br> **_calloc:** allocate memory and fills it with zeros
| `built-ins.`c | Built-ins functions: <br> **check_word:** evalute alpha chars in string <br> **exit_built_in:** stop execution of shell <br> **env_built_in:** prints environment variables |
| `core_funs.c` | Heart of simple_shell <br> **check_builtin:** check if first argument is a built-int <br> **not_found_error:** handler for print error when command is not found <br> **simple_exec:** decision flow for command execution|
| `path_funs.c` | Function to check command in path <br> **_getenv:** search variable in environment vars <br> **cmd_path:** concat first argument with PATH dirs |
| `shell.h`     | Header file <br> **All includes** <br> **All prototypes** <br> **Definition of struct params** |
| `simple_shell.c` | Initialize the simple_shell execution: <br> **test:** <br> Remove \n last char readed with getline <br> Tokenize and save in argv all arguments readed <br> Calls simple_exec <br> **main:** <br> Initialize params struct vars <br> Set signal listenes <br> Print prompt (interactive mode) <br> Read arguments with getline <br> Handle CTRL + D to stop execution|
| `string_funs.c`  | First string functions file <br> **_strcat:** concat string (no malloc) <br> **_strlen:** get length of string <br> **rev_string:** reverse a string <br> **_itoa:** convert int to string <br> **_strcmp:** compare two strings |
| `string_funs2.c`  | Second string functions file <br> **_strchr:** search char in string <br> **_strcpy:** copy string in other one <br> **str_concat:** concat string (malloc) <br> **_atoi:** convert string num, to int|





## Authors
Yishak Kibru [yishakk](https://github.com/yishakk)

Yohannes Tesfaye [jojo2172](https://github.com/jojo2172)
