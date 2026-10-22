# unix-cat

A lightweight implementation of the Unix `cat` command written in C. This project is a hands-on exercise in command-line argument parsing, file I/O, pointers, and dynamic memory management.

## Features

- Accepts one or more filenames as command-line arguments.
- Reads file contents in chunks using `fread()`.
- Uses `malloc()` and `realloc()` to manage buffers dynamically.
- Concatenates file contents in the order specified and prints them to standard output.
- Supports the `--help` option.

## Build

Requires a C compiler such as GCC.

```bash
gcc main.c -o unix-cat
```

## Usage

Print a single file:

```bash
./unix-cat file1.txt
```

Concatenate multiple files:

```bash
./unix-cat file1.txt file2.txt
```

Show help:

```bash
./unix-cat --help
```

## How it works

1. `parse_arguments()` collects filenames from `argv`.
2. `read_file()` opens each file, reads its contents into dynamically allocated memory, and returns the buffer through a `char **` parameter.
3. `main()` appends each file's contents to a growing buffer, then prints the combined result.

## Limitations

This is an educational implementation, not a full replacement for the Unix `cat` utility.

## License

No license has been specified yet.
