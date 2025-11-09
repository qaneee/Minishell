# Minishell

**Minishell** is a group project developed by me and Ilya (ipogodae)

This repository contains our implementation of a simplified shell (“minishell”) as typically required in a C curriculum project (such as 42 School). Minishell is a command-line interpreter that mimics basic command parsing and execution, similar to Bash, but with limited built-in functionality, written in C.

---

## Features

- **Prompt & Input Handling:** Interactive prompt where users can type commands.
- **Command Parsing:** Supports quoting, variable expansion, and tokenization.
- **Built-in Commands:** Implements core built-ins such as `cd`, `echo`, `pwd`, `export`, `unset`, and `exit`.
- **External Commands:** Runs executables found in system `$PATH`.
- **Pipes & Redirections:** Supports shell pipes (`|`) and input/output redirection (`>`, `<`, `>>`).
- **Environment Management:** Handles environment variables.
- **Signal Handling:** Properly handles signals like `CTRL+C`, `CTRL+\` and `CTRL+D`.
- **Error Management:** Displays appropriate error messages on invalid commands or syntax.

## Installation

You will need to have a C compiler (like gcc or clang) and Make installed on your machine.

```bash
git clone https://github.com/qaneee/Minishell.git
cd Minishell
make
```

## Usage

Run minishell in the terminal:

```bash
./minishell
```

You should be greeted by a prompt. You can now enter shell commands. Examples:

```bash
echo "Hello, world!"
ls -la | grep minishell
export MYVAR=42
echo $MYVAR
cd ..
pwd
```

## Project Structure

- `src/` — Source code files
- `include/` — Header files
- `Makefile` — Build instructions

## Example

```shell
$ ./minishell
minishell$ echo "Welcome to Minishell!"
Welcome to Minishell!
minishell$ pwd
/home/qaneee/Minishell
minishell$ ls | grep minishell
minishell.c
minishell$
```
