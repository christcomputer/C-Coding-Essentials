# C Programming

* **Print Hello World in C**
  
```
#include <stdio.h>
#include <stdlib.h>

int main(void) {
	puts("!!!Hello World!!!"); /* prints !!!Hello World!!! */
	return EXIT_SUCCESS;
}
```
This is a C program that prints “!!!Hello World!!!” to the standard output stream. Here is a line-by-line explanation of the code:

* #include <stdio.h>: This is a preprocessor directive that tells the compiler to include the header file stdio.h, which contains the declarations of input/output functions such as printf() and puts().
* #include <stdlib.h>: This is another preprocessor directive that tells the compiler to include the header file stdlib.h, which contains the declaration of the macro EXIT_SUCCESS, which represents a successful termination of the program.
* int main(void): This is the definition of the main function, which is the entry point of the program. The int keyword specifies the return type of the function, which is an integer. The void keyword inside the parentheses indicates that the function takes no arguments.
* puts("!!!Hello World!!!");: This is a function call that prints the string “!!!Hello World!!!” followed by a newline character to the standard output stream, which is usually the console or the terminal. The puts() function is defined in the stdio.h header file.
* return EXIT_SUCCESS;: This is a return statement that ends the execution of the main function and returns the value of EXIT_SUCCESS to the operating system. The EXIT_SUCCESS macro is defined in the stdlib.h header file and has a value of 0, which indicates a successful termination of the program
