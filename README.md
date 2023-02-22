# Simple Shell
This is a simple UNIX command line interpreter (shell) that can read, parse, and execute commands from a terminal or a script file. The shell is implemented in C programming language and can execute built-in shell commands, as well as external commands located in the directories specified in the PATH environment variable.


## Files

- **shell.h**: Header file containing all function prototypes and struct definitions.

- **builtins.c**: Contains the implementation of the built-in functions `exit`, `env` and `cd`.

- **env.c**: Contains functions for working with environment variables, such as `make_env` for creating an environment array and `free_env` for freeing its memory.

- **execute.c**: Contains the implementation of the function `execute_cmd` that executes a command.

- **helpers.c**: Contains helper functions such as `_puts` for printing strings and `_strdup` for duplicating strings.

- **path.c**: Contains functions for working with the `PATH` variable, such as `get_path` for retrieving the `PATH` value and `check_for_path` for searching for a command in the directories specified in the `PATH`.

- **strfunc.c**: This file contains functions related to string manipulation such as `_strlen`, `_strcat`, `_strcmpr` and `_strdup`.

- **tokenize.c**: This file contains the `tokenize` function, that takes a buffer string and a delimiter string as input, and returns a dynamically allocated array of strings representing the tokens obtained by splitting buffer along the occurrences of delimiter.

- **mem_alloc.c** : This file contains `_realloc` function that reallocates a pointer to double the space

- **errs.c**: This file could contain functions related to error handling such as `print_error`, `_puts` and `_utoia`

- **new_strtok.c**: This file contains a custom implementation of strtok function `new_strtok` that is used to split a string into a sequence of tokens based on a delimiter.

- **shell.c**: Main program that contains the shell loop

## Installation
To use the shell, you can compile the program from the source code using the following command:

`gcc -Wall -Werror -Wextra -pedantic *.c -o hsh`
Alternatively, you can use the provided Makefile to build the program:

To start the shell, run the following command:

#### bash

`./hsh`
The shell will display a prompt (**$** ) and wait for the user to enter a command. The user can enter any UNIX command (with or without options) and the shell will execute it. The shell supports command chaining using semicolons (;).

## Built-in Commands
The shell supports the following built-in commands:

* `exit`: exits the shell
* `env`: prints the current environment
* `setenv`: sets the value of an environment variable
* `unsetenv`: removes an environment variable

_**Examples**_
 Here are some examples of how to use the shell:

#### bash
**$** `./hsh`

**$** `ls -l`

``` 
total 100
 
-rw-rw-r-- 1 user user  1157 Mar 11 16:45 shell.h

-rwxrwxr-x 1 user user 27416 Mar 11 16:45 hsh

-rw-rw-r-- 1 user user  1178 Mar 11 16:45 builtins.c

-rw-rw-r-- 1 user user  1165 Mar 11 16:45 env.c

-rw-rw-r-- 1 user user  1177 Mar 11 16:45 execute.c

-rw-rw-r-- 1 user user  2764 Mar 11 16:45 helpers.c

-rw-rw-r-- 1 user user  1119 Mar 11 16:45 path.c

-rw-rw-r-- 1 user user  3748 Mar 11 16:45 shell.c 
 ```


**$** `echo "Hello, world!"`

`Hello, world!` 


**$** `ls -l ; pwd`

``` 
total 100

-rw-rw-r-- 1 user user  1157 Mar 11 16:45 shell.h
 
-rwxrwxr-x 1 user user 27416 Mar 11 16:45 hsh
 
-rw-rw-r-- 1 user user  1178 Mar 11 16:45 builtins.c
 
-rw-rw-r-- 1 user user  1165 Mar 11 16:45 env.c
 
-rw-rw-r-- 1 user user  1177 Mar 11 16:45 execute.c
 
-rw-rw-r-- 1 user user  2764 Mar 11 16:45 helpers.c
 
-rw-rw-r-- 1 user user  1119 Mar 11 16:45 path.c
 
-rw-rw-r-- 1 user user  3748 Mar 11 16:45 shell.c

/home/user
```

**$** `exit`

## Credits
This shell was developed by 
- Gloria Owusu 
- Joshua Dei-Alorse @github _https://github.com/YoungKing-Joshua_

as a project for _Alx Software Engineering C course_.
