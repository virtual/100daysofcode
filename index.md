# #100DaysOfCode

## [HarvardX's CS50x](https://learning.edx.org/course/course-v1:HarvardX+CS50+X)

- [Week 9 Flask](#week-9-flask)
- [Week 8 HTML, CSS, JavaScript](#week-8-html-css-javascript)
- [Week 7 SQL](#week-7-sql)
- [Week 6 🐍 Python](#week-6--python)
- [Week 5 Data Structures](#week-5-data-structures)
- [Week 4 🍌 Memory](#week-4--memory)
- [Week 3 🍍 Algorithms](#week-3--algorithms)
- [Week 2 🧁 Arrays](#week-2--arrays)
- [Week 1 C](#week-1-c)

### Week 9 Flask

Framework - a way of organizing your code

Flask:

Running locally (Mac) assuming application.py is entry:

```bash
python3 -m venv venv
. venv/bin/activate
pip install Flask
export FLASK_APP=application
flask run
```

Basic application.py:

```py
# Greets user
from flask import Flask, render_template, request
app = Flask(__name__)

@app.route("/")
def index():
    return render_template("index.html", name=request.args.get("name", "world"))
```

### Week 8 HTML, CSS, JavaScript

TCP/IP governs what goes outside the envelopes. HTTP governs what goes inside of the envelopes.

- Internet Protocol - standardizes how computers address each other
- Domain Name System - translates a english-like domain names, or fully qualified domain names, to the corresponding IP addresses
- Transmission Control Protocol - TCP ports allows a server to handle multiple services (html, email, chat) and retransmitting data if needed

`curl` - connect to URL

### Week 7 SQL

We can nest queries:

```sql
SELECT title FROM shows WHERE id IN (SELECT show_id FROM genres WHERE genre = "Musical");
```

### Week 6 🐍 Python

Loosely-typed language:

- bool
- float
- int
- str
- range
- list - like an array, but dynamic size
- range - sequence of numbers
- tuple - collection of ordered values like x- and y-coordinates, or longitude and latitude
- dict, dictionaries, collection of key/value pairs, like a hash table
- set - unique values


```py
print("hello, " + answer)

# or new print format syntax
print(f"hello, {answer}")
```

Simple for loop

```py
for i in [0, 1, 2]:
    print("mew")

# or use range
for i in range(0,3):
    print("mew")    
```

- Python runs code through an interpreter, which makes it a bit slower than C
- `python` translates Python code to computer code

Using library imports

```py
from cs50 import get_int
x = get_int("x: ")
y = get_int("y: ")

# or use namespace
import cs50
x = cs50.get_int("x: ")
y = cs50.get_int("y: ")
```

Function hoisting

- Prototypes don't exist in Python
- Functions aren't automatically hoisted (undefined if they exist below running code)
- Use a `def main()` to call the functions and call `main()` to init

```py
def main():
    for i in range(3):
        meow()

def meow():
    print("meow")

main()
```

Scope

- In python, the variable will exist until the end of the function
- Don't need to initialize the var outside of a loop


```py
print("I'll print with a newline")

# You can use an end argument to specify end of line
print("I'll print on the same line", end="")
```

Errors

```py
import sys

# error (1)
sys.exit(1)

# all good (0)
sys.exit(0)
```

Files

- using `with open` will automatically close the file


----

### Week 5 Data Structures

Helpful terms:

- `struct` - let's us define our own structures
- `.` - let's you access a property
- `*` dereference operator - goto / get the value at a pointer
- `->` combines `.` and `*` functionality

#### Arrays

- Time: *O*(*n*), Ω(1) 
- More memory efficient (than LL) if you can erase the old array created by malloc
- If space available, add one
- If no space, copy and make a larger array space
- "vector" means a resizable array (Java)
- arrays in C are contiguous and cannot be resized

#### Linked Lists

- A list of numbers that are linked together ("nodes")
- Stores the value `1` or `3`
- Stores the pointer to the next value `0x456` or `0x00` (NULL)

Example of LL as custom struct, where `next` is a pointer to the next node

```c
typedef struct
{
    int number;
    node *next; // What is a node here?
}
node;
```

But since node doesn't exist to refer to the pointer for a type node, we also add the name `node` to the top of the struct def and `struct` to the pointer variable def:

```c
typedef struct node
{
    int number;
    struct node *next;
}
node;
```

More on Linked Lists 

- Not contiguous
- Cannot be searched with using binary search (phonebook)
- Calling `malloc` gives you the *address* of the first byte (size 1 or 100!)
- If you initialize without a value, it may hold garbage values--set it to `NULL`; create empty LL: `node *list = NULL;`
- Create a node in LL `node *n = malloc(sizeof(node));` (syntax for storing an address)
- When creating via malloc, check if `n` is not `NULL` before doing any work on it

```c
(*n).number = 1; 

// or equivalent:
n->number = 1;
n->node = NULL;
```

- After creating the first node, point the list to the first node
- After instantiating n, point the list node with `next` value NULL to n
- Search Time: *O*(*n*) - must travel thru each 1-by-1
- Insert new into LL on to end or sorted placement: *O*(*n*) (doesn't have to go at the end!)
- Can insert at beginning of LL: *O*(1)
- `list[0]` bracket notation adds to stack
- `int *list = malloc(sizeof(int));` adds to heap

Reallocate

- `realloc` - reallocates memory we used earlier
- `int *tmp = realloc(list, 4 * sizeof(int));`
- copies old to new
- don't need to free previous list after realloc


Example for loop for linked list items:

```c
for (node *tmp = list; tmp != NULL; tmp = tmp->next)
    {
        printf("%i\n", tmp->number);
    }
```

How to allocate more nodes in the middle (sorted)

- Order matters so you don't orphan the remaining nodes and cause a memory leak
- Point your new item to the first element
- List still points to the first element
- Remove list -> first element pointer, switch list -> new element, new element already points to previous first element

```c
n->next = list;
list = n;
```

Linked lists are 1-dimensional

#### Trees

- Trees let us work in 2 dimensions! (Left-to-right and top-to-bottom)
- Binary search - Requries you to be able to index into an array using Random Access 
- Trees are deliberately ordered; left child is less, right child is more
- Recursive data structure, tree with a child that is a tree

```c
typedef struct node
{
    int number;
    struct node *left;
    struct node *right;
}
node;
```

- Running time to insert new value into *balanced* tree: - Time: *O*(log *n*)
- Height of balanced search tree is log2 *n* (Steps to find/insert new items)

#### Hash table

Essentially an array of linked lists; allows you to "bucketize" data to let you get data more quickly

- init phonebook[26]
- set phonebook[0] = linked list that contains Albus
- set phonebook[25] = linked list that contains Zack
- hash function - a function that tells you which array element to insert into
- "hash" - look at some input and return output (which bucket?) based on characteristic of input  
- colissions - when there are too many results (chains) under a certain hash array element

More "buckets"

- can we add another level of hash tables? 26 * 26 (676)
- can we add levels for each letter? price = more memory 26 * 26 * 26 (17576)
- Use `bc` for a CLI calculator! 
- hash sort example, card suits
- Running time of searching for an item: (4 buckets? n/4) as item count get larger: *O*(*n*), however still faster than LL and Array

#### Tries (Retrievals)

AKA Prefix tree

- Used for storing words or sophisticated data
- Tree made up of arrays, where each array is a pointer to another node
- Retrieval time: *O*(1)
- Needs a lot of memory

#### Abstract data structures

- Queue: FIFO, store checkout; enqueue (get in line), dequeue (get out of line), array isn't dynamic enough, need linked list 
- Stack: LIFO, cafeteria tray; push and pop
- Dictionary: associate keys with values; dictionary or salad pickup; *apple* has definition, lookup value by key

----

### Week 4 🍌 Memory

**Hex**

- Hex is base 16
- `FF` works out perfectly for 4 bits: `16 x F` (240) + `1 x F` (15) = 255 
- Any time you reference hex digits, prefix w/ `0x` eg `0x49`

**Addresses**

- `&` What is the address
- `*` Go to the address; what's inside?

```c
int n = 50;
printf("%i", n);   // 50 - value of n
printf("%p", &n);  // 0x123 - address
printf("%i", *&n); // 50 - print value at 0x123 (address)
```

**Pointers**

- Store the *address* and *type* of value
- `int *p = &n` - declare a pointer of type int
- use `*p` to print the value of `n` (`*&n`)
- Pointer address is 8 bytes

Mailbox example

- Mailbox `p` [0x123] - contains value of an address; points to mailbox 0x123
- Mailbox 0x123 `n` [50] - contains value of 50 
- We don't care about the pointer's (`p`) address

**Strings**

- Not native to C - created as `typedef char *string`
- Example of string `[H][I][!][\0]`, where addresses would be consecutive, eg: `[0x123][0x124][0x125][0x126]`, 1 byte apart
- The first byte of a "string" is the string's address
- `string` = `char *s = "HI!";` where address of `s = &s[0]`
- `printf("%c", *s); \\ H` - print value at address
- last char of "string" is `\0` or `0` as type int
- `get_string` returns address of first character

How would you copy a string?

- Allocate a new spot in memory: eg 4 bytes, `malloc(4)`, or `malloc(strlen(s) + 1)` (to account for `\0`)
- Check if the address created is valid (not NULL)
- Check that length of string is not 0
- Loop over char address (`n <= i`) and copy all values, including `\0`
- Or you could copy using `strcpy(s, t)`

Libraries

- `strcpy(s, t)` - create a new copy of s to t
- Compare using `strcmp(v1, v2) == 0`
- `malloc()` returns the address of the first byte
- if you use `malloc()`, give the memory back `free(t)`
- `get_string()` uses `malloc()` and `free()`
- `valgrind()` shows where you touched memory; use it debug code
- `'scanf()` scan from user's keyboard

Defining a string variable w/ allocation:

```c
char *s = malloc(4);
// uses heap, needs to also use free()
```

```c
char s[4];
// uses stack, doens't need free()
```

**Memory layout**

- machine code
- globals
- heap (malloc)
- stack (calling a function, local vars) - memory gets used and reused

#### File Input/Output

File I/O - taking input and output from files

```c
FILE *file = fopen("phonebook.csv", "a"); 
// a - append
// w - write
// r - read
```

Full example of reading input and printing to a file:

```c
// Saves names and numbers to a CSV file

#include <cs50.h>
#include <stdio.h>
#include <string.h>

int main(void)
{
    // Open CSV file
    // FILE is a native C type
    FILE *file = fopen("phonebook.csv", "a");
    
    // Check if file is not null
    if (!file)
    {
        return 1;
    }

    // Get name and number
    string name = get_string("Name: ");
    string number = get_string("Number: ");

    // Print to file
    fprintf(file, "%s,%s\n", name, number);

    // Close file
    fclose(file);
}
```

- `fopen(pathname, mode)` - returns a pointer to the FILE or NULL
- `fclose(pointer)` - close the file (previously opened by `fopen`) at the given pointer
- `fprintf(pointer, format, values)` - prints to a file
- `fread(pointerToStoreAt, size, numberToRead, filePointer)` - read bytes from a file and store at the pointerToStoreAt

For iterating thru bytes, we need to define a custom typedef:

```c
typedef uint8_t BYTE;
```

Then we can copy, using `buffer` as a temporary value 

```c
// Copy source to destination, one BYTE at a time
BYTE buffer;
while (fread(&buffer, sizeof(BYTE), 1, source))
{
    fwrite(&buffer, sizeof(BYTE), 1, destination);
}
```

Images

Many file types have "magic numbers" the first N bytes in a file that establish what type of file it is; for example, every JPG will start with `0xff 0xd8 0xff`

----

### Week 3 🍍 Algorithms

- **running time** - how long it takes to run, steps/time
- *O* - big O notation: the maximum time/steps it will take to run
- big O only focuses on dominant factors and not any constant factors, like the 1/2 or the divided by 2
- Ω (omega): the lower bound on the time/steps it takes to run
- θ (theta): if the program takes the same lower bound and upper bound time to run

Common formulas:

- *O*(*n*^2) -- worst
- *O*(*n* log *n*)
- *O*(*n*)
- *O*(log *n*)
- *O*(1) -- best

#### Search types

- Linear search: *O*(*n*), Ω(1) - one by one, for random ordered elements
- Binary search: *O*(log *n*), Ω(1) - divide by half, half again, half again, ..., for increasingly ordered elements

Comparing string values

- You cannot use `==` for comparing string values
- Use `strcmp()` from `string.h` include: `strcmp(compare_to_string, word_to_find)` returning 0 (equal), negative (first str comes before second), positive (first str comes after second) -- compares ASCII order, not alphabetical 
- Strings always end with `\0`
- Any non-zero value in C is considered true (truthy); only 0 is false

Hertz defs

- 1 hertz = do 1 *thing* per second
- 1 gigahertz = do 1 bil *things* per second, like a CPU


Creating custom types / data structures--allows you to keep related data tied together

```c
typedef struct
{
	string name;
	string number;
}
person;

int main(void) 
{
	person people[2]; // Init person structure of size 2
	people[0].name = "Brian";
	people[0].number = "555-555-5555";
	
	...
}
```

- Sir Kittian's ribbons
- Little Kitty Fluffpuff
- Ciao MiaoMiao


#### Sorting

[Comparison Sorting Examples](https://www.cs.usfca.edu/~galles/visualization/ComparisonSort.html)

Selection Sort

- Time: n^2/2 + n/2 = *O*(*n*^2) & *Ω*(*n*^2) = *θ*(*n*^2)
- Looks through every number to find smallest, then swaps position at i. 
- If no swaps, the sort still runs again.

```
For i from 0 to n-1
  Find smallest item between i'th item and last item
  Swap smallest item with i'th item
```

Bubble Sort

- Time: n^2 - 2n + 1 = *O*(*n*^2) & *Ω*(*n*) 
- Looks through pairs of numbers and sorts in pairs and biggest numbers start "bubbling up" to the top. 
- If no swaps, the list is sorted and program can complete.
- Finish for-loop at `(n-2)` because we don't compare the last number to another number (out of bounds)
- Lower bounds time if the numbers are already sorted (look thru all elements 1 time)

```
Repeat n-1 times
  For i from 0 to n-2
   If i'th and i+1'th elements out of order
   Swap them
  If no swaps
    Quit
```

Merge Sort

- Time: n * log n = *O*(*n* log *n*) & *Ω*(*n* log *n*) = *θ*(*n* log *n*)
- Divide in half, in half, in half (log)
- Can't escape early if the input is already sorted
- For C, you'll need a second array to temporarily merge things (Needs twice as much memory)

```
If only one number // Needs recursive base case
  Quit
Else
  Sort left half of numbers
  Sort right half of numbers
  Merge sorted halves
```

Recursion

- Needs a base case to quit
- Define the answer in terms of itself

----

### Week 2 🧁 Arrays

Clang 

- `clang` is used as a compiler when you type `make`
- It uses command-line arguments
- `clang -o hello hello.c -lcs50`: passes in arguments, -o, hello, hello.c, -lcs50

Compiling

- compiler: a program that converts source code to machine code
- compiling includes these four steps: preprocessing, compiling, assembling and linking

1. **Preprocessing**--looks for any lines that start with a hash symbol, like `#include cs50.h`, and copies the contents of the file into the program; implements prototypes
2. **Compiling**--changes source code to assembly code (`xorl %ebx, %ebx` would be like `i = 0`)
3. **Assembling**--coverts assembly code to machine code (0s and 1s)
4. **Linking**--takes the machine code from the given file and any included libraries and combines

Debugging

- Use `debug50` on your compiled code, e.g. `debug50 ./buggy`

Size of C Types

- bool - 1 byte
- char - 1 byte
- double - 8 bytes
- float - 4 bytes
- int - 4 bytes
- long - 8 bytes


"code smell" - when something is off with the code, but you can't quite pinpoint it

C Notes:

- In C, you cannot find the length of the array; you need to capture this value separately as a int
- For a function using an array, you'd need to pass both the array and length values as arguments
- If you multiply ints by a float, it will convert to a float; only one float value automagically converts
- If you're setting a character, use single quotes: `char brick = '#'`
- If you're setting a string, use double quotes: `string pyramid = "###"`
- String is implemented as an array of 1-byte chars with a final byte that stores the end `\0` (the Null character)

For loop to get chars from string, check for null character:

```c
string s = get_string("Input: "); 
printf("Output: "); 

for (int i = 0; s[i] != '\0'; i++) { 
  printf("%c", s[i])
}


for (int i = 0, n = strlen(s); s[i] < n; i++) { 
  printf("%c", s[i])
}
```

Or use string.h and `strlen()`


`ctype.h`

- islower() true / false
- toupper()

[Manual pages for the C standard library, C POSIX library, and the CS50 Library.](https://manual.cs50.io/)

```c
int main(int argc, string argv[]) {
  # argv[0] will be the file name
  # argv[1] would be the command line argument
  # argc automatically saves how many words typed in (including filename, so 2 here)
}
```

Successful c functions `return 0` for normal or `return 1` for errors


🥥 Shorts


```c
#include <studio.h>
#include <cs50.h>

bool main(void) {
	int side1 = get_int("Side 1: ");
	int side2 = get_int("Side 2: ");
	int side3 = get_int("Side 3: ");
	return valid_triangle(side1, side2, side3);
}

bool valid_triangle(int side1, int side2, int side3) {

	if (side1 <= 0 || side2 <= 0 || side3 <= 0) {
		return false;
	}

	if (side1 + side2 > side3) {
		if (side2 + side3 > side1) {
			if (side3 + side1 > side 2) {
				return true;
			}
		}
	}
	return false;
}
```


Arrays in C

- Initialization `type name[size]` or `bool truths[3] = { true, false, true }`
- Will not prevent you from going out of bounds = segmentation fault!
- You can actually look at what is stored in memory for other spaces
- You cannot copy arrays to another variable; instead you need to loop over it and create a new array
- When an array is passed into a function, it is the actual array, not a copy of it

Command line args

- int main(int argc, string argv[]) {}
- input comes in as strings 

----

### Week 1 C

- introduction to C
- use `help50 make file`, `style50 make file` or `check50 make file` as needed 
- there is no hoisting in C, instead you use prototypes to hint at the function that is defined later below

```c
#include <cs50.h>
#include <stdio.h>

// Prototype
void meow(void);

int main(void)
{
   meow();
}
void meow(void)
{
    string answer = get_string("what's your name? ");
    printf("meow, %s\n", answer);
}
```

5 Types built-in to C:

- int
- char
- float (floating point number)
- double
- void (for functions)

Types not built-in to C available in CS50 library:

- bool
- string

You can init two variables in one line, for example: `int height, width;`

----


### Week 0

- [satinflame Scratch Project 0](https://scratch.mit.edu/projects/582543204/)

