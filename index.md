# #100DaysOfCode

## [HarvardX's CS50x](https://learning.edx.org/course/course-v1:HarvardX+CS50+X)

- [Week 3 🍍 Algorithms](#week-3--alogrithms)
- [Week 2 🧁 Arrays](#week-2--arrays)
- [Week 1 C](#week-1-c)

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




### Week 0

- [satinflame Scratch Project 0](https://scratch.mit.edu/projects/582543204/)

------------


## 👑 Round 4 Projects 👑

### Hightlights from this round:

- [Scientific Computing with Python certification!](https://www.freecodecamp.org/certification/virtual/scientific-computing-with-python-v7)
- [Sentiment Analyzer](https://github.com/virtual/sentiment-analyzer)
- [Recipe App - fixed search](https://fcc-recipe.herokuapp.com/)
- [Front-end projects with base theme](https://github.com/virtual/fed-projects)

### All projects:

- freeCodeCamp [Python](https://www.freecodecamp.org/learn/scientific-computing-with-python/) & [Scientific Computing with Python certification!](https://www.freecodecamp.org/certification/virtual/scientific-computing-with-python-v7)
  - Python Project 2: [Time Calculator ✓](https://replit.com/@virtual/boilerplate-time-calculator) 
    - Day 01: test #1, simple time addition
    - Day 02: tests #2-5, next day
    - Day 03: tests #6-12, show days elapsed ✓
  - Python Project 3: [Budget App ✓](https://replit.com/@virtual/virtual-fcc-budget-app)  
    - Day 11: local setup
    - Day 12: tests #1-7, deposit, withdraw, check balance
    - Day 13: tests #8-10, transfer, override str method
    - Day 15, 17, 18: bar chart ✓
  - Python Project 4: [Polygon Area Calculator ✓](https://replit.com/@virtual/fcc-polygon-area-calculator)  
    - Day 19: tests #1-5
    - Day 20: all tests complete ✓
  - Python Project 5: [Probability Calculator ✓](https://replit.com/@virtual/probability-calculator)
    - Day 21: test #1
    - Day 22: test #2
    - Day 23: random library
    - Day 24: test #3 ✓
- freeCodeCamp Information Security
  - Python for Penetration Testing
    - Day 26: sockets
- [Sentiment Analyzer](https://github.com/virtual/sentiment-analyzer)
  - Day 04: Began looking into sentiment analysis
  - Day 05: Created front-end form using React and Axios
  - Day 06: App now working on www 
  - Day 07: Lifted state, added dynamic coloring based on pos/neg
  - Day 08: Added svgs that appear based on the content
  - Day 09: Added pop-in animation, delay, and some more randomization; made more performant
  - Day 10: Added a bit more random sizing, hover effects and interactive note sounds using Tone JS
- Sololearn
  - Day 14: Python core
  - Day 65: Go
- Codepen
  - Day 25: [Styling broken images](https://codepen.io/virtual/pen/BaRBajq)
  - Day 30: Fixed some broken codepens
- Projects
  - [Recipe App](https://fcc-recipe.herokuapp.com/)
    - Day 27: Fixed & readded search
    - Day 28: Internationalization
    - Day 29: Failed attempt adding ingredients on edit
  - Day 39: Scrape Q&A api
  - Flask App
    - Day 40: Setup for collaboration
    - Day 41: Add SCSS functionality
    - Day 42: Django
  - [JavaScript30](https://github.com/virtual/javascript30)
    - Day 43: Started project 11, video player 
    - Day 45: Project 11, build out button interactions with dataset
    - Day 46: Project 11, ranges and updates ✓
    - Day 48: Project 12, key sequence detection ✓
    - Day 96: Project 13, copy JS arrays and objects ✓
  - [Front-end projects](https://github.com/virtual/fed-projects)
    - Day 50: Setup local environment
    - Day 52: Add a second page 
    - Day 53: Roughed in HTML & CSS, setup variables 
    - Day 54: Played with scss functions
    - Day 55: Stylelint setup
    - Day 56: Stylelint hackery
    - Day 61: FED Project #1
    - Day 62: scss loops
    - Day 64: scss theme overrides
    - Day 67: FED Project #2
    - Day 68: FED Project #2
    - Day 69: FED Project #3
    - Day 70: FED Project #3
    - Day 71: learning about !default scss flag
    - Day 73: restructured using !default
    - Day 74: FED Project #3, form
    - Day 75: FED Project #3, type
    - Day 76: FED Project #3, cards
    - Day 78: Setup JavaScript include
    - Day 81: Added PristineJS validation, alert styles
    - Day 82: Styling hero, results table
    - Day 83: Styling tweaks
    - Day 84: Menu collapsing JS
    - Day 85: Styling mobile menu
    - Day 86: Dynamic table results
    - Day 87: Copy to clipboard button
    - Day 88: Style stackable tables for mobile
    - Day 89: Lighthouse audit fixes
    - Day 92: Fix mobile styles; add robots.txt
- Python
  - Day 97: Reviewing some PY4E code
  - Day 98: PY4E code, file reading
  - Day 99: Codewars, list comprehension
  - Day 100: Codewars
- LinkedIn
  - Localization for Developers ✓
    - Day 31: Intro: Overview
    - Day 32: Intro: Localization management & research
    - Day 34: Internationalizing content
    - Day 35: Unicode fonts, RTL support
    - Day 36: formatting, icons, pseudolocalization
    - Day 37: translators
    - Day 38: wrap-up
- Reading
  - Day 47: Code Complete, pp 74-86
  - Day 60: Code Complete, pp 86-94


## R4 Day 100: 2021-09-08 Wednesday

Last day of code! Poked around on [codewars](https://www.codewars.com/kata/578aa45ee9fd15ff4600090d/train/python)

## R4 Day 99: 2021-09-07 Tuesday

[Codewars](https://www.codewars.com/kata/546f922b54af40e1e90001da/solutions/python), learning list comprehension!

## R4 Day 98: 2021-09-06 Monday

Played with some python and file reading lines

## R4 Day 97: 2021-09-05 Sunday

Reviewing some python code :)

## R4 Day 96: 2021-09-04 Saturday

[Javascript 30 Day 13](https://virtual-javascript30.herokuapp.com/index.html) How to copy JS arrays and objects

## R4 Day 95: 2021-09-03 Friday

Skip

## R4 Day 94: 2021-09-02 Thursday

Tried running a prior university project on my Mac, but everything is so out-of-date and broken. 

## R4 Day 93: 2021-09-01 Wednesday

Skip

## R4 Day 92: 2021-08-31 Tuesday

Update styles for mobile and add robots.txt. Good default:

```txt
User-agent: *
Allow: /
```

## R4 Day 91: 2021-08-30 Monday

Skip

## R4 Day 90: 2021-08-29 Sunday

Skip

## R4 Day 89: 2021-08-28 Saturday

Check Lighthouse scores

- 76 Performance
- 95 Accessibility
- 100 Best Practices
- 100 SEO

Actionable:

- Set widths and heights on images
- Move JS to bottom
- Change font loads to use a print media type to lower priority
- Updated text contrast
- Removed aria hidden on load and relying on JS to set instead

Updated score: (at least all green)

- 90 Performance
- 98 Accessibility
- 100 Best Practices
- 100 SEO

## R4 Day 88: 2021-08-27 Friday

Modified table styles to be responsive on mobile.

## R4 Day 87: 2021-08-26 Thursday

Update Copy button to copy the fake shortened link to clipboard

## R4 Day 86: 2021-08-25 Wednesday

Build dynamic rows in table for shortened links and create more dynamic (fake) link shortener.

## R4 Day 85: 2021-08-24 Tuesday

Styling for mobile menu, transitions and SVG image, and fix ARIA

## R4 Day 84: 2021-08-23 Monday

JavaScript for mobile menu toggle

## R4 Day 83: 2021-08-22 Sunday

Styling tweaks for [FED project #3](https://virtual.github.io/fed-projects/03/).

Still to do:

- Mobile menu
- JavaScript to generate URL
- JavaScript for Copy Link button
- Check keyboard accessibility


## R4 Day 82: 2021-08-21 Saturday

Working on [FED project #3](https://virtual.github.io/fed-projects/03/). Styled hero background to be better for mobile and desktop; updated URL shortener to include (faked-in) result if the link given in valid. Spacing between table rows (given a different background color) is kind of difficult actually. Ended up using a border top for `tr + tr`. 

## R4 Day 81: 2021-08-20 Friday

Added form validation for the URL box using [PristineJS validation library](https://github.com/sha256/Pristine). Added alert colors to base theme & FED project #3, generated with https://colors.eva.design/.


## R4 Day 80: 2021-08-19 Thursday

Skip

## R4 Day 79: 2021-08-18 Wednesday

Try out Storybook with Jigsaw (no-go); Try out responsively for Chrome

## R4 Day 78: 2021-08-17 Tuesday

Setup JavaScript to use in the project #3

## R4 Day 77: 2021-08-16 Monday

Skip

## R4 Day 76: 2021-08-15 Sunday

FED Project #3, card designs

## R4 Day 75: 2021-08-14 Saturday

FED Project #3, font styles

## R4 Day 74: 2021-08-13 Friday

Styling the form and more of project 3. Instead of using offset margins and padding for the off-centered look of the form, I used a 50%/50% linear background. 

```scss
.cta-form {
  background:linear-gradient(to bottom, $color-white, $color-white 50%, $color-gray-light 50%);
}
```

## R4 Day 73: 2021-08-12 Thursday

> Sass variables, like all Sass identifiers, treat hyphens and underscores as identical. This means that `$font-size` and `$font_size` both refer to the same variable.

Restructuring projects 1-3 using `!default`; reduces repeating code and overrides.

Original:

| File | Size |
| -------- | ---------: |
| `/js/main.js` | 10.9 KiB |
| `css/main.css` | 6.74 KiB |
| `css/proj01.css` | 7.38 KiB |
| `css/proj02.css` | 8.35 KiB |
| `css/proj03.css` | 9.36 KiB |
 

Updated compiled sizes after restructure:


| File | Size |
| -------- | ---------: |
| `/js/main.js` | 10.9 KiB |
| `css/main.css` | 6.34 KiB |
| `css/proj01.css` | 6.79 KiB |
| `css/proj02.css` | 7.72 KiB |
| `css/proj03.css` | 8.52 KiB |


## R4 Day 72: 2021-08-11 Wednesday

Skip

## R4 Day 71: 2021-08-10 Tuesday

Read up on the scss `!default` usage. Will try to [reorder my base theme](https://thoughtbot.com/blog/sass-default) after my child themes to see if this helps reduce redundancy. 

## R4 Day 70: 2021-08-09 Monday

Building out HTML and some more base styles (padding, menu, forms) https://virtual.github.io/fed-projects/03/

## R4 Day 69: 2021-08-08 Sunday

Start [FED Project #3](https://virtual.github.io/fed-projects/03); going a little more complex now that I have a standard base theme figured out with overrides. More things to add the base core will become apparent like list styles, menu things. :)

## R4 Day 68: 2021-08-07 Saturday

Finished [FED Project #2](https://virtual.github.io/fed-projects/02); added flexbox mixins to the base SCSS core (pretty easy!); refactored base to a 'base' folder to cleanup the structure a little.

## R4 Day 67: 2021-08-06 Friday

Setup and worked on [FED Project #2](https://virtual.github.io/fed-projects/02)

## R4 Day 66: 2021-08-05 Thursday

Learning Go (Google's machine learning language) on SoloLearn app

## R4 Day 65: 2021-08-04 Wednesday

Skip

## R4 Day 64: 2021-08-03 Tuesday

Set up FED projects to allow for theme / scss variable overrides in order to maintain one general base code and themes that can override it.

- Easier way to do this in webpack mix file?
- Should I do an include for general includes?


proj01.scss:

```scss
@import './variables';
@import './01/variables';

// General includes
@import './structure';
@import './colors';
@import './typography';
@import './lists';

@import './components/buttons';

// Local overrides
@import './01/structure';
@import './01/colors';
@import './01/components/cards';
@import './01/components/buttons';
```


## R4 Day 63: 2021-08-02 Monday

Skip

## R4 Day 62: 2021-08-01 Sunday

Worked on building out more [columns, margin](https://github.com/virtual/fed-projects/blob/main/source/_assets/sass/_structure.scss), and [theme](https://github.com/virtual/fed-projects/blob/main/source/_assets/sass/_colors.scss) classes (similar to Bootstrap) using scss for loops.

```scss
$marginbuffers: 5;
@for $i from 0 through $marginbuffers {
  .my-#{$i} {
    margin-top: $i * ($theme-font-size-base * .5);
    margin-bottom: $i * ($theme-font-size-base * .5);
  }
  .mt-#{$i} {
    margin-top: $i * ($theme-font-size-base * .5);
  }
  .mb-#{$i} {
    margin-bottom: $i * ($theme-font-size-base * .5);
  }
}
```

## R4 Day 61: 2021-07-31 Saturday

Worked on FED Project #1

## R4 Day 60: 2021-07-30 Friday

Read Code Complete pp 86-94; inheritance, abstraction

## R4 Day 59: 2021-07-29 Thursday

Skip

## R4 Day 58: 2021-07-28 Wednesday

Skip

## R4 Day 57: 2021-07-27 Tuesday

Skip


## R4 Day 56: 2021-07-26 Monday

Got stylelint working with some third-party packages

package.json:

```json
{
  "name": "code",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "stylelint": "^13.13.1", 
    "stylelint-declaration-block-no-ignored-properties": "^2.4.0",
    "stylelint-config-rational-order": "Allohamora/stylelint-config-rational-order#master",
    "stylelint-order": "^2.2.1",
    "stylelint-scss": "^3.20.1"
  }
}
```

.stylelintrc.json:

```json
{
  "plugins": [
    "stylelint-order", 
    "stylelint-config-rational-order/plugin",
    "stylelint-declaration-block-no-ignored-properties"
  ],
  "rules": {
    "order/properties-order": [[], { "severity": "warning" }], 
    "order/order": [
			"custom-properties",
			"declarations"
		],
    "plugin/rational-order": [true, {
      "border-in-box-model": false,
      "empty-line-between-groups": false,
      "severity": "warning"
    }],
    "declaration-no-important": true,
    "plugin/declaration-block-no-ignored-properties": true
  } 
}
```

## R4 Day 55: 2021-07-25 Sunday

Working on setting up my styelint for a computer but it turns out there's some issues with this package not being updated for sometime: `stylelint-config-rational-order`; need to find a new way to accomplish it, due to security vulnerabilities on these packages.

Quick update to add border-radius; if you have an outer parent with a border radius, you can use `overflow: hidden` to give all the child elements the same border-radius. Never quite thought that through :)

## R4 Day 54: 2021-07-24 Saturday

Updated scss to [use some functions](https://github.com/virtual/fed-projects/commit/c2e68d3f2a6432b5171d8f6553eab5f7a19c25cf)

- Great article on [functions from gavsblog](https://www.gavsblog.com/blog/for-each-while-loops-sass-scss)
- [Sass div](https://sass-lang.com/documentation/breaking-changes/slash-div); using the math libray in scss
- [Kitchen sink code incl. headings](https://fashionipsum.com/snippets.html) for testing css

## R4 Day 53: 2021-07-23 Friday

Setup some styles and HTML for a small project.

## R4 Day 52: 2021-07-22 Thursday

Set up a second page in jigsaw

## R4 Day 51: 2021-07-21 Wednesday

Not exactly coding; spent the evening trying to figure out mic recording and processing tracks on reaper

## R4 Day 50: 2021-07-20 Tuesday

Setup a local environment for working on [front-end projects](https://github.com/virtual/fed-projects)

## R4 Day 49: 2021-07-19 Monday

Skipped

## R4 Day 48: 2021-07-18 Sunday

JavaScript30, [project 12, key sequence detection](http://virtual-javascript30.herokuapp.com/12-konami/) (like the Konami code used on buzzfeed) pretty magical! 

## R4 Day 47: 2021-07-17 Saturday

Code Complete, pp 74-86

- Break up larger systems into subpackages
- use references between classes as a last resort
- the simpler the better 
- never have circular references
- if you have old obfuscated code, create an interface so that it's easier to access the data returned by kludgy code in a more consistent way

## R4 Day 46: 2021-07-16 Friday

Finished JavaScript 30 project 11 with custom video controls.

## R4 Day 45: 2021-07-15 Thursday

Worked more on JavaScript 30 project #11. Reminder about how cool `.dataset.myitem` is to pull any items that have an attribute like `data-myitem`

## R4 Day 44: 2021-07-14 Wednesday

Skip

## R4 Day 43: 2021-07-13 Tuesday

Started project 11, video player. Seems like there's a feature/bug that the video will automatically start/stop on click without an event listener for video.click (so basically if you listen for it, you're doubling the work and negating the effect). Also interesting: videos have no "playing" status, only "paused."

## R4 Day 42: 2021-07-12 Monday

Not much--figured out the Flask app uses django for HTML templating.

## R4 Day 41: 2021-07-11 Sunday

Adding [Flask-Scss](https://pythonhosted.org/Flask-Scss/) to the flask app and restructured some of the scss files; added vars

## R4 Day 40: 2021-07-10 Saturday

Working to setup https://github.com/virtual/flask-tutorial to maybe work on a team repo project with arek_grows!

## R4 Day 39: 2021-07-09 Friday

Trying to scrape practice questions for license information to make Anki cards but the API seems to be limited to 10 results, no matter what limit you put. 

## R4 Day 38: 2021-07-08 Thursday

### QA Strategy
 
- Locale testing: 
  - Testing text strings and media files
  - Interface can support variable-width strings
  - Lanugage is correct
  - Product won't be misinterpreted
  - Test it by someone who is native; are comfortable using computers in _their_ language; and comfortable with using similar products
- Functional testing:
  - Do all program functions still work with different languages
  - Retest with your QA checklist

Test by changing your locale in your OS! Can also try the Language Switcher App. Virtual environments can be good.  

## R4 Day 37: 2021-07-07 Wednesday

- [A guide to buying translation service](https://www.atanet.org/client-assistance/getting-it-right/)
- [Translator directory](https://www.proz.com/)
  - Best to translate into their native language
  - Find a translator with experience in a relative field
  - Transifex

Localization solutions:
- gettext GNU
- Shuttle, integrates with Github - requires Ruby & subscription
- OneSky - paid & free for sole developers

## R4 Day 36: 2021-07-06 Tuesday

If you're formatting with bold, italics, or underlines, this may not work in other languages:
- Some languages don't have italics versions
- Bold might make asian characters indistinguishable
- They may use a different font or dots instead

Formatting:
- A for-loop with space & commas might not work some languages, like Chinese which uses an Ideographic Comma & Fullwidth Comma
- In French, punctuation (: ? !) are always preceded by a space
- Many languages use [different quotation marks](https://en.wikipedia.org/wiki/Quotation_mark)

### Adapting UI

- Interface should support at least 30% expansion of text (50-60% ideal)
- Communicate if there's a necessary limit of characters in a certain space
- Some characters may need to be displayed larger to be legible
- Arrows & tab icons may need to be flipped for RTL interfaces
- Pagination for RTL can be confusing (text labels might be the clearest)
- Don't change shortcut keys (CTRL+S, CTRL+B) as they're expected to work a certain way
- Make sure sorting happens in the expected order of a locale
- Icons only work if the user can identify the icon (eg inbox)
- Using red for alerts and icons is okay in China, even though they usually use red for celebration
- Best to add the color format to the translated string
- Avoid using flags to represent a language
- Showing divided maps can be an issue for regions where there's disputed territory
- Hand gestures can mean different things
- Animal icons can mean different things: owls (wise in US; death in China; bad luck in India)
- [Foreign lorem ipsum](https://generator.lorem-ipsum.info/_hebrew) is good for testing encoding support

### Pseudolocalization

- Create a placeholder file that allows you to test string replacement
- Easy to visualize unlocalized strings
- Use longer test strings to test for long text

## R4 Day 35: 2021-07-05 Monday

Media:
1. Unlocalize media
    - Yellow school buses are not common outside NA
1. Media swapping
    - Should be as easy to swap as text
    - RtL / LtR infographics
    - Japan reads comics RtL but text LtR
1. Media separation
    - Avoid text in an image
1. Media context
    - Know guidelines of things to avoid in countries / context
1. Keep all source files
    - Makes dubbing easier
    - Some countries are accepting of dubbing, others not
    - Make sure all audio can be turned off

### Internationalizing GUI

Unicode:
- encodes characters _up to_ 4 bytes
- UTF-8 is encoded in up to 4 8-bit groups (variable width)
- UTF-16 
- Ensure every input, function, storage format and font is Unicode compliant
- [Unicode normalization](https://unicode.org/reports/tr15)

__Diacritical marks__ - accents, tone marks used for pronunciation

Fonts
- There is no font that supports 100% of the unicode mapped characters
- Google is working on this project with [Noto](https://www.google.com/get/noto/) - Google’s goal is to see “**no** more **to**fu” (tofu - the white boxes for when a character isn't supported)

### RTL Support

**BiDi** - Bi-directional text; where using a mix of LTR & RTL text in the same field or interface

| Characters | Direction | Effect |
| - | - | - | 
| Most alphabets | LTR | Strong | 
| Hebrew & Arabic | RTL | Strong | 
| European numbers | none | Weak | 

- Numbers and punctuation appear in the overall direction (weak)
- You can force the [direction of unicode](https://www.explainxkcd.com/wiki/index.php/1137:_RTL)
- [202 encoding reference](http://unicode.org/reports/tr9/#Explicit_Directional_Embeddings)
- [Demystifying BiDi talk](https://youtu.be/wOEzYefrqo4?t=653)


| Abbr. |	Code Point | 	Name	| Description |
| - | - | - | - |
| LRE |	U+202A|	LEFT-TO-RIGHT EMBEDDING | 	Treat the following text as embedded left-to-right. |
| RLE |	U+202B|	RIGHT-TO-LEFT EMBEDDING | 	Treat the following text as embedded right-to-left. |
| LRO |	U+202D|	LEFT-TO-RIGHT OVERRIDE | 	Force following characters to be treated as strong left-to-right characters. |
| RLO |	U+202E|	RIGHT-TO-LEFT OVERRIDE | 	Force following characters to be treated as strong right-to-left  characters. |
| PDF |	U+202C|	POP DIRECTIONAL FORMATTING	 | End  the scope of the last LRE, RLE, RLO, or LRO. |

Use example, as stored in database:

```text
תבותכ: [U+202a] 123 Easy St. [U+202c]
```

Desired output:
```text
123 Easy St. :כתובת
```

202C allows us to "pop" back to global settings after overriding

You can also use native HTML solution (as stored in DB):
```html
תבותכ: <span dir="ltr">123 Easy St.</span>
```

## R4 Day 34: 2021-07-04 Sunday

### Content

- Content needs context
- The shorter the word, the more obscure the translation can be
- Annotate strings as you pull them out
- Is the text itself appropriately international?
  - Figures of speech
  - Culture-specific: sports metaphors (Kickoff meeting)
  - Listing seasons
  - Exaggerations 
  - Sarcasm

Strings:
- Don't concatenate
- Use interpolation: where the variables are directly placed in the string: `you sent a message at $time` allows you rewrite the sentence correctly
- You don't know which order the variables will be used, so they need to be able to be rearranged
- Avoid using strings in two different content / locations
  - "Edit" - is it a verb or noun?
  - Grammatical gender

Numbers:
- Some languages have three forms:
  - Singular (1)
  - Dual (2+)
  - Plural (3+)    
- GetText is a free GNU localization framework
- [Language plural rules](https://www.unicode.org/cldr/cldr-aux/charts/29/supplemental/language_plural_rules.html)  




## R4 Day 33: 2021-07-03 Saturday

--

## R4 Day 32: 2021-07-02 Friday

1. Identify target locales
1. Internationalize your product
1. Pseudo-localization - test that media, text is changing
1. Test for functionality
1. Add additional locales
1. Test each locale

### Localization solution - one spot for all localizations, translations, media

- Context and feedback - translators can ask questions, if others ask similar questions for other locales, it helps streamline
- Translation memory (TM) - keeps track of how a phrase may have been previously translated
- Machine translation (MT) - eg Google Translate
- Other features - online repo, permissions, stats

### Research

- Identify potential targets
  - User feedback
  - Watch for an elevated # of users from a certain geolocation
  - How easy (eg France, Italy and Spain at the same time)
  - Check what your competitors support (App Annie)
- Locale needs
  - How is language written?
  - Punctuation? 
  - Currency, special symbols
- Consumption
  - What types of smartphones are most common?
  - Is internet readily available
  - How are similar services received?

### Legal Implications

- Identify any major legal obstacles
- Restrictions on data storage? User consent? PII
- uk.practicallaw.com - Laws about data storage
- COPPA - legislation about info for children under 13

### Specialists

- Consultants for the whole process or a part
- Analysis and training
- Internationalization
- Localization (translators)
- Review
- QA & Testing

## R4 Day 31: 2021-07-01 Thursday

[Localization for Developers](https://www.linkedin.com/learning/localization-for-developers/welcome?u=104778834)

- **Locale** - a group of target users described by location, language, and preferences. _language, currency, measurements_
- **Localization (L10n)** - the process of tailoring a product for a specific locale
- **Internationalization (i18n)** - preparing a product to support multiple languages and settings

Steps for localization:
1. Translation (inc. reading direction)
1. Unit conversion
1. Social conventions - accommodating user expectations
1. Legal regulation

Considerations:
- Separate code from content
- Load different assets
- Toggle region / language
- Support displaying content of different lengths

Localization != language

Associated Preferences:
- Time
- Date
- Number
- Currency
- Keyboard layout
- Input prefs
- Paper sizes
- Writing standards (e.g. simplified vs traditional Chinese)

Identifying locales: typically defined using two values: (eg `en_US` vs `en_CA`)
1. language in lowercase (ISO 639.1 - 2 chars/639.2 - 3 chars)
1. region in uppercase (ISO 3166 - 2 chars)

## R4 Day 30: 2021-06-30 Wednesday

Fixing some of my better codepens!

- [Quote generator](https://codepen.io/virtual/full/jqJeKb) - Chris has a new API, working good!
- [Collapsible timeline](https://codepen.io/virtual/full/Vjrbvb) - Placehold.it images have a new link

## R4 Day 29: 2021-06-29 Tuesday

Attempted to add editing and adding ability for Recipe app ingredients, but ended up scrapping it. 

## R4 Day 28: 2021-06-28 Monday

Looking into [implementing internationalization](https://dev.to/adrai/how-to-properly-internationalize-a-react-application-using-i18next-3hdb) (i18n) for my Recipe app, but running into some issues with wrapping the export class in the library. [(Example)](https://www.codeandweb.com/babeledit/tutorials/how-to-translate-your-react-app-with-react-i18next) May try it on a simpler app, or non-React project another time.

## R4 Day 27: 2021-06-27 Sunday

Fixed 3-year old issue with my [Recipe App search](https://fcc-recipe.herokuapp.com/)! It turns out the [key for the card component](https://github.com/virtual/fcc-recipe-box/commit/6ab07f003946ed7db86ffcf4f7425d4bd723fd47#diff-46882322b44ef809269ece297270640b0509766c1ce82a6338855b5b83b590ad) wasn't correct which was causing the wrong results to cache/render. Also spent a good chunk of time playing with outdated node_modules.

## R4 Day 26: 2021-06-26 Saturday

Starting freeCodeCamp Information Security, Python for Penetration Testing

Socket: an internal endpoint for sending and receiving data (analogy: outlet)

Types:
1. TCP - transmission control protocol (IPV4 or IPV6)
1. UDP


## R4 Day 25: 2021-06-25 Friday

[Styling broken images](https://codepen.io/virtual/pen/BaRBajq) with CSS

## R4 Day 24: 2021-06-24 Thursday

Finished the [Probability Calculator](https://replit.com/@virtual/probability-calculator) and claimed my [Scientific Computing with Python certification!](https://www.freecodecamp.org/certification/virtual/scientific-computing-with-python-v7) Pretty excited :)

## R4 Day 23: 2021-06-23 Wednesday

Sick day but did learn a bit more about Python's random library. It's more predestined randomization--it always gives the same "random" result given the same inputs. (Good for testing...) It can instead be re-written using SystemRandom()

```py
sr = random.SystemRandom()
# for truly random use sr
# randomSelection = random.choice(contents)
randomSelection = sr.choice(contents)
```

## R4 Day 22: 2021-06-22 Tuesday

Battling it out with Python and bash; turns out I just needed a restart. 😅

Did end up changing my launch.json for python (internalConsole from integratedTerminal), so now it has different colors. (Not sure if it's better...)

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: Current File",
      "type": "python",
      "request": "launch",
      "program": "main.py",
      "console": "internalConsole"
    }
  ]
}
```

Passing test #2, but... why is always returning `['blue', 'red']` for a "random" choice?

## R4 Day 21: 2021-06-21 Monday

Started the fifth python project--[Probability Calculator](https://replit.com/@virtual/probability-calculator), passing 1/3 tests.

## R4 Day 20: 2021-06-20 Sunday

Finished [Polygon Area Calculator](https://replit.com/@virtual/fcc-polygon-area-calculator)! Seemed a lot easier than the last challenge. :D

## R4 Day 19: 2021-06-19 Saturday

Started [Polygon Area Calculator](https://replit.com/@virtual/fcc-polygon-area-calculator) 

## R4 Day 18: 2021-06-18 Friday

Finished [Python Budget App](https://replit.com/@virtual/virtual-fcc-budget-app)! 🎉 Calculated percentages overall for withdrawals and added accurate representations for the bar chart. A  nifty function:

- `max(names, key=len)` - get the longest length item in a list (then take its length)

## R4 Day 17: 2021-06-17 Thursday

Setup the vertical labels for the categories for the Python Budget App.

## R4 Day 16: 2021-06-16 Wednesday

🌑

## R4 Day 15: 2021-06-15 Tuesday

Working through the final python project #3, started setting up the bar chart; also worked on a definition to center the category title when printing the given category object.

## R4 Day 14: 2021-06-14 Monday

Simple day of python on sololearn app

## R4 Day 13: 2021-06-13 Sunday

Tests #8-10 of Budget app passing; need to still center the title of the instance dynamically.

Overriding what is returned when calling the instance obj by overriding `__str__` in the Class; roughly:

```py
def __str__(self):
    output = ''
    for iter in range(len(self.ledger)):
      output = output + str(self.ledger[iter]['amount'])
    return f'{output}'
```

Using [Sphinx documentation for Python](https://www.sphinx-doc.org/en/master/usage/restructuredtext/domains.html#python-signatures) is helpful for later auto-generating docs.

Example:

```py
def transfer(self, amount, targetCategory):
  '''
  Send a message to a recipient

  :param float amount: The amount of money to transfer
  :param str targetCategory: The target category to transfer to
  :return: `True` if the transfer took place, and `False` otherwise
  :rtype: boolean
  :raises ValueError: if the targetCategory exceeds 160 characters
  :raises TypeError: if the targetCategory is not a basestring
  '''
```

Had a bit of fun at looking at more profile customizations & updated my GitHub profile a bit with [Spotify stats](https://spotify-recently-played-readme.vercel.app/) from [JeffreyCA](https://github.com/JeffreyCA), also their project [spleeter web](https://github.com/JeffreyCA/spleeter-web) looks really neat. Will need to check out :)

## R4 Day 12: 2021-06-12 Saturday

Python Project #3: [Budget App](https://replit.com/@virtual/virtual-fcc-budget-app)

Revising Python and [objects from py4e](https://www.py4e.com/lessons/Objects#)

- **Class** - a template `Dog`
- **Method or Message** - A defined capability of a class `bark()`
- **Field or attribute** - A bit of data in a class `length`
- **Object or Instance** - A particular instance of a class `Lassie`

Use `dir(var)` to list all the items/methods inside a variable

Use [dictionaries](https://docs.python.org/3/tutorial/datastructures.html#dictionaries) for a structure like `{'jack': 4098, 'sape': 4139}`

## R4 Day 11: 2021-06-11 Friday

Back to python, setup the Budget App locally; tried adding a few lines of code to the class but it's obvious I completely forgot everything about python classes.

## R4 Day 10: 2021-06-10 Thursday

Added a bit more random sizing, hover effects and interactive note sounds using Tone JS. Done with this project for a bit, not quite going the way I want between the advanced svgs and delays I'd like. And the interactivity, I'm not even sure what I want. 

## R4 Day 9: 2021-06-09 Wednesday

Added animation delay and better handling for performance; only showing svg changes on submit. 

A few gotchas:

- Animation needs to include `forwards` otherwise it will revert to original style
- React relies on the key to know if should rerender a specific element (otherwise animation-delay was not firing when key stayed the same)
- Use `shouldComponentUpdate` to check if the component should re-render. By default it seems every component is re-rendering everytime anything changes!

[Sentiment Analyzer](https://github.com/virtual/sentiment-analyzer) - 
`count your lucky stars okay star star star rawr star star circle mew star`



## R4 Day 8: 2021-06-08 Tuesday

`i hate cirlces and stars`

Oh, no, not really. But now my sentiment app adds svgs based on how many certain words appear (cirlce, star) with a very badly performing regex! You can also click them and see a nice console log.


## R4 Day 7: 2021-06-07 Monday

Lifted the state for the sentiment analysis value for my [sentiment analyzer](https://sentiment-analyzer.virtual.repl.co/) and added some coloring based on positive / negative, and attempted to do some saturation value (HSL) based on just how intense the result is.

Learned about using `isInfinite()` instead of checking if a var equals `Infinity` (doesn't work)
 

## R4 Day 6: 2021-06-06 Sunday

Configured my [sentiment analyzer to run on replit](https://sentiment-analyzer.virtual.repl.co/)!

Overview of [changes](https://github.com/virtual/sentiment-analyzer/commit/ef16254386d4fa46e9be1e799bd0a2fcd02fc0ed):
- Run `npm run build` in public folder
- Remove `build` folder from `public/.gitignore`
- Add an `.env` to the replit app `NODE_ENV` set to `production`
- Add conditional logic to to app.js to serve files if on prod

Updated app.js:
```bash
require('dotenv').config();

if (process.env.NODE_ENV === 'production') { 
  app.use(express.static("./public/build"));
} else {
  app.use(express.static("public"));  
}
```

Added logging and debugging with log4js

A few ideas:
- Check for certain words and add X amount svgs that are related (stars, hearts, skulls, lulz)
- Other things could be unique if found in the text (city skyline)
- Slow svg animation or something
- Change color/theme based on sentiment rating
- Then add audio to these svgs on interaction


Also updated my Heroku apps since they have an necessary upgrade (The Heroku-16 stack is end-of-life).

## R4 Day 5: 2021-06-05 Saturday

Added a [textarea to input words/lyrics](https://github.com/virtual/sentiment-analyzer) and then using Axios, make a post request to node which then queries my original function to output the sentiment value. :)

Looks like if I want this to run on replit, I need to set up some [environment variables](https://marcopeg.com/2019/nodejs-backend-on-repl-it)


## R4 Day 4: 2021-06-04 Friday

Considering a sentiment analyzer to potentially create an interactive app that can later use a sound library

A few notes:

- Lyrics repeat a lot of words, but I also tried to remove repeats, and that didn't seem to be a good solution
- Need to create a custom word list to filter lyrics like "yeah" that might repeat several time (and have a positive sentiment)
- Phrases like "shooting stars" become negative--any way to better process phrases? :\

Resources:

- [Stopwords](https://github.com/fergiemcdowall/stopword) - words to filter out
- [Building a sentiment analysis app with Node.js](https://blog.logrocket.com/sentiment-analysis-node-js/)

## R4 Day 3: 2021-06-03 Thursday

- Finished the [second python project for FCC](https://replit.com/@virtual/boilerplate-time-calculator)!

Learned there's no case statements for python, but may be coming soon :)

## R4 Day 2: 2021-06-02 Wednesday

Not very pretty but now passing tests 2-5 for the [Time Calculator](https://github.com/virtual/fcc-python-projects/blob/master/time-calculator/time_calculator.py) &middot; [(Replit)](https://replit.com/@virtual/boilerplate-time-calculator)

Working with the Python debugger to check my values

- `str(min).zfill(2)` - for left padding numbers with 0s (07 vs 7)
- python uses `elif` not `elseif` 

## R4 Day 1: 2021-06-01 Tuesday

### Audio JS Libraries

- [Tone.js](https://tonejs.github.io/)
  - [Inspiration: Yume](http://www.unseen-music.com/yume/)
  - [Tweakable](https://tweakable.org/)
  - [More examples](https://tonejs.github.io/demos)
- [pizzicato](https://alemangui.github.io/pizzicato/) - Might need to try to make a song with this

To reset your Github account on VSCode after enabling 2FA use:

```bash
git config --global --unset credential.helper
```

### Python Project #2: Time Calculator

Run debugger with `F5` in VSCode; set up `launch.json` if needed, e.g.

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Python: Main File",
      "type": "python",
      "request": "launch",
      "program": "main.py",
      "console": "integratedTerminal"
    }
  ]
}
```

Implemented code to pass the first test for the [Time Calculator](https://github.com/virtual/fcc-python-projects/blob/master/time-calculator/time_calculator.py)

Tidy code to split a string and assign it as ints to two variables:

```python
dHours, dMins = map(int,duration.split(':'))
```

## 👑 👑 Round 4 begins 👑 👑

Ideas for Round 4 starting June 1, 2021

- [Bouncy Panda phaser](https://codepen.io/virtual/pen/QWjaRRo)
- [Phaser](https://www.codecademy.com/courses/learn-phaser/lessons/learn-phaser-basics/exercises/hello-world)
- javascript 30
- python projects
- [python sololearn app](https://www.sololearn.com/learning/1073) for when i'm lazy 
- [Microservices with Node JS and React](https://www.udemy.com/course/microservices-with-node-js-and-react/)
- advanced scss stylelinting
- fix my old app databases
- [Libworx](https://github.com/virtual/libworx)
- create a virtual pet site
- read Code Complete
- [build out more of toy-factory!](https://virtual.github.io/toy-factory/)
- check out https://apexcharts.com/ for item leveling charts
- [Javascript design patterns (MVC)](https://classroom.udacity.com/courses/ud989)
- [make search work on recipe app; make list items editable](https://fcc-recipe.herokuapp.com/)
- broken image css
- music-related javascript?
