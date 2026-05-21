# Bitwise and Logical Operations

## Description

A C program for Linux that **reverses the bit order** of a 64-bit number.

Example:
```
Input:  00000000 00000000 00000000 00000000 00000000 00000000 00000000 00001101  (number 13)
Output: 10110000 00000000 00000000 00000000 00000000 00000000 00000000 00000000
```

### What the program does

1. Accepts a decimal number as an argument (or generates a random one)
2. Prints its 64-bit binary representation
3. Reverses all 64 bits
4. Prints the result in binary

### Key bitwise operations

| Operation | Used in | Purpose |
|-----------|---------|---------|
| `num >> i` | `print_binary` | Right shift — get the bit at position `i` |
| `& 1` | `print_binary` | Masking — isolate the least significant bit |
| `reversed << 1` | `reverse_bits` | Left shift — make room for the next bit |
| `\| (num & 1)` | `reverse_bits` | OR — write the LSB of the source number into result |
| `num >>= 1` | `reverse_bits` | Shift — move to the next bit |

---

## Requirements

- OS: Linux
- Compiler: `gcc`
- Build tool: `make`

---

## Build & Run

### Build
```bash
make
```

### Run with a number
```bash
./prg1pmsN3146 <number>
```

### Run without arguments (random number)
```bash
./prg1pmsN3146
```

### Clean compiled files
```bash
make clean
```

---

## Examples

![Program output example](assets/screenshot.png)

```bash
$ ./prg1pmsN3146 1
Original number in binary:
00000000 00000000 00000000 00000000 00000000 00000000 00000000 00000001 
Number after bit reversal in binary:
10000000 00000000 00000000 00000000 00000000 00000000 00000000 00000000 

$ ./prg1pmsN3146 255
Original number in binary:
00000000 00000000 00000000 00000000 00000000 00000000 00000000 11111111 
Number after bit reversal in binary:
11111111 00000000 00000000 00000000 00000000 00000000 00000000 00000000 
```

### Error handling
```bash
$ ./prg1pmsN3146 abc
Error: 'abc' is not a valid number.
```

---

## Project structure

```
Bitwise and logical operations/
├── main.c          # Source code
├── Makefile        # Build configuration
├── README.md       # Project description
└── assets/
    └── screenshot.png  # Example output
```

---

## Author

Polina — 2nd year student, ITMO University, Information Security
