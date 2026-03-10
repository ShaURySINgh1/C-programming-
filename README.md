# C-programming-
# C Programming Absolute Beginner’s Guide Third Edition

## Part 1 What Is C Programming, and Why Should I Care

### Compiler

C is more efficient than most programming languages. It is also a relatively small programming language.
In other words, you don't have to learn many commands in C.

All C program filenames end in the .c file extension.

your source code is like the raw materials that your computer needs.
The compiler is like a machine that converts those raw materials to a final product,
a compiled program that the computer can understand.

Before you can write and execute a C program on your computer, you need a C compiler.
The C compiler takes the C program you write and builds or compiles it
(technical terms for making the program computer-readable),
enabling you to run the compiled program when you're ready to look at the results.

Because of the many possible versions of C, a committee known as the American National Standards
Institute (ANSI) committee developed a set of rules (known as ANSI C) for all versions of C.
As long as you run programs using an ANSI C compiler,
you can be sure that you can compile your C programs on almost any computer that has an ANSI C compiler.

In 1983, ANSI created the X3J11 committee to set a standard version of C.
This became known as ANSI C. The most recent version of ANSI C, C11, was formally adopted in 2011.

As soon as you compile a C program, you can run the compiled program on any computer that is
compatible with yours, whether or not the computer has an ANSI C compiler.

### Conventions

C isn't picky about everything.

Put lots of extra spacing in your C programs, to make them more readable.

For instance, most of the spacing you see in C programs makes the programs clearer to people, not to C.
As you program, add blank lines and indent sections of code that go together
to help the appearance of the program and to make it easier for you to find what you are looking for.

C requires that you use lowercase letters for all commands and predefined functions.
About the only time you use uppercase letters is on a line with #define and inside the printed messages you write.

Don't put leading zeroes before integers unless the integer is zero.

Integers are whole numbers without decimal points. Floating-point numbers have decimal points.

If you use a character, enclose it in single quotes. Strings go inside quotation marks.

Every C command and function needs a semicolon `;` after it to let C know that the line is finished.
Braces and the first lines of functions don't need semicolons because nothing is executing on those lines.

### `main()`

Although at this point the distinction is not critical, `main()` is a C function, not a C command.
Each program must always include a main() function.

These are functions: `main()` `calcIt()` `printf()` `strlen()`
and these are commands: `return` `while` `int` `if` `float`

One of the functions just listed, `calcIt()`, contains an uppercase letter.
However, the preceding section said you should stay away from uppercase letters.
If a name has multiple parts, as in `doReportPrint()`,
it's common practice to use uppercase letters to begin the separate words, to increase readability.
(Spaces aren't allowed in function names.) Stay away from typing words in all uppercase,
but an uppercase letter for clarity once in a while is okay.

The required `main()` function and all of C's supplied function names must contain lowercase letters.
You can use uppercase for the functions that you write, but most C programmers stay with the
lowercase function name convention.

Just as the home page is the beginning place to surf a website, `main()` is always the first place the
computer begins when running your program.

Even if `main()` is not the first function listed in your program,
`main()` still determines the beginning of the program's execution.

Therefore, for readability, make `main()` the first function in every program you write.
adding functions after `main()` improves your programming power even more.

C executes `main()` before any other function.

## Data Types

### Characters and C

the following three data types are by far the most common used in C programming:
• Characters
• Integers
• Floating points (also called real numbers)

A C character is any single character that your computer can represent. Your computer knows 256
different characters.
Each of them is found in something called the ASCII table.
The American National Standards Institute (ANSI), which developed ANSI C,
also developed the code for the ASCII chart.

As you can see, every letter, number, and space is a character to C. Sure, a `4` looks like a number,
and it sometimes is, but it is also a character. If you indicate that a particular `4` is a character,
you can't do math with it.

The plus sign (`+`) is a character, but the plus sign also performs addition.

All of C's character data is enclosed in apostrophes (`'`).
Some people call apostrophes single quotation marks.
Apostrophes differentiate character data from other kinds of data, such as numbers and math symbols.

For example, in a C program, all of the following are character data:
`'A'` `'a'` `'4'` `'%'` `' '` `'-'`

None of the following can be character data because they have no apostrophes around them:
`A` `a` `4` `%` `-`

If you need to specify more than one character
(except for the special characters that you'll learn, like the `\n` just described),
enclose the characters in quotation marks (`"`).
A group of multiple characters is called a string. The following is a C string:
`“C is fun to learn.”`

`\n` is a single character, but it's one of the few two-character combinations that C interprets as a single character

```c
char name[] = "ehsan";
printf("01- my name is %s\n", name);
```

### `printf()`

No actual command performs output, but the `printf()` function is a part of every C compiler and one of
the most used features of the language. `printf()` sends characters, numbers, and words to the screen.

The format is the general look of the statement. If something in a format appears in brackets,
such as , data in the printf function just shown, that part of the statement is optional. You
almost never type the brackets themselves. If brackets are required in the command, that is made clear
in the text following the format. `printf()` requires a controlString, but the data following the
controlString is optional.

`printf()` doesn't actually send output to your screen, but it does send it to your
computer's standard output device. Most operating systems, including Windows, route
the standard output to your screen unless you know enough to route the output
elsewhere. Most of the time, you can ignore this standard output device stuff because
you'll almost always want output to go to the screen. Other C functions you will learn
about later route output to your printer and disk drives.

The Format of `printf()`:

```c
printf(controlString [, data]);
printf("You are on your way to C mastery");
```

The string (You are on your way to C mastery) is the controlString in this `printf()`.

`printf()` requires a controlString, but the data following the controlString is optional.

Because every string in C must be enclosed in quotation marks, the
controlString must be in quotation marks. Anything following the controlString is
optional and is determined by the values you want printed

All statements with `printf()` should end in a semicolon. You won't see semicolons after `main()`,
however, because you don't explicitly tell C to execute `main()`. You do, however, tell C to execute `printf()`
and many other functions. As you learn more about C, you'll learn more about
semicolon placement.

C does not automatically move the cursor down to the next line when a `printf()`
executes. You must insert an escape sequence in the controlString if you want C
to go to the next line after a `printf()`.

The statement `#include <stdio.h>` is needed in almost every C program.

It helps with printing and getting data.

That's because almost every program in this book uses `printf()`
The file you include is called a header file. That's why most included files end in the extension `.h`

### Escape Sequences

The term escape sequence sounds harder than it really is. An escape sequence is
stored as a single character in C and produces the effect described in Table 4.1. When
C sends '`\a`' to the screen, for example, the computer's bell sounds instead of the
characters \ and a actually being printed.

C contains a lot of escape sequences, and you'll use some of them in almost every program you write.
Here is a list of some of the more popular escape sequences.

| (Escape sequence) (Hex value in ASCII) | (Character represented) | Alert (Beep, Bell) [added in C89](1)                                          |
| -------------------------------------- | ----------------------- | ----------------------------------------------------------------------------- |
| \a                                     | 07                      | Backspace                                                                     |
| \b                                     | 08                      | Escape character                                                              |
| \e                                     | 1B                      | Formfeed Page Break                                                           |
| \f                                     | 0C                      | Newline (Line Feed); see notes below                                          |
| \n                                     | 0A                      | Carriage Return                                                               |
| \r                                     | 0D                      | Horizontal Tab                                                                |
| \t                                     | 09                      | Vertical Tab                                                                  |
| \v                                     | 0B                      | Backslash                                                                     |
| \\                                     | 5C                      | Apostrophe or single quotation mark                                           |
| \'                                     | 27                      | Double quotation mark                                                         |
| \"                                     | 22                      | Question mark (used to avoid trigraphs)                                       |
| \?                                     | 3F                      | The byte whose numerical value is given by nnn interpreted as an octal number |
| \nnn                                   | any                     | The byte whose numerical value is given by hh… interpreted as a hex number    |
| \xhh…                                  | any                     | Unicode code point below 10000 hexadecimal                                    |
| \uhhhh                                 | none                    | Unicode code point where h is a hexadecimal digit                             |
| \Uhhhhhhhhn                            | none                    | Unicode code point where h is a hexadecimal digit                             |

Double quotation marks begin and end a string, single quotation marks begin and end a character, and
a backslash signals the start of an escape sequence, so they have their own escape sequences if you
need to print them.

`\a` rings your computer's bell, `\b` moves the cursor back a line, and `\t` causes the
output to appear moved over a few spaces.

These three lines show you how to use the most popular Escape Sequences

```c
printf("Column A\tColumn B\tColumn C");
printf("\nMy Computer\'s Beep Sounds Like This: \a!\n");
printf("\"Letz\bs fix that typo and then show the backslash ");
printf("character \\\" she said\n");
```

RESULT:

```text
Column A    Column B    Column C
My Computer's Beep Sounds Like This: !
"Let's fix that typo and then show the backslash character \" she
said

```

You should understand a few things about the previous listing.
First, you must always place `#include <stdio.h>` at the beginning of all programs that use the
`printf()` function—it is defined in `stdio.h`,
so if you fail to remember that line of code,
you will get a compiler error because your program will not understand how to execute `printf()`.

Also, different C/C++ compilers might produce a different number of tabbed spaces for the `\t` escape sequence.

Finally, it is important to note that using the `\b` escape sequence overwrites anything that was there.

That's why the '`z`' does not appear in the output, but the '`s`' does.

## Commenting on Your Code

You will change your programs often, and if you write programs for a company,
the company's needs will change over time.
You must ensure that your programs are understandable to people as well as to computers.
Therefore, you should document your programs by explaining what they do.

Even if you write the program, you aren't always able to follow it later—
you might forget why you wrote a particular chunk of code,
so a comment will help to decipher matters.
Add comments as you write your programs. Get in the habit now,
because programmers rarely go back and add comments later.

you can scan through your comments, finding sections of code that you need faster.

If you didn't comment, you would have to decipher your C code every time you looked through a piece of it.
Comments are not C commands. C ignores every comment in your program.

Comments are for people, and the programming statements residing outside the comments
are for the computer.

The closer a comment is to spoken language and the further a comment is from C code,
the better the comment is.

Redundant comments are a waste of your time, and they don't add anything to programs.
Add comments to explain what is going on to people (including yourself)
who might need to read your program.

Many companies require that their programmers embed their own names in comments at the top of
programs they write.
If changes need to be made to the program later, the original programmer can be found to help.

It's also a good idea to include the filename that you use to save the program on disk at
the beginning of a program so that you can find a program on disk when you run across a printed
listing.

### C comments begin with /_and end with_/

Today's C compilers support another kind of comment that was originally developed for C++
programs.

With its C99 release, the American National Standards Institute (ANSI) committee
approved this new kind of comment, so you should be safe using it

(unless you are using a really, really old computer and compiler!).

The second style of comment begins with two slashes (`//`) and ends only at the end of the line.

## Numbers in C

Whole numbers are called integers.

Integers have no decimal points.

(Remember this rule: Like most reality shows, integers have no point whatsoever.)

Any number without a decimal point is an integer.
All of the following are integers:
`10` `54` `0` `–121` `–68` `752`

Don't use a comma in a number, no matter how big the numbers are!
Enter the figure 100,000 as `100000`, not 100,000.

Never begin an integer with a leading `0` (unless the number is zero),
or C will think you typed the number in hexadecimal or octal.

Hexadecimal and octal, sometimes called base-16 and base-8, respectively,
are weird ways of representing numbers.

`053` is an octal number, and `0x45` is a hexadecimal number. If you don't know what
all that means, just remember for now that C puts a `hex` on you if you mess around with
leading zeroes before integers.

Numbers with decimal points are called floating-point numbers. All of the following are floatingpoint numbers:
`547.43` `0.0` `0.44384` `9.1923` `–168.470` `.22`
As you can see, leading zeroes are okay in front of floating-point numbers.

Different C compilers use different amounts of storage for integers and floating-point values.
a floating-point value usually takes twice as much memory as an integer.

Therefore, if you can get away with using integers, do so—
save floating points for values that need the decimal point.

The size of C's number storage is affected not by the value of the number, but by the type of the number.

For representing floating point numbers, we use float, double and long double.

What's the difference?

Double has 2x more precision then float.

| We have 3 float data types:         |          |         |
| ----------------------------------- | -------- | ------- |
| 1. Single float (float)             | 4 bytes  | 32 bits |
| 2. Double float (double)            | 8 bytes  | 64 bits |
| 3. Long Double float. (long double) | 10 bytes | 80 bits |

float is a 32 bit IEEE 754 single precision Floating Point Number1 bit for the sign,
(8 bits for the exponent, and 23\* for the value), i.e. float has 7 decimal digits of precision.

double is a 64 bit IEEE 754 double precision Floating Point Number
(1 bit for the sign, 11 bits for the exponent, and 52\* bits for the value), i.e.
double has 15 decimal digits of precision.

When you print numbers and characters, you must tell C exactly how to print them. You indicate the
format of numbers with conversion characters. Here is a few of C's most-used conversion characters.

| Conversion Character | Displays Argument (Variable's Contents) As            |
| -------------------- | ----------------------------------------------------- |
| %c                   | Single character                                      |
| %d                   | Signed decimal integer (int)                          |
| %e                   | Signed floating-point value in E notation             |
| %f                   | Signed floating-point value (float)                   |
| %g                   | Signed value in %e or %f format, whichever is shorter |
| %i                   | Signed decimal integer (int)                          |
| %o                   | Unsigned octal (base 8) integer (int)                 |
| %s                   | String of text                                        |
| %u                   | Unsigned decimal integer (int)                        |
| %x                   | Unsigned hexadecimal (base 16) integer (int)          |
| %%                   | (percent character)                                   |

```c
printf("%d roses cost %.2f per %d\n", 24, 19.95, 12);
// 24 roses cost 19.5 per 12
// 24            19.5     12
printf("%s %d %c %f\n", "Sam", 14, 'X', -8.76);
// Sam 14 X -8.760000
// Sam 14 X -8.760000
```

When you want to print a value inside a string, insert the appropriate conversion characters in the
controlString. Then to the right of the controlString, list the value you want to be printed.

The string Sam needs quotation marks, as do all strings, and the character X needs
single quotation marks, as do all characters.

You can control how C prints floating-point values by placing a period (`.`) and a number between the
`%` and the f of the floating-point conversion character.

The number you place determines the number of decimal places your floating-point number prints to.

The following `printf()` produces four different-looking numbers,
even though the same floating-point number is given:

The only reason two spaces appear between the numbers is that the controlString has two spaces between each `%f`.

C rounds the floating-point numbers to the number of decimal places specified in the `%.f` conversion
character and produces this output:

```c
printf("%f\n", 3.1234567);   // 3.123457
printf("%f\n", 3.12345678);  // 3.123457
printf("%f\n", 3.12345);     // 3.123450

printf("%.f\n", 3.1234567);  // 3
printf("%.1f\n", 3.1234567); // 3.1
printf("%.2f\n", 3.1234567); // 3.12
printf("%.3f


# C Programming Notes

## C Program Format:

A C program is first converted to machine language for execution by a C Compiler. The compiler expects a certain (strict) structure for the C program to follow - Standard format.

C files must be saved in a file whose extension is `.c` (Ex: `hello.c`)

Basic Format:
```
#include <stdio.h>
int main() {
    // Your code ...
}
```

### What is `#include <stdio.h>`

`#` prefixed lines are known as Preprocessor Directives: They give some instructions to the compiler.

`#include` is a preprocessor directive that asks the compiler to 'Include' the mentioned source before executing the current program further.

`#include <stdio.h>` : 'stdio.h' is a file that is a library of functions mainly to do with 'standard input output'. This library is included in most C programs in order to display/receive input. It is a Standard Library available to all programs.

Examples of functions contained in `stdio.h`:
- scanf() : Function used to scan or receive input. (Read in input from user)
- printf() : Function used to print or display the output. (Outputs to screen)

### What is `int main()`:

`main()` : It is a type of function. 

A function is a block of code that takes in input & produces output. It can be called by other pieces of code (Ex: Called from other functions). A 'function body' refers to the set of statements inside the function (Within {}) that gets executed when that particular function is called.

`main()` : It is a special type of function. When a C program is run, it starts executing from the first line of the main() function. Hence, `main()` is a **mandatory** function in all C programs. It takes NO inputs & produces an Integer (int) output.  

### C Comments:

Comments are sections of code that are not executed or compiled. These are for the programmers to document parts of the code - to help with debudding later or for when multiple developers work on the same code.

- `// This is a single line comment` : Single line comments start with `//` and to the end of the line.
- `/* Some comment */` : This is used as a block or multiline comment. 

```
/* This
is also a 
multiline comment
*/
```

### Variables:

Variables are containers that store values of different types of data. Ex: `int a = 5;` declares a variable 'a' to be an integer variable and initialises it to hold the value 5 (5 is an integer value).

## C Data Types:

Data types define what is the type of the value that we are dealing with. Literals and variables in the C program are classified based on their type.

### Integer Data Types:

`int` is the keyword for Integer Data Types.

There are 3 main integer data types. 
- `short`: Usually about 2 bytes long on most systems.
- `int`  : Usually about 2 or 4 bytes long on most systems. (Minimum 2 bytes)
- `long` : Usually about 4 or 8 bytes long on most systems. (Minimum 4 bytes)

The range of values for each type:
- The range of values for any integer type is `-2^(n - 1)` to `2^(n - 1) - 1` where n is the number of bits assigned to that data type.
- The reason it is not `2^n` is because 1 bit will be used to represent the sign of the value(+/-). (Most systems follow 2's - complement representation)
- Ex: Range for `short` is `-2^15` to `2^15 - 1` since short is 2 bytes, which is 16 bits. (-32768 to 32767)

#### What happens of you exceed the limits of the ranges:

You get wrong values. Ex: 32767 + 1 will give you -32768 in `short` type. Ex2: 32767 + 10 will give you -32758 in `short` type.

Condition is called `Overflow`.

#### Syntax for `short` declaration:

To declare a short integer 'a': `short int a;` or simply `short a;`

#### Syntax for `int` declaration:

To declare a integer 'a': `int a;`

#### Syntax for `long` declaration:

To declare a long integer 'a': `long int a;` or simply `long a;`

#### Unsigned Integers:

We know that one bit in every integer type is kept to save the sign of the value. What if we know that the integer is always going to be **positive** only? In that case we can tell the compiler to free the greatest bit from saving the sign of the integer and effectively increase the range of the data type from `0` to `2^n - 1` where n is the number of bits for that type.

Keyword used to define only positive integers: `unsigned`

Examples:
- `unsigned short a;` : is having a range between 0 and 65535.
- `unsigned int a;` : an unsigned integer.
- `unsigned long a;` : an unsigned long integer.

Note:
- The total values in the unsigned range is the same as in the signed range. Only difference is that the range starts from 0 in unsigned and moves in the positive direction.
- The default is `signed` but we do not have to prefix it before any integer data type (since it's the default).

### Floating Point Data Types:

There a 3 Floating point data types:
- `float` : Usually holds 4 bytes of data
- `double` : Usually holds 8 bytes of data
- `long double` : Usually holds 10 bytes of data

These data types store their values in Scientific Notation (Mantissa & Exponent form). Reason: Storing decimal pointed values is somewhat complicated.

#### Declaration Syntaxes:
- `float a;` 
- `double a;` 
- `long double a;` 

### Text Data Types:

In C, we use the `char` data type to store a single character.

Ex:
- `char a, b, c;`
- `char a = 'A';`

A character data type is only 1 byte long. The character must be enclosed withing **Single Quotes**. 

#### How can we store a character?:

Since machines can only store numeric values, stored in binary, how can we represent text/symbols/characters?

The characters are actually mapped to integers which are then stored in binary in the computer whenever we use `char`. The mappings are defined by standards such as `ASCII` and nowadays (on more modern systems)by `UTF-8`. Therefore, we can replace the character with the corresponding integer associated with it while storing it. Ex:
- `char a = 'A';` : Stores the character 'A'
- `char a = 65;` : Also stores the character 'A' since it is mapped to the integer 70 in the ASCII table.

Note: 
- `char` can be thought of as a subset to the `short` integer type since it can hold 1 byte(8 bits) or 256 integer values (0 to 255) and the symbol stored in it maps to one of these integer values.
- Hence, **Arithmetic Operations** can be performed on following data types: INTEGERS, FLOATING POINTS & CHARACTERS. **Imp!** 

Ex:
```
char x, y;
int z;
x = 'a'; // Integer equivalent is 97
y = 'b'; // Integer equivalent is 98
z = x + y; // Will be 97 + 98 = 195
printf("%d", z); // 195
printf("%c %c", x, y); // 97 98 => %c is a formatter to char type. (Reverse map to char)
```

** Fill notes here > Control Structures **

## C Functions:

- A function is a self-contained block or code which does a particular task.
- It contains statements that perform that particular task.
- It may take in input (information) in order to execute.
- It may also return information after it has finished running.

Note: 
- Functions can call other functions and also call themselves.
- C programming follows IMPERATIVE programming paradigm (C++ & Java follow OO paradigm. There is also a Functional Programming paradigm that is quite popular).

Advantages of functions:
- Breaks code into manageable units which are reusable.
- Helps keep code clean and readable.
- Can help with delegating work (as separate tasks).

### Library vs Functions:

- Libraries are essentially collections of functions. But, they are written by other developers and made available for us to use.
- `printf` and `scanf` are examples of readily available functions from the `stdio` library.
- User-defined functions (functions written by us) are the most useful parts of our own programs.

### Anatomy of a function:

Declaring a function: Announcing that a function exists, specifying the kind of input it takes and what output we should expect from it. (Signature of a function)

Definition of a function: Exactly what the function does. The meat of the function that contains all the statements of the function.

Call to a function: When we interact with a function (by passing it input) and ask it to accomplish its task (and wait for an output) it is referred to as a function 'call'.

Function Definition:
```
<return-type> <function-name>(<arguments-list>) {
	// Function Statements (Also known as the FUNCTION BODY)
}
```

- `<return-type>` : Type of information returned by the function. If function returns nothing then the return type is specified as `void`. Else, it is one of the C data types including user-defined types such as structs, pointers, etc.
- `<function-name>` : Way to identify a function in order to call it (so that it executes its statements). Function names can contain Letters of the alphabet(A-Z or a-z), Numbers(0-9) and Underscore(_) but it cannot start with a Number. Ex: `void echo_1_func()`, `int _convertToRs(int currency)`
- `<arguments-list>` : This is the list of the inputs expected by the function. Format: Data type followed by a name for the variable that is going to hold the passed value. It can be Zero or more and are separated by commas(,) while being enclosed within parentheses. Ex: `void _fun1(int num)`, `int add(int num1, int num2)`, `int floor(double _rawInput)`.

Note: 
- In C, two functions cannot have the same name even they have different return types or different arguments list. In contrast, in C++ or Java, the functions can have the same name as long as their return types or argument(s) lists differ.
- To return a value from within a function, use the `return` command to which we must pass a value. Ex: `return 5;`, `return num`. The value returned must match with the return type of the function.

The return-type, function-name and arguments-list constitute the 'function signature'.

Function Call:
```
...
int sum = add(a, b);
...
```

While calling a function:
- We are asking the function to accomplish its task.
- We can pass it arguments which must match those in the function signature or definiton in order, data types and number of arguments. (If pass by value then arguments are usually: Variables or literals)
- The returned value of the called function can be saved in a variable. The type of the variable holding the returned value should match the return type of the function. Ex: `float fun() { ... }` matches return type with `float x = fun();`

Function Declaration:
- Before we can call a function, it has to be declared first. It is like saying 'this functin exists and can be called by other code'.
```
<return-type> <function-name>(<arguments-list>);
```

Note: The arguments list in the declaration need not contain the associated variable names (Optional) (But, in the definition they should have names - known as formal parameters). Ex. of function declaration: `int sum(int, int);`, `int sum(int a, int b)` (with variable names).

Note:
- Formal parameters - The variables in the arguments list in the function definition (Act as local variables - see scope).
- Actual parameters - The actual values passed to the function through a function call. Ex: `int sum = add(a, 5);`. The formal parameters receive these particular values when the function is called/invoked.

### Putting it All Together:

We must: 
- Declare a function.
- Define a function.
- Call a function. (In that order)

Ex:
```
int add(int, int);

int add(int a, int b) {
	return a + b;
}

int main() {
	...
	int sum = add(x, y);
	...
}
``` 

### Why have Separate Declarations and Definitions:

The reason is because the declarations usually go into Header Files (with `.h` extension) while the definitions go into Source Files(with `.c` extensions). Hence, they have to be separated.

### Parameter Passing: By-Value vs By-Reference:

In C, there are two ways by which we can pass data or inputs to a function:
- Pass by Value, or
- Pass by Reference

Pass by Value: Ex:
```
int main() {
	int a = 50, b = 100;
	func(a, b);
	printf("%d %d", a, b); // 50 100 (Unaffected by execution of 'func')
}
...
void func(int x, int y) { 
	printf("%d %d", x, y); // 50 100
	x = 1;
	y = 2;
	printf("%d %d", x, y); // 1 2
}
```

In pass by value, the actual parameter values are copied to the formal parameters. Changing formal parameter values inside the function will not affect the values of the values of the actual variables passed to it. (Note: Even if the formal and actual parameters have the same variable names, they are still different - formal parameters are local to the called function).

Pass by Reference: Uses pointers to achieve this. We pass the address of the location where the variables' values are stored. Therefore, changing the values of formal parameters will affect the actual parameters/values at the specified addresses (See pointers section).

## Storage Classes in C:

We can create variables with different 'settings' such as:
- Where the variable would be stored.
- Default value for the variable.
- Scope of the variable.
- Life of the variable.

These settings are governed by what is known as the variable's 'Storage Class'.

Tnere are 4 storage classes in C:
- Automatic
- Register
- Static
- External

### Automatic Storage Class:

- Where would the variable be stored? : In `Memory` (i.e Within the program's allocated space in the RAM while it is being executed by the CPU).
- Default Value for the Variable? : `Garbage Value` - random value (i.e Whatever value was at that memory location before it was assigned to the variable).
- Scope of the Variable? : `local` to the block (A set of curly braces {}) in which it is defined.
- Life of the Variable? : Till the `control` remains within the `block`.

This is the **default** storage class for any variable in C.

Explicitly defining an automatic variable: Use `auto` keyword during declarations (Although NOT using it is also automatic by default). Ex:
- `auto int a, b;` which is the same as `int a, b;`.

Scope of an Automatic Variable: Alive within a block({}) and lost/dead once control goes out of it. If two variables exist in different (nested) scopes, then the reference to the variable actually takes the nearest declaration (Within the closest scope). Ex:
```
int main() {
	auto int j = 1;
	{
		auto int j = 2;
		{
			auto int j = 3;
			printf("%d", j); // 3
		}
		printf("%d", j); // 2
	}
	printf("%d", j); // 1
}
```

Note: We can create random blocks too (with {}) and not just for functions or if/else/while/for etc.

### Register Storage Class:

- Where would the variable be stored? : In `CPU Registers` (This is the difference between automatic and register variables). Access to registers is much faster than access to memory locations used to store automatic variables.
- Default Value for the Variable? : `Garbage Value` - random value (i.e Whatever value was at that register location before it was assigned to the variable).
- Scope of the Variable? : `local` to the block (A set of curly braces {}) in which it is defined.
- Life of the Variable? : Till the `control` remains within the `block`.

With the main difference between automatic and register variables being Register v/s Memory storage locations, **everything else is the same**.

Note: Register storage classes are **almost never used** these days because:
- Issues with multithreaded processes.
- Modern compilers choose when to store variables in registers (Smart optimizations) - Therefore, it does not make sense to explicity define register variables.

Explicitly defining an register variable: Use `register` keyword. Ex: `register int x;`.

### Static Storage Class:

- Where would the variable be stored? : In `Memory` (Same as automatic variables)
- Default Value for the Variable? : `0` 
- Scope of the Variable? : `local` to the block (A set of curly braces {}) in which it is defined.
- Life of the Variable? : Value `persists` between different `function calls`.

Note: Static variable values don't disappear when the function is no longer active. In fact, the old values are remembered for successive function calls.

Explicitly defining an static variable: Use `static` keyword. Ex: `static int x;`. Ex:
```
int main() {
	int z;
	z = blah(2); // z = 2
	z = blah(2); // z = 4
	z = blah(2); // z = 8
}
int blah(int a) {
	static int x; // 0 by default
	x = x + a;
	return x;
}
```

If `x` was not static then the 3 calls to `blah()` would have yielded the value `2` all three times (Assuming the variable `x` was assigned a default value of `0` inside the function).

### External Storage Class:

- Where would the variable be stored? : In `Memory` (Same as automatic variables)
- Default Value for the Variable? : `0` 
- Scope of the Variable? : `Global`
- Life of the Variable? : Till `execution` does not come to an `end`.

External/Global variables are 'Omnipresent': That is, they are declared **outside functions**, yet are available to all functions that care to use them.

Usage: 
- Either declaring a variable outside any function, or 
- Declaring with an `extern` keyword inside a function.

Ex:
```
int x = 5; // global variable (outside any function)
int main() {
	extern int y; // y has not yet been defined outside the function but extern helps us to identify it.
	printf("%d %d", x, y);
}
int y = 31; // global variable. Used inside main() with the help of extern keyword
```

Note: 
- If `extern` keyword was NOT being used inside the main() function then trying to access `y` inside it would have **caused an error** because the global declaration of `y` falls after the function definition. `extern` helps with idenitify global variables declared after the functions are defined.
- Global variables vs Local variables(auto, static, register): Local variables of a function, when accessed inside it, take precedence over a global variable having the same name.

Ex:
```
int a = 5;
int main() {
	int a = 10;
	printf("%d", a); // 10 (Local 'a')
	anotherFunc();
}
void anotherFunc() {
	printf("%d", a); // 5 (Global 'a')
}
```

When to use external storage classes? 
- For variables being used (ubiquitously) by all functions of a program.
- Avoiding unnecessary passing of parameters between functions everytime. (But, nowadays function call overheads are not that great a concern because if faster CPU switching times & memory access speeds)

Caution: Declaring all or most of the variables as extern would amount to a lot of wastage of memory space - because the variables would remain alive throughout the program.





