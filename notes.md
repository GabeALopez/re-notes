# Registers Notes
Register Definitions:

- EAX - Accumulator for operands and results
- EBX - Pinter to data in the DS segment
- ECX - Counter for string and loop operations
- EDX - I/O pointer
- ESI - Source pointer for string operations
- EDI - Destination pointers for string operations
- ESP - Stack pointer
- EBP - Pointer to data on the stack

String Registers:
- ECX
- ESI
- EDI

General Purpose: 
- EAX
- EBX
- ECX
- EDX
- ESI
- EDI
- EBP
- ESP

# C/C++ Notes
- stdin - file descriptor 0
- stdout - file descriptor 1
- stderror - file descriptor 2
---
This type of casting is dangerous as it can interpret ascii and numbers as integers:

int* ip = (int*)p; //Where p is a character array

- The code above was used to take a 20 byte string and converting it into 5 integers. 
- 4 characters for were used in each section of the string to make the integer.
---

When hitting the 32 bit limit of a int the bits will invert a int value that is negative. 

---
When causing a collision can input bytes directly in the arguement
ex: ./col "`python -c "print '\xc8\xce\xc5\x06'*4+'\xcc\xce\xc5\x06'"`"

---


## GDB Notes
When first compiling the code use the following command:
gcc -ggdb {fileName} -o {fileName output}

To set arguments:

set args {input}
ex: set args 25

commands:
1. TUI enable
2. break main
3. start
4. step - go one line
5. next - go over a line
6. continue - continue until break point

# Linux Command Notes

SCP command:
- template: scp {file name} {Username}@{IP address}:{Directory} {location on local machine} 
- ex: scp file.txt remoteUsername@10.10.0.2:/remote/directory ./ 
