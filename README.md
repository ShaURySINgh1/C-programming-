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
