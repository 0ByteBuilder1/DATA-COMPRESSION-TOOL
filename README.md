# RLE Compression Tool in C

**Author:** Yes Chandra
**Intern ID:** CT06DH337
**Company:** CODTECH IT SOLUTIONS
**Mentor:** Neela Santosh
**Domain:** C Programming
**Duration:** 4 Weeks


---

## Overview

A simple command-line Run-Length Encoding (RLE) compression tool written in C. The tool allows you to compress or decompress text files using a basic form of lossless data compression.

---

## Features

* Compresses repeated characters into a compact format (e.g., `aaaaa` → `#a5`)
* Decompresses previously compressed files back to their original form
* Uses marker character (`#`) for encoding runs
* Handles character-level reading and writing
* Avoids compressing short runs (3 or fewer characters)
* Preserves all file content that doesn’t benefit from compression

---

## Technologies Used

* C Language
* Standard Libraries: `stdio.h`, `stdlib.h`, `string.h`, `ctype.h`

---

## File Structure

```
rle_tool.c           # Main source file  
output.txt            # Sample input file (for compression or decompression)  
README.md            # Documentation  
```

---

## Compile & Run

```bash
gcc rle_tool.c -o rle
./rle
```

Follow the prompts to choose an option:

1. Compress file  
2. Decompress file  
3. Exit

You'll be asked to enter input and output file names.

---

## Example

**Input (input.txt):**
```
aaaaabbbcccd##dddd
```

**Compressed Output (output.txt):**
```
#a5#b3#c3d##d4
```

**Decompressed Output (decompressed.txt):**
```
aaaaabbbcccd##dddd
```

---

## Key Learnings

* Implementing Run-Length Encoding from scratch
* Working with file I/O in C
* Using `ungetc()` for precise character parsing
* Handling edge cases in compression (like escaping `#`)
* Basic command-line tool design

---

## Limitations

* Only works with plain text files
* Compression benefits are best with large repeating sequences
* `#` is treated as a special escape character; it will always be encoded even once

---


