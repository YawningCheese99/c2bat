# c2bat
Compile c code to windows batch files.

To use, extract c2bat.zip. Modify test.c, run build.sh, and then run final.bat with windows command prompt.

For test.c, you must include "std.h" at the top of the file. No standard libraries are included. Use puti(int) to print an integer. Your main function must begin with ENTRY (defined in std.h). See the provided test.c for an example.

It works by compiling the c to riscv with gcc, and then translating the riscv assembly into batch. You will need the necessary dependencies for working with riscv in gcc.
