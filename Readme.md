# Rust Grep

This is a very simple implementation of the basic functionality of the `grep` command-line tool using Rust.

## Requirements

To compile and run this project, you will need to have Rust installed on your system. You can download and install Rust from the official website: https://www.rust-lang.org/tools/install

## Usage

To use this program, you will need to provide two arguments:

- The search string: The string you want to search for.
- The file path: The path to the file you want to search in.

By default, the search is case-sensitive. However, you can ignore case by either:

- Setting the `IGNORE_CASE` environment variable to a non-empty value.
- Passing the `--ignore-case` flag when running the program.

If both options are used, the `--ignore-case` flag takes precedence.

To run the program with case-sensitive search, you can use one of the following commands:

```
# Option 1: Run the base command
cargo run -- <search string> <file path>
```

To run the program with case-insensitive search, you can use one of the following commands:

```
# Option 1: Set the IGNORE_CASE environment variable
IGNORE_CASE=1 cargo run -- <search string> <file path>

# Option 2: Pass the --ignore-case flag
cargo run -- <search string> <file path> --ignore-case
```

For example, if you want to search for the word "hello" in the file `example.txt` ignoring case, you would run the following command:

```
# Option 1
IGNORE_CASE=1 cargo run hello example.txt

# Option 2
cargo run -- hello example.txt --ignore-case
```

## Example

Suppose we have a file named `example.txt` that contains the following lines:

```
Hello, world!
This is a test.
This is only a test.
```

If we want to search for the word "test" in the file, ignoring case, we would run the following command:

```
# Option 1
IGNORE_CASE=1 cargo run test example.txt

# Option 2
cargo run -- test example.txt --ignore-case
```

The output would be:

```
This is a test.
This is only a test.
```

## License

This project is licensed under the terms of the MIT license. See the LICENSE file for more details.
