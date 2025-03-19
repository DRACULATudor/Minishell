## Project Info

### Objective
The **MiniShell** project consists of creating a basic Unix shell. This shell should be able to execute commands, handle input from the user, and execute built-in functions. The project focuses on understanding process management, handling signals, managing file descriptors, and implementing essential shell functionalities.

## Compilation

```
make
```
Or, if there is no Makefile:
```
gcc -Wall -Wextra -Werror + all files which have .c as extenstion
```
Run the program:
```
./exec_name(check Makefile)

```

How to use:
```
$ ./minishell
minishell$ echo Hello, World!
Hello, World!
minishell$ cd /home/user
minishell$ exit
```

### Functionality
The shell should support the following basic features:
- **Reading User Input**: The shell should continuously read user input.
- **Executing Commands**: It should execute external commands by calling appropriate system functions.
- **Handling Built-in Commands**: Implement built-in commands like `cd`, `exit`, etc.
- **Signal Handling**: Implement signal handling, particularly for the `SIGINT` signal (Ctrl + C).
- **Redirection and Pipelines**: Implement basic I/O redirection (e.g., `>`, `<`) and pipes (`|`).
- **Environment Variables**: The shell should support environment variable handling, allowing users to set and read environment variables.

## Topics Covered

### 1. **Process Management**
   - **Forking**: Creating child processes using the `fork()` system call.
   - **Executing Commands**: Using `exec()` functions to execute external commands.
   - **Waiting for Processes**: Using `waitpid()` to wait for child processes to terminate.

### 2. **Signal Handling**
   - Handling signals such as `SIGINT` (Ctrl + C) to manage how the shell reacts to interruptions.
   - Customizing signal handling behavior to ensure the shell does not terminate unexpectedly.

### 3. **Built-In Commands**
   - Implementing basic built-in commands such as `cd`, `exit`, and handling them within the shell.
   - Understanding how built-in commands bypass the usual process creation and execution flow.

### 4. **Environment Variables**
   - Managing environment variables using functions like `getenv()`, `setenv()`, and `unsetenv()`.
   - Setting and exporting environment variables to maintain the state of the shell.

### 5. **Redirection and Pipelines**
   - Implementing input and output redirection (`>`, `<`) to control where data is sent or read from.
   - Handling pipelines (`|`) to link multiple commands together, passing the output of one command as the input to the next.

### 6. **Memory Management**
   - Proper handling of dynamic memory allocation and deallocation.
   - Avoiding memory leaks when manipulating strings and handling processes.
