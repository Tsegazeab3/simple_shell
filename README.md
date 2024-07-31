# Simple Shell Project

This project implements a simple shell that can execute commands with their full path. The shell reads commands from the standard input, searches for the executable file, and runs it in a child process.

## Files and Functions

### main.c
The main file of the project, containing the entry point of the shell.

#### Functions:
- `int main(void)`: The main function that implements the shell loop, reads commands, and executes them.

### execve.c
Implements the `_execve` function which wraps the `execve` system call.

#### Functions:
- `void _execve(const char *pathname, char *const argv[], char *const env[])`: Executes a program with given arguments and environment variables.

### fork.c
Implements the `_fork` function which wraps the `fork` system call.

#### Functions:
- `int _fork(void)`: Creates a new child process and returns the PID of the child to the parent process.

### free.c
Implements the `_free` function to free allocated memory for arrays.

#### Functions:
- `void _free(char **argv)`: Frees memory allocated for an array of strings.

### getenv.c
Implements the `_getenv` function to get environment variables.

#### Functions:
- `char *_getenv(const char *name)`: Retrieves the value of an environment variable.

### realloc.c
Implements the `_realloc` function to reallocate memory blocks.

#### Functions:
- `void *_realloc(void *ptr, unsigned int old_size, unsigned int new_size)`: Reallocates a memory block to a new size.

### strdup.c
Implements the `_strdup` function to duplicate strings.

#### Functions:
- `char *_strdup(const char *str)`: Returns a pointer to a new string which is a duplicate of the input string.

### strstr.c
Implements the `_strstr` function to locate a substring.

#### Functions:
- `char *_strstr(char *haystack, const char *needle)`: Finds the first occurrence of a substring within a string.

### isatty.c
Implements the `_isatty` function to check if a file descriptor refers to a terminal.

#### Functions:
- `void _isatty(void)`: Writes a prompt if the standard input is a terminal.

### path_dir.c
Implements the `path_dir` function to find the command directory.

#### Functions:
- `char *path_dir(char *program)`: Searches for the directory of a command in the system PATH.

### strtok.c
Implements the `_strtok` function to split strings into tokens.

#### Functions:
- `char **_strtok(char *str, const char *delim)`: Splits a string into tokens based on delimiters and returns an array of tokens.

### str_concat.c
Implements the `str_concat` function to concatenate two strings.

#### Functions:
- `char *str_concat(char *s1, char *s2)`: Concatenates two strings and returns a new string.

### strlen.c
Implements the `_strlen` function to find the length of a string.

#### Functions:
- `int _strlen(char *s)`: Returns the length of a string.
## Usage
1. Clone the repository.
2. Compile the project using `gcc -Wall -Werror -Wextra -pedantic *.c -o simple_shell`.
3. Run the shell using `./simple_shell`.
4. Type commands with their full path to execute them.
5. Type `exit` to exit the shell.

## Example
```sh
$ ./simple_shell
$ /bin/ls
$ /bin/echo Hello, world!
$ exit
