# minigrep

A simple, minimal implementation of the classic command-line search tool `grep`, written in Rust as a learning exercise from Chapter 12 of *The Rust Programming Language* book. This tool, `minigrep`, is a basic example and not intended for production use; it’s designed to help Rust learners practice working with file I/O, error handling, and command-line arguments.

## Overview

`minigrep` reads a specified file and searches for a provided string, printing each line that contains the string. It demonstrates several core Rust concepts and patterns, including:

- Organizing code effectively
- Using vectors and strings to manage data
- Handling errors gracefully
- Applying traits and lifetimes where needed
- Writing unit tests to validate functionality

Additionally, `minigrep` introduces some common command-line tool features, such as using environment variables to configure behavior and printing error messages to the standard error stream (stderr).

> **Note:** For a fully-featured and optimized Rust-based search tool, consider using [ripgrep](https://github.com/BurntSushi/ripgrep) by Andrew Gallant.

## Features

- Search for a string in a file, displaying each matching line
- Optional case-insensitive search using an environment variable (`IGNORE_CASE`)
- Basic error handling for missing files or incorrect input

## Usage

### Prerequisites

- [Rust](https://www.rust-lang.org/tools/install) installed on your system

### Running minigrep

To run `minigrep`, clone this repository and build the project:

```sh
# Clone the repository
git clone https://github.com/your-username/minigrep.git
cd minigrep

# Build the project
cargo build

# Run minigrep with search term and file path
cargo run <search_term> <file_path>
```

### Example

Assuming you have a file `example.txt` with some content:

```sh
cargo run to example.txt
```

This command will print each line in `example.txt` that contains the word "to".

### Case Insensitive Search

Set the `IGNORE_CASE` environment variable to perform a case-insensitive search:

```sh
IGNORE_CASE=1 cargo run to example.txt
```

## Project Structure

This project consists of a single Rust module with the following key files:

- `src/main.rs`: Contains the main logic for parsing arguments and handling file I/O.
- `src/lib.rs`: Contains helper functions for search functionality, which are organized to support unit testing.
- `tests`: Includes tests for various functions in the library.

## Concepts Practiced

`minigrep` builds on several foundational Rust topics:

- **File I/O**: Reading from files and handling different types of errors.
- **Error Handling**: Using Rust’s `Result` and `Option` types to manage errors gracefully.
- **Command-line Argument Parsing**: Retrieving command-line arguments using Rust's standard library.
- **Environment Variables**: Using environment variables to modify the program's behavior.
- **Testing**: Writing unit tests to verify the correctness of individual functions.

## Limitations

This project is intentionally simple, focusing on learning rather than performance. The search is basic and doesn’t support advanced regular expressions. For more powerful and optimized searching capabilities, consider using [ripgrep](https://github.com/BurntSushi/ripgrep).

## Contributing

This project is designed as a learning exercise, so contributions are primarily for educational purposes. Feel free to fork the project and modify it as part of your Rust learning journey.
