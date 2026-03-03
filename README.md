# c2bat
Compile c code to windows batch files.

To use, extract c2bat.zip. Modify test.c, run build.sh, and then run final.bat with windows command prompt. You also need mem_init.bat in the same directory as final.bat.

For test.c, you must include "std.h" at the top of the file. You cannot use any other standard libraries. The main function must begin with ENTRY (defined in std.h). Use puti(int) to print an integer. Use poparg(int) to get an argument passed to the batch file (1 through 9). Note that if the argument was not passed, undefined behavior may occur. Use puts(string) to print a string. The string must end with a semicolon (;). You may only use characters a-z A-Z 0-9. See the provided test.c for an example program.

std.bat can be modified to allow for more library functions.

It works by compiling the c to riscv with gcc, and then translating the riscv assembly into batch. You will need the necessary dependencies for working with riscv in gcc.
You need: riscv64-unknown-elf-gcc, riscv64-linux-gnu-objdump, riscv64-unknown-elf-objdump
