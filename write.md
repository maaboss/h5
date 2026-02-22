CTF Write-Up: Debugging and Recovering the Flag Using GDB
Objective

The goal of this challenge was to analyze a crashing binary (gdb_example1) and determine the hidden message (flag) using debugging techniques.

Step 1 – Compilation with Debug Symbols

The binary was compiled using:

gcc -o gdb_example1 -Wall -std=c99 gdb_example1.c -g

The -g flag ensured debugging symbols were included, allowing source-level inspection inside GDB.

Step 2 – Running the Program in GDB

The program was executed inside GNU Debugger:

gdb ./gdb_example1
run

The output was:

Khoor/#zruog1

Immediately after printing this, the program crashed with:

Program received signal SIGSEGV, Segmentation fault.
print_scrambled (message=0x0)

This indicated a null pointer dereference.

Step 3 – Inspecting the Crash

Using:

You handled your first crash-analysis CTF correctly.
