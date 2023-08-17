get_next_line Project Documentation


In this project, you'll implement the get_next_line function that reads a line from a file descriptor and returns it. The function should work with both files and standard input. Your implementation should adhere to certain guidelines and include helper functions.

Table of Contents
Common Instructions
Mandatory Part
Function get_next_line
Bonus Part
Common Instructions
Your project must be written in C.
Follow the Norm: Coding style and rules.
Functions should not quit unexpectedly (segmentation fault, bus error, double free, etc).
Properly free all heap allocated memory.
Include a Makefile for compilation with flags -Wall, -Wextra, and -Werror.
Your Makefile should contain rules for $(NAME), all, clean, fclean, and re.
Encourage the creation of test programs for your project.
Mandatory Part
Function get_next_line
You are required to implement the get_next_line function that reads a line from a given file descriptor and returns it. The function has the following prototype:

c
Copy code
char *get_next_line(int fd);
Parameters
fd: The file descriptor to read from.
Return Value
Read line: Returns the line that was read, including the terminating newline character (\n).
NULL: Returns NULL if there is nothing else to read or if an error occurred.
External Functions
read
malloc
free
Description
The function should work with both files and standard input.
Repeated calls to get_next_line should allow you to read the text file pointed to by the file descriptor one line at a time.
The returned line should include the terminating \n character, except if the end of file was reached and does not end with a \n character.
Your header file get_next_line.h must contain at least the prototype of the get_next_line() function.
Helper functions should be included in the get_next_line_utils.c file.
Buffer Size
To define the buffer size for read(), add the option -D BUFFER_SIZE=n to your compiler call:

shell
Copy code
cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 <files>.c
The buffer size value will be modified during testing.

