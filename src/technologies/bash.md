# Bash Scripting Guide

## Table of Contents

- [Bash Scripting Guide](#bash-scripting-guide)
  - [Table of Contents](#table-of-contents)
  - [1. Introduction](#1-introduction)
  - [2. Basic Script Structure](#2-basic-script-structure)
  - [3. Variables](#3-variables)
  - [4. Conditional Statements](#4-conditional-statements)
  - [5. Loops](#5-loops)
  - [6. Functions](#6-functions)
  - [7. Command Line Arguments](#7-command-line-arguments)
  - [8. File Operations](#8-file-operations)
  - [9. Error Handling](#9-error-handling)
  - [10. Best Practices](#10-best-practices)
  - [11. Conclusion](#11-conclusion)

## 1. Introduction<a name="introduction"></a>

Bash (Bourne Again SHell) is a command language and shell scripting language widely used in Unix-like operating systems. This guide provides an overview of basic Bash scripting concepts and best practices.

## 2. Basic Script Structure<a name="basic-script-structure"></a>

- **Shebang Line:**
  ```bash
  #!/bin/bash
  ```

- **Comments:**
  ```bash
  # This is a comment
  ```

- **Execution Permission:**
  ```bash
  chmod +x script.sh
  ```

- **Run Script:**
  ```bash
  ./script.sh
  ```

## 3. Variables<a name="variables"></a>

- **Assigning Variables:**
  ```bash
  variable_name="value"
  ```

- **Accessing Variables:**
  ```bash
  echo $variable_name
  ```

## 4. Conditional Statements<a name="conditional-statements"></a>

- **if statement:**
  ```bash
  if [ condition ]; then
    # commands
  fi
  ```

- **elif statement:**
  ```bash
  if [ condition ]; then
    # commands
  elif [ another_condition ]; then
    # commands
  fi
  ```

- **case statement:**
  ```bash
  case $variable in
    pattern1)
      # commands
      ;;
    pattern2)
      # commands
      ;;
    *)
      # default commands
      ;;
  esac
  ```

## 5. Loops<a name="loops"></a>

- **for loop:**
  ```bash
  for item in list; do
    # commands
  done
  ```

- **while loop:**
  ```bash
  while [ condition ]; do
    # commands
  done
  ```

- **until loop:**
  ```bash
  until [ condition ]; do
    # commands
  done
  ```

## 6. Functions<a name="functions"></a>

- **Function Declaration:**
  ```bash
  function_name() {
    # commands
  }
  ```

- **Function Call:**
  ```bash
  function_name
  ```

- **Function with Parameters:**
  ```bash
  function_with_params() {
    param1=$1
    param2=$2
    # commands
  }

  function_with_params arg1 arg2
  ```

## 7. Command Line Arguments<a name="command-line-arguments"></a>

- **Accessing Command Line Arguments:**
  ```bash
  # $1, $2, ... represent the first, second, etc. arguments
  echo "First argument: $1"
  ```

## 8. File Operations<a name="file-operations"></a>

- **Check if File Exists:**
  ```bash
  if [ -e file ]; then
    # commands
  fi
  ```

- **Read from a File:**
  ```bash
  while IFS= read -r line; do
    echo "$line"
  done < file.txt
  ```

- **Write to a File:**
  ```bash
  echo "Hello, World!" > output.txt
  ```

## 9. Error Handling<a name="error-handling"></a>

- **Exit on Error:**
  ```bash
  set -e
  ```

- **Custom Error Messages:**
  ```bash
  die() {
    echo "$1" >&2
    exit 1
  }

  # Usage: die "Error message"
  ```

## 10. Best Practices<a name="best-practices"></a>

- Use meaningful variable names.
- Add comments for complex sections.
- Use indentation for readability.
- Test scripts on various environments.

## 11. Conclusion<a name="conclusion"></a>

Bash scripting is a powerful tool for automating tasks in a Unix-like environment. This guide covers fundamental concepts, but there is much more to explore. Refer to the [Bash manual](https://www.gnu.org/software/bash/manual/bash.html) for detailed information and advanced features.