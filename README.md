# Unix Utilities

A collection of basic Unix command-line utilities implemented in Go. This project recreates fundamental Unix tools to help understand their inner workings and practice Go programming.

## Prerequisites

- Go 1.16 or higher must be installed on your system
- Basic knowledge of command-line operations

## Implemented Utilities

This project includes the following Unix utilities:

### 1. ls - List Directory Contents

Lists all files and directories in the current working directory with color coding for executables.

**Features:**
- Lists all files in the current directory
- Color codes executable files in green for easy identification
- Displays regular files with standard formatting

**Usage:**
```bash
go run ls.go
```

**Example Output:**
```
.git  cat.go  grep.go  ls.go  main.go  test.txt  ws.go
```
*Note: Executable files will appear in green in the terminal*

---

### 2. cat - Concatenate and Display File Contents

Reads and displays the complete content of a specified file.

**Features:**
- Reads any text file
- Displays content to standard output
- Error handling for missing or unreadable files

**Usage:**
```bash
go run cat.go <filename>
```

**Example:**
```bash
go run cat.go test.txt
```

**Example Output:**
```
first line for testing
second line for testing
third line for testing
fourth line for testing
fifth line for testing
```

---

### 3. grep - Search for Text in Files

Searches for a target string within a file and highlights matching occurrences.

**Features:**
- Searches for a specific string in a file
- Highlights matching text in red
- Word-based pattern matching

**Usage:**
```bash
go run grep.go <filename> <search_string>
```

**Example:**
```bash
go run grep.go test.txt "testing"
```

**Example Output:**
```
first line for testing
second line for testing
third line for testing
fourth line for testing
fifth line for testing
```
*Note: Matching words will be highlighted in red in the terminal*

---

### 4. ws - Word Statistics (Word Count)

Displays statistics about a file including the number of lines, words, and bytes.

**Features:**
- Counts the number of lines in a file
- Counts the total number of words
- Displays the file size in bytes

**Usage:**
```bash
go run ws.go <filename>
```

**Example:**
```bash
go run ws.go test.txt
```

**Example Output:**
```
Lines: 5
Words: 16
Bytes: 116
```

---

## Installation

No installation is required. Simply clone the repository and run the utilities using `go run`:

```bash
git clone https://github.com/ashusevim/Unix-Utilities.git
cd Unix-Utilities
```

## Project Structure

```
Unix-Utilities/
├── ls.go      # List directory contents utility
├── cat.go     # Display file contents utility
├── grep.go    # Search text in files utility
├── ws.go      # Word statistics utility
├── main.go    # (Currently unused)
└── test.txt   # Sample test file
```

## How to Use

Each utility can be run independently using the `go run` command. Make sure you're in the project directory before running any commands.

## Notes

- These utilities are simplified versions of their Unix counterparts
- They serve as educational implementations to understand basic file operations in Go
- Color coding in terminal output uses ANSI escape codes

## Contributing

Feel free to contribute by:
- Adding new Unix utilities
- Improving existing implementations
- Adding more features to current utilities
- Reporting bugs or suggesting enhancements

## License

This project is open source and available for educational purposes.
