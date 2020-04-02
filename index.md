# #100DaysOfCode


## ⭐ Some ideas for round 3: ⭐ 

- Read 10 pages of Code Complete
  - Day 10: History of programming languages
- Continue developing out [Libworx](https://github.com/virtual/libworx)
- Develop out [Knight University using TailwindCSS](https://virtual.github.io/knightu/)
- Consider apps that might help Toastmaster groups online (Timer, Feedback forms)
- Continue through [Javascript30](https://javascript30.com/)
  - Day 01: Challenge 08 ✓
  - Day 09: Challenge 09 ✓
- Animations / maniuplations with SVG
- Create a game with an isometric view
- Create a virtual pet site
- Update server for TLS
- Mod a game (Minecraft)
- Complete lessons in freeCodeCamp
  - Information Security and QA section
    - Day 05: Finish new Javascript Algorithm challenges, began ChaiJS
    - Day 06: Continue testing with ChaiJS
    - Day 07: Finish testing with ChaiJS ✓
    - Day 08: Complete HelmetJS & bcrypt ✓
    - Day 11: Pug/Passport - Node & Express
    - Day 12: Passport - Node & Express
    - Day 13: Passport - Node & Express
- [React Storybook with Emma Bostian (FEM)](https://livestream.com/accounts/4894689/events/9027490/videos/202820134)
- [CSS In-Depth, v3, Estelle Weyl (FEM)](https://frontendmasters.com/workshops/css-in-depth-v3/)
  - Day 02: Intro and review of failures
  - Day 03: Attribute selectors and specificity
  - Day 04: Pseudo-selectors

----------

## R3 Day 13: 2020-04-02 Thursday

> Continuing @freecodecamp's passport authentication and trying to debug errors preventing tests to pass even though it works. Frustrating! 😣
> 
> I hope all your coding adventures have been more rewarding today! R3D13/#100DaysOfCode

There are so many issues and gotchas with this chapter outlined in a myriad of forum posts and GitHub issues.

Time for me to leave this challenge and hope when I get back to it, it's been given some TLC. I tried a GitHub PR for the page title issues, but it was rejected.


## R3 Day 12: 2020-04-01 Wednesday

> Just like any time I do server setup, spending way too much time debugging silly things like page titles... 
> 
> Is there anyone with @freecodecamp approval access that can review the PRs for this repo? R3D12/#100DaysOfCode
> https://github.com/freeCodeCamp/boilerplate-advancednode/pulls

[Glitch project](https://glitch.com/~virtual-fcc-node-security)

Serialization of a User Object

_To serialize an object means to convert its contents into a small key essentially that can then be deserialized into the original object. This is what allows us to know whos communicated with the server without having to send the authentication data like username and password at each request for a new page._

Authentication Strategies

_A strategy is a way of authenticating a user._

## R3 Day 11: 2020-03-31 Tuesday

> Markdown links—someone once shared that "Brackets" comes before "Parenthesis" alphabetically, and I haven't screwed up creating a link since! 💙 (Thank you!)
> 
> Working on @freeCodeCamp's Node & Express section, starting with 🐶 #PugJS templates. R3D11/#100DaysOfCode

- [Pug docs](https://github.com/pugjs/pug)
- [Pug Templates, Introduction to Advanced Node and Express Challenges - Glitch project](https://virtual-fcc-node-security.glitch.me/)

### Pug code example:

``` pug
doctype html
html(lang="en")
  head
    title= pageTitle
    script(type='text/javascript').
      if (foo) bar(1 + 5)
  body
    h1 Pug - node template engine
    #container.col
      if youAreUsingPug
        p You are amazing
      else
        p Get on it!
      p.
        Pug is a terse and simple templating language with a
        strong focus on performance and powerful features.
```

### Passport

_It's time to set up Passport so we can finally start allowing a user to register or login to an account! In addition to Passport, we will use Express-session to handle sessions. Using this middleware saves the session id as a cookie in the client and allows us to access the session data using that id on the server. This way we keep personal account information out of the cookie used by the client to verify to our server they are authenticated and just keep the key to access the data stored on the server._

```js
const session = require('express-session')
const passport = require('passport')

// ...

app.use(session({
  secret: process.env.SESSION_SECRET,
  resave: true,
  saveUninitialized: true,
}));

// passport. initialize() is a middle-ware that initialises Passport. Middlewares are functions that have access to the request object (req), the response object (res), and the next middleware function in the application's request-response cycle
app.use(passport.initialize())

// passport.session() acts as a middleware to alter the req object and change the 'user' value that is currently the session id (from the client cookie) into the true deserialized user object.
// `app.use(passport.session());` is equivalent to `app.use(passport.authenticate('session'));`
app.use(passport.session())
```

## R3 Day 10: 2020-03-30 Monday

> Making R3D10/#100DaysOfCode an easier day, reading through the history of languages on Code Complete.
> 
> Amused by this tidbit: "The acronym PHP originally stood for Personal Home Page." 

Language History from _Code Complete_ (ed.2, pp 63-66)

LL = Low-level
ML = Mid-level
HL = High-level
OOL = Object-oriented 

- Ada (HL) - embedded systems, named after Adam Lovelace
- Assembly language (LL) - assembler for a single machine instruction, used in processors
- C (ML) - originally associated with UNIX OS, extensive use of pointers and addresses, used for microcomputers 1980-1990s
- C++ (OOL) - classes, exception handling, templates, compatible with C
- C# (OOL) - programming environment developed by Microsoft, used for dev on Microsoft platforms
- Cobol - DOD, mathematical and object-oriented. Stands for COmmon Business-Oriented Language
- Fortran (HL) - Scientific and engineering applications, stands for FORmula TRANslation
- Java (OOL) - Sun Microsystems, platforms convert Java source code to bye code and runs in a virtual machine
- JavaScript - Client-side programming
- Perl - used for administration tasks, building scripts, report generation. Stands for Pratical Extraction and Report Language
- PHP - Can be embedded in web pages and present database info, originally stood for Personal Home Page but now stands for PHP: Hypertext Processor
- Python (OOL) - Interpreted, used for writing scripts
- SQL - Structured Query Language - is declarative language meaning that it does not define a sequence of operations, but rather the result of some operations
- Visual Basic (HL) - Developed at Dartmouth College in 1960s, stands for Beginner's All-purpose Symbolic Instruction Code


## R3 Day 9: 2020-03-29 Sunday

> Another #javascript30 down! Neat console logging ideas like formatting as errors, custom styles & grouping. Added  @prismjs for syntax highlights.
> 
> I return for the intro riff 🎶 & stay for the great content from Wes Bos. 😉  
https://virtual-javascript30.herokuapp.com/09-dev-tools/index.html R3D9/#100DaysOfCode

- [JavaScript 09 Dev Tools](https://virtual-javascript30.herokuapp.com/09-dev-tools/index.html)
- [JavaScript 30 Repo](https://github.com/virtual/javascript30)

## R3 Day 8: 2020-03-28 Saturday

> R3D8/#100DaysOfCode Completed #Helmetjs/bcrypt for 
@freeCodeCamp's Information Security and QA section.
> 
> Have any of you finished this certification? Thinking face I'm curious about what the projects are like and would love to see your GitHub repos/examples! #womenintech

### Applied InfoSec Challenges

#### HelmetJS 

_HelmetJS is a type of middleware for Express-based applications that automatically sets HTTP headers to prevent sensitive information from unintentionally being passed between the server and client. While HelmetJS does not account for all situations, it does include support for common ones like Content Security Policy, XSS Filtering, and HTTP Strict Transport Security, among others. HelmetJS can be installed on an Express project from npm, after which each layer of protection can be configured to best fit the project._

- `contentSecurityPolicy` for setting Content Security Policy	 
- `dnsPrefetchControl` controls browser DNS prefetching
- `frameguard` to prevent clickjacking
- `hidePoweredBy` to remove the X-Powered-By header
- `hsts` for HTTP Strict Transport Security
- `ieNoOpen` sets X-Download-Options for IE8+
- `noSniff` to keep clients from sniffing the MIME type
- `referrerPolicy` to hide the Referer header	 
- `xssFilter` adds some small XSS protections

Resources 
- [HelmetJS Challenges - Glitch Project](https://virtual-fcc-helmetjs.glitch.me)
- [HelmetJS Docs](https://helmetjs.github.io/docs/)

#### BCrypt 

_BCrypt hashes are very secure. A hash is basically a fingerprint of the original data- always unique. This is accomplished by feeding the original data into an algorithm and returning a fixed length result. To further complicate this process and make it more secure, you can also salt your hash. Salting your hash involves adding random data to the original data before the hashing process which makes it even harder to crack the hash._

_BCrypt hashes will always looks like `$2a$13$ZyprE5MRw2Q3WpNOGZWGbeG7ADUre1Q8QO.uUUtcbqloU0yvzavOm` which does have a structure. The first small bit of data `$2a` is defining what kind of hash algorithm was used. The next portion `$13` defines the cost. Cost is about how much power it takes to compute the hash. It is on a logarithmic scale of 2^cost and determines how many times the data is put through the hashing algorithm. For example, at a cost of 10 you are able to hash 10 passwords a second on an average computer, however at a cost of 15 it takes 3 seconds per hash... and to take it further, at a cost of 31 it would takes multiple days to complete a hash. A cost of 12 is considered very secure at this time. The last portion of your hash `$ZyprE5MRw2Q3WpNOGZWGbeG7ADUre1Q8QO.uUUtcbqloU0yvzavOm`, looks like one large string of numbers, periods, and letters but it is actually two separate pieces of information. The first 22 characters is the salt in plain text, and the rest is the hashed password!_

- [Understand BCrypt Hashes - Glitch Project](https://virtual-fcc-bcrypt.glitch.me)

## R3 Day 7: 2020-03-27 Friday

> Finished Unit and Functional testing for @freecodecamp.
> 
> I was always curious about how to test an actual form. #ChaiJS can mimic filling in a form & submitting it, and test the output on the screen.
> 
> Assertions cheat sheet: https://devhints.io/chai
R3D7/#100DaysOfCode 

[Chai Testing Repo](https://github.com/virtual/boilerplate-mochachai) running on [Heroku](https://fcc-boilerplate-mochachai.herokuapp.com/)

``` javascript
suite('Functional Tests', function () {
  test('submit "surname" : "Vespucci" - write your e2e test...', function (done) {
    browser
    // fill the form, and submit.
    .fill('surname', 'Vespucci')
    .pressButton('submit', function(){
      // assert that status is OK 200
      browser.assert.success(); // 200
      // assert that the text inside the element 'span#name' is 'Amerigo'
      browser.assert.text('span#name', 'Amerigo', 'name should be Amerigo');
      // assert that the text inside the element 'span#surname' is 'Vespucci'
      browser.assert.text('span#surname', 'Vespucci', 'surname is Vespucci');
      // assert that the element(s) 'span#dates' exist and their count is 1
      browser.assert.element('span#dates', 1, 'dates element exists');
      // assert.fail();
    })
    done();
  });
});
```


## R3 Day 6: 2020-03-26 Thursday

> R3D6/#100DaysOfCode Another day working with Chai on @freeCodeCamp. I'm impressed with the flexibility of tests like "approximately." 
> 
> Spent a while debugging my testing scripts until I realized I had the wrong branch set to be automatically deployed on Heroku--oops! 🙄

## R3 Day 5: 2020-03-25 Wednesday

> Happy to now be a monthly supporter for @freeCodeCamp! 
>
> R3D5/#100DaysOfCode 
Started working through the testing curriculum; worked out how to manage via GitHub and Heroku (instead of Glitch) so my workflow is much happier. 🤗 https://github.com/virtual/boilerplate-mochachai 

[Chai Testing Repo](https://github.com/virtual/boilerplate-mochachai) running on [Heroku](https://fcc-boilerplate-mochachai.herokuapp.com/)

*Note on CSS Update for reduced motion:*

``` css
@​media (prefers-reduced-motion: reduce) {
  *,
  *:after,
  *:before {
    animation: none !important;
    transition: none !important;
  }
}
```

## R3 Day 4: 2020-03-24 Tuesday

> R3D4/#100DaysOfCode In-range but still invalid? 
Here's a pen to help you understand the difference between :invalid and :out-of-range CSS psuedo-selectors. Example from 
@FrontendMasters
 CSS In-Depth. https://codepen.io/virtual/pen/abORwjw?editors=0100




### Psuedo-selectors

Selectors that match based on the current state of the UI

`:valid`

`:invalid` (out of range and/or unmatched step value)

`:required`

`:optional`

`:in-range`

`:out-of-range` (out of range, ignores step)

`:user-invalid` Similar to on blur


## R3 Day 3: 2020-03-23 Monday

> R3D3/#100DaysOfCode I'll admit, I don't use these much (aside from form styling), and many have been around since CSS2! Do you ever style your elements this way?
> 
> Reviewing selectors, specificity, and gotchas with 
@estelle
—you know, for the next CSS trivia night. Winking face

### Selectors
 

Selector: "The part that comes before the declaration block"

Pseudo-classes have the same selector weight as classes (0 - 1 - 0)

### Attribute selectors

`[attribute]` Has the attribute (e.g. [type])

`[attribute='value']` Equal to the exact value only

`[attribute~='value']` Includes the full word 'value'

`[attribute|='en']` Equal to "en" specifically or "en-" followed by anything

`[attribute^='val']` Starts with (e.g. 'https:')

`[attribute$='lue']` Ends with (e.g. ".pdf")

`[attribute*='alu']` Has anywhere 

## R3 Day 2: 2020-03-22 Sunday 

> Interesting information on CSS failures and faux-commenting while you're testing code as shown from CSS in Depth (v3) with 
@estelle, @FrontendMasters. 
> 
> If you style CSS, take a peek at all these less common selectors! https://drafts.csswg.org/selectors-4/#overview R3D2/#100DaysOfCode

Began [CSS In-Depth, v3, Estelle Weyl (FEM)](https://frontendmasters.com/workshops/css-in-depth-v3/)

- ✓ Introduction
- Selectors
- Specificity
- Generated Content
- Media Queries
- Units and Values
- Colors & Transparency
- Math (variables, calc, etc)
- Text and fonts
- Box Model
- Float & Flexbox
- Tables
- CSS Grids
- Backgrounds & Images
- Gradients
- Transforms
- Transitions and Animations
- Other features
- File organization

## R3 Day 1: 2020-03-21 Saturday 

> Scrubbed my toaster, cleaned my knife set, cut my finger, and then decided maybe I should start #100daysofcode back up instead. 
> 
> Challenge 8/#javascript30--now enjoying this mindnumbingly fun canvas board I can now doodle on like it's 2002. R3D1 https://virtual-javascript30.herokuapp.com/08-canvas/index.html

Starting Round 3 of #100DaysOfCode--honestly for a mental health break from reading #covid19 info; getting back into Javascript30 

- Added overdue favicon to JS30
- Created a canvas drawing board for [Challenge 8 of #javascript30](https://virtual-javascript30.herokuapp.com/08-canvas/index.html) 

--------

## ⭐ ⭐ Round 3 begins ⭐ ⭐

--------

## 2018-09-03 Monday

Finished Udacity's Accessibility course. 

-------------

Logging Graphic Design on Google Keep

## 2018-04-15 Sunday

Worked on Project Briefs in Lynda's [Planning your Project](https://www.lynda.com/Graphic-Design-tutorials/Understanding-needs-your-client/419419/479098-4.html)

- Drew 20 Parmigianos logo samples
- Created typeface palette
- Worked on menu layout - 14 x 11 and a Kid's menu
- Worked through Illustrator project setting up the logo from a sketch using shapes and creating 3 versions (color, inverse, black) of the logo; exported to png

## 2018-04-14 Saturday

Started working on the [Lynda - Graphic Designer path](https://www.lynda.com/learning-paths/Design/become-a-graphic-designer)

Finished: 

- [What is Graphic Design](https://www.lynda.com/Graphic-Design-tutorials/What-Graphic-Design/614734-2.html)
- [Graphic Design Careers: First Steps](https://www.lynda.com/Design-tutorials/Graphic-Design-Careers-First-Steps/497761-2.html)

Working through [Intro to Graphic Design](https://www.lynda.com/Graphic-Design-tutorials/Introduction-Graphic-Design/419419-2.html)

- Typography: Typeface palettes, anatomy of, terminology
- Colors: emotional effects of color

> I learned about #Design on Lynda.com. I completed Graphic Design Careers: First Steps by @kristinellison  https://www.lynda.com/Design-tutorials/Graphic-Design-Careers-First-Steps/497761-2.html?certificate=85B2DBD03120450E8AF21F20AB82FDD6&utm_medium=certificateshare&utm_source=twitter

------------

## Starting Graphic Design #100DaysOfCreativity~


Choosing not to continue with Round 2, but I wrote up a blog of some of [my favorite apps](https://www.satinflame.com/blog/2018/04/apps-and-tiny-tools/) from last few years

-------

## R2 Day 57: 2018-04-11 Wednesday

Working through some React challenges on freeCodeCamp beta! https://beta.freecodecamp.org/en/challenges/react/create-a-simple-jsx-element

## R2 Day 56: 2018-04-10 Tuesday

Watched more of Tyler McGinnis's react bootcamp. A good reminder to use the callback function style for this.setState()

Got work's server on CloudFlare! It's amazing <3

## R2 Day 55: 2018-04-09 Monday

> Too slow to win :P but we had a great night with @tylermcginnis and @freeCodeCamp Bozeman walking through the challenges! R2D55/#100DaysOfCode

Remember:  Babel = makes JSX code run in the browser without having to write React.createElement everywhere!

Updated my server to PHP 7.2 and got my first laravel project running

## R2 Day 54: 2018-04-08 Sunday

> Realizing I'm a little inexperienced with left navigation sweeping in from the side, I spent the morning playing with it on CodePen. There are some nice examples on https://www.w3schools.com/howto/howto_js_sidenav.asp but need a little TLC. https://codepen.io/virtual/full/JLwjKz/ 

## R2 Day 53: 2018-04-07 Saturday

Read more of chapter 3 of Code Complete about architecture requirements

## R2 Day 52: 2018-04-06 Friday

Read more of chapter 3 of Code Complete about project requirements; started architecture requirements

## R2 Day 51: 2018-04-05 Thursday

> "Requirements are like water. They're easier to build on when they're frozen." Read more on defining program requirements and their importance from #codecomplete. Also added HP bar and death/restart to my game. 

## R2 Day 50: 2018-04-04 Wednesday

> Day 50! #freecodecamp Dungeon Crawler continues... Added HP potions and a weapon. So close yet still so far; still need to add a boss, more weapons, levels, and that whole dying bit.
R2 #100DaysOfCode https://virtual.github.io/toy-factory/ 

## R2 Day 49: 2018-04-03 Tuesday

> Added darkness toggle, experience points and the ability to kill off cute little pandas #freecodecamp Dungeon Crawler. R2D48/#100DaysOfCode https://virtual.github.io/toy-factory/ 

## R2 Day 48: 2018-04-02 Monday

> Continuing on my #freecodecamp Dungeon Crawler, there's now walls and my player can bump into them! (Hooray for little victories.) R2D48/#100DaysOfCode https://virtual.github.io/toy-factory/ 

## R2 Day 47: 2018-04-01 Sunday

> My player can now move around the board for my Toy Factory #freecodecamp Dungeon Crawler! https://virtual.github.io/toy-factory/ R2D47/#100DaysOfCode

## R2 Day 46: 2018-03-31 Saturday

> Updated BS4 sliders to use Slick Slider and implemented a fancy Skip to Main (focus) content region for my faux Knight University. Celebrating Easter with the folks! 🐇 R2D46/#100DaysOfCode

## R2 Day 45: 2018-03-30 Friday

Spent 3 hours fighting with Vagrant on my PC. Think I've got it worked out using the exact same process as my Mac now. R2D45/#100DaysofCode

## R2 Day 44: 2018-03-28 Wednesday

OUTC18 Hackathon--teamed up with Adam S.! Created a Gadget using the @omniupdate API that sends messages to users. #MyFirstGadget R2D44/#100DaysOfCode

## R2 Day 43: 2018-03-27 Tuesday

Worked on implementing a Google App Script to pull data from a Google Sheet

## R2 Day 42: 2018-03-25 Sunday

Changed setup for toy factory and worked on C# for Sololearn. Big day of traveling with OmniUpdate for the OUTC18! Hung out with Jim Heiney and went to House of Blues Anaheim and some shops in the Garden Walk. :)

## R2 Day 41: 2018-03-24 Saturday

📕 Read chapter 3.1-3.3 of Code Complete on defining program prerequisites. 

Determine whether prerequisites need to be defined using a sequential or iterative approach.

➡️ Sequential:

- low risk
- familiar application and implementation
- design is well understood

🔄 Iterative:

- high risk
- unfamiliar application
- complex/hard to understand

❓ Determine problem definition: ask what the problem is using clear language. The "problem definition" should not include a solution or technical jargon.

## R2 Day 40: 2018-03-23 Friday

[Laravel twbs4](http://virtual-laravel-twbs4.herokuapp.com/) 

- Worked on the search functionality
- Added spotlight carousel, think I might switch to implementing SlickSlider for more styling options
- Added meta

## R2 Day 39: 2018-03-22 Thursday

Added in a responsive mega menu using Bootstrap 4 to my Knight Univesity page. http://virtual-laravel-twbs4.herokuapp.com/ R2D39/#100DaysOfCode

## R2 Day 38: 2018-03-21 Wednesday

> Practicing some Flexbox Zombies tonight because my brain isn't functioning enough to think about my current projects. 🏹 "...Never pays to be shady!" R2D38/#100DaysOfCode  

Just a little practice of Flexbox zombies. 

## R2 Day 37: 2018-03-20 Tuesday

> Did some cleanup and maintenance on my GitHub repos/pages. Read Ch1 of #CodeComplete on what "construction" entails. 🌮 ...And made tacos! R2D37/#100DaysOfCode 

Moved my Game of Life app off of Heroku (previously fcc-game-of-life.herokuapp.com) to [Github](https://virtual.github.io/fcc-game-of-life/)

Made a [PR for Habit100](https://github.com/OppNHeimer/habit100/pull/1) to add in some mobile styling

Code Complete: Read Ch. 1 about construction--what it encompasses, why "coding" is not quite an accurate word (it simply means translating into computer language).

## R2 Day 36: 2018-03-19 Monday

> Reviewing a skills checklist for full-stack developers and noting which areas I still need to focus on. Also, invested in this 900-page book on best practices. Wish me luck! Moved my panda sprite into a responsive grid and started creating a game board for the #freecodecamp Dungeon Crawler challenge. https://virtual.github.io/toy-factory/ 

### [Full-Stack Developer: The Definitive Guide](https://medium.com/coderbyte/a-guide-to-becoming-a-full-stack-developer-in-2017-5c3c08a1600c)

Reviewing which parts I need to work more on.

#### 1. HTML/CSS

_Almost every single program, whether online or in-person, that is teaching you how to be a web developer will start with HTML and CSS because they are the building blocks of the web. Simply put, HTML allows you to add content to a website and CSS is what allows you to style your content. The following topics related to HTML/CSS come up often in interviews and on the actual job when you’re working:_

- [x] Semantic HTML.
- [x] Be able to explain the CSS Box Model.
- [x] Benefits of CSS preprocessors.
- [x] CSS Media Queries to target different devices and write responsive CSS.
- [x] Bootstrap

#### 2. JavaScript

_The JavaScript language is growing more popular every year and new libraries, frameworks, and tools are constantly being released. Based on the Stack Overflow 2016 Developer Survey, JavaScript is the most popular language in both Full-Stack, Front-end, and Back-end Development. It’s the only language that runs natively in the browser, and can double up as a server-side language as well (as you’ll see below with Node.js). Below are some topics you need to understand as a Full-Stack Developer:_

- [x] Understand how to work with the DOM. Also know what JSON is and how to manipulate it.
- [ ] Important language features such as functional composition, prototypal inheritance, closures, event delegation, scope, higher-order functions.
- [ ] Asynchronous control flow, promises, and callbacks.
- [ ] Learn how to properly structure your code and modularize parts of it, things like webpack, browserify, or build tools like gulp will definitely be helpful to know.
- [x] Know how to use at least one popular framework. (React)
- [x] jQuery
- [ ] Some knowledge on testing frameworks and why they’re important.
- [x] Learn about some important new ES6 features (optional).

#### 3. Back-End Language

_Once you feel you’ve gotten a good grasp on HTML/CSS and JavaScript, you’ll want to move on to a back-end language that will handle things like database operations, user authentication, and application logic. All online programs and bootcamps usually focus on a specific back-end language, and in reality in doesn’t matter which one you learn so much as long as you understand what is going on and you learn the nuances of your chosen language. You’ll get a ton of different responses if you ask someone which back-end language is the best to learn, so below I’ve listed a few popular combinations. An important note: whichever you decide to learn, just stick with it and learn as much as you can about it — there are jobs out there for all the languages listed below._
 
- [x] Node.js: This is a great option because Node.js is itself just a JavaScript environment which means you don’t need to learn a new language. This is a big reason why a lot of online programs and bootcamps choose to teach Node.js. The most popular framework you’d most likely learn to aid you in developing web applications is Express.
- [ ] Ruby: Some popular frameworks for developing in Ruby are Rails and Sinatra. Plenty of programs teach Ruby as a first back-end language.
- [ ] Python: Some popular frameworks for developing in Python are Django and Flask.
- [ ] Java: The Java language isn’t taught so much these days when it comes to Full-Stack Web Development, but some companies do use Java as their back-end and it is still a very in-demand language (see image above).
- [x] PHP: PHP is rarely taught in programs these days, but just like with Java, it is still very in-demand and it is a cornerstone of the web today.

#### 4. Databases & Web Storage

_When learning to build web applications, at some point you’ll probably want to store data somewhere and then access it later. You should have a good grasp on the following topics related to databases and storage._

- [x] Understand the benefits of relational data, e.g. SQL.
- [x] Learn about NoSQL databases, e.g. MongoDB.
- [x] Understand which would be better in certain situations.
- [x] Know how to connect a database with your chosen back-end language (e.g. Node.js + MongoDB).
- [ ] Understand the benefits of in-memory data stores like Redis or memcached.
- [x] Web storage to store sessions, cookies, and cached data in the browser.
- [ ] Scaling databases, ACID, and ORM (all optional).

#### 5. HTTP & REST

_HTTP is a stateless application protocol on the Internet — it’s what allows clients to communicate with servers (e.g. your JavaScript code can make an AJAX request to some back-end code you have running on a server which will happen via HTTP)._ 

- [x] What is REST and why is it important in regards to the HTTP protocol and web applications.
- [x] Best practices for designing a RESTful API. POST/GET requests.
- [x] Learning how to use Chrome DevTools can be extremely helpful.
- [x] What are SSL Certificates.
- [ ] HTTP/2 & SPDY (optional).
- [ ] WebSockets, Web Workers, and Service Workers (all optional).

#### 6. Web Application Architecture

_Once you think you have a grasp on HTML/CSS, JavaScript, back-end programming, databases, and HTTP/REST, then comes the tricky part. At this point if you want to create a somewhat complex web application, you’ll need to know how to structure your code, how to separate your files, where to host your large media files, how to structure the data in your database, where to perform certain computational tasks (client-side vs server-side), and much more._

_There are best practices that you can read about online on, but the best way to actually learn about application architecture is by working on a large application yourself that contains several moving parts — or even better, working on a team and together developing a somewhat large/complex application._

_This is why, for example, someone with 7+ years of experience may not necessarily know CSS or JavaScript better than someone with 2 years of experience, but over all of those years they’ve presumably worked with all sorts of different applications and websites and have learned how to architect and design applications (among learning other important things) to be most efficient and can see the “big picture” when it comes to development. Below are some things you can read that will help you learn how to architect your web applications efficiently:_ 

- [x] Learn about common platforms as a service, e.g. Heroku and AWS. Heroku allows you to easily upload your code and have an application up and running with very little configuration or server maintenance and AWS offers dozens of products and services to help with storage, video processing, load balancing, and much more.
- [ ] Performance optimization for applications and modern browsers.
- [ ] Some opinions on what a web application architecture should include.
- [ ] Designing Web Applications by Microsoft.
- [x] MVC.
- [x] Most importantly though you should try to work on projects with people, look at codebases of popular projects on GitHub, and learn as much as you can from senior developers.

#### 7. Git

_Git is a version control system that allows developers working on a team to keep track of all the changes being made to a codebase. It’s important to know a few important things related to Git so that you understand how to properly get the latest code that you’ve missed, update parts of the code, make fixes, and change other people’s code without breaking things. You should definitely learn the concept behind Git and play around with it yourself._

- [x] Here’s a reference list of some common git commands you’ll likely use.
- [x] Here’s a tutorial on using Git and GitHub for beginners.

#### 8. Basic Algorithms & Data Structures

_This topic is somewhat polarizing in the development world because there are developers who don’t think there should be such a heavy focus on computer science topics like tree traversal, sorting, algorithm analysis, matrix manipulation, etc. in web development. However, there are companies like Google that are notorious for asking these types of questions in their interviews. As someone said about the Front-End engineering interview at Google:_

_That said, as Ryan McGrath mentions, our front-end (FE) engineers are expected to have a solid CS background, like all our engineers. While there are companies that practically require applicants to have a computer science degree or equivalent, there are plenty of companies that will hire people without this technical qualification if they can prove that they know how to develop applications and show an understanding of the whole domain. But part of being a competent developer and not writing inefficient code or using the wrong tools is an understanding of some basic algorithms and data structures and being able to analyze trade-offs. So here are some things you should definitely learn:_

- [ ] Improving your Algorithms & Data Structure Skills Article
- [ ] Study hash tables and try to understand them on a deeper level. This data structure underlies objects in JavaScript (dictionaries in Python and hashes in Ruby).
- [ ] Understand how trees and graphs can be beneficial as data structures.
- [x] Understand the basics of Big-O analysis so you don’t do silly things like create a nested loop 3 levels down if you don’t need to!
- [ ] Know when to use an object vs an array and understand the trade-offs.
- [ ] Learn why caching is so important when working with a large amount of data. Also learn the pros and cons of in-memory vs disk storage.
- [x] Learn the difference between queues and stacks.

## R2 Day 35: 2018-03-18 Sunday

Played with creating a sprite in my [Toy Factory](https://github.com/virtual/toy-factory), eventually a part of the Dungeon Crawler app for freeCodeCamp R2D35/#100DaysofCode

Created [demo with board](https://virtual.github.io/toy-factory/). Ran out of space on Heroku, so checking out Github pages more! 

- Added `"homepage": "https://virtual.github.io/toy-factory/"` to the package.json
- Modified build script: `"build": "rm -rf docs && react-scripts build && mv build docs",` in package.json

## R2 Day 34: 2018-03-17 Saturday

Worked a little on javascript 30 Challenge 5 flexbox image gallery

## R2 Day 33: 2018-03-16 Friday

Added fancybox video player (and some sweet Manchester Orchestra videos) to my [Laravel demo](http://virtual-laravel-twbs4.herokuapp.com/)

Finished ch3 of Flexbox zombies

## R2 Day 32: 2018-03-15 Thursday

Finished the first #D3 challenge in @freeCodeCamp! 📊 I'm pretty proud to have worked out the logic for the scales and method chaining, as well as the styles for a *responsive* vertical bar chart! R2D32/#100DaysOfCode https://codepen.io/virtual/full/XEXVpp/

Laravel Homestead for twbs4:

```
cd ~/Homestead
vagrant up
```

## R2 Day 31: 2018-03-14 Wednesday

> Working more on the D3 challenge for @Freecodecamp. It helped to think about how I would do it in HTML/CSS first and then translate that back into D3 functions/JS. R2D31/#100DaysOfCode https://codepen.io/virtual/full/XEXVpp/

## R2 Day 30: 2018-03-13 Tuesday

> Finished reviewing setup for Debian servers; learned you can use zcat/zless to read files that are gzipped. Also did some Haml, flexbox and D3 for a small mock resume on codepen. R2D30/#100DaysOfCode

Finished reviewing [chapter 3](https://www.lynda.com/Linux-tutorials/Configure-HTTP-server/664829/710621-4.html?autoplay=true) on setting up Apache/Debian on a web server.

Practed Haml markup, a little D3 and flexbox in the start of a simple [Web resume](https://codepen.io/virtual/full/XEXVpp/)

## R2 Day 29: 2018-03-12 Monday

> Watching some videos from Lynda's Linux Foundation Cert Prep series & happened upon managing SSH keys... so I organized my SSH keys using an SSH config file! So tidy! ✨ R2D29/#100DaysOfCode 

Watching some videos from Lynda's [Linux Foundation Cert Prep: Service Configuration (Ubuntu)](https://www.lynda.com/Linux-tutorials/Configure-SSH-based-remote-access-using-publicprivate-key-pairs/664829/710619-4.html?autoplay=true) series and learned about managing SSH keys... so I organized my SSH keys using an SSH config file! Related walkthrough: [Simplify Your Life With an SSH Config File](http://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/)

## R2 Day 28: 2018-03-11 Sunday

> "Worked out" some challenges doing Array Cardio! #javascript30 R2D28/#100DaysOfCode https://virtual-javascript30.herokuapp.com/04-arrays/index.html

## R2 Day 27: 2018-03-10 Saturday

> Added a polyfill to one of my #javascript30 programs so it would run in older browsers; checked out a D3/React ex in Github (w/ PR: https://github.com/virtual/d3-explorer) and started challenge 4 data setup. R2D27/#100DaysOfCode

Added [padStart polyfill](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/padStart) to JavaScript30 challenge 2 (clock) so it works for older browsers.

Played with this [D3 library example](https://github.com/virtual/d3-explorer) and updated the .eslintrc file so the program would run for me. Made a PR in case this is helpful--accepted!  

Began working on challenge 4 data

## R2 Day 26: 2018-03-09 Friday

> RS26: Added a procfile to my heroku install so now my #javascript30 application is working! Completed challenge #3 -- CSS variables. https://virtual-javascript30.herokuapp.com/index.html #100DaysOfCode

```text
web: vendor/bin/heroku-php-apache2 /
```

## R2 Day 25: 2018-03-08 Thursday
> R2D25 - PR accepted for updates to these "Spark Notes" for the Pragmatic Programmer. 💪 Lots of great information—check it out! #100DaysOfCode https://github.com/HugoMatilla/The-Pragmatic-Programmer

## R2 Day 24: 2018-03-07 Wednesday

> Refined the styles for my video grid section inspired by the amazing UX designer [Krista Lacida](http://www.kristalacida.com/contact/). (Video functionality to come later.) 

I first coded the play area without flexbox--it was much more classy using flexbox! Also I learned about using the box-shadow for overriding initial text-decorations (including line size and color.)

When implementing the JS, I'll want to find a way to tag the current playing one with an active status and maybe lighten the box... (Or maybe that is pointless, since the video player will be overlaid over the page?)

Anyhow, enjoying how it's coming together ;)

## R2 Day 23: 2018-03-06 Tuesday

> Learning about adding models (data) to views (page layouts) in Laravel. https://www.lynda.com/Laravel-tutorials/Create-forms/604257/648654-4.html?autoplay=true R2D23/#100DaysOfCode

## R2 Day 22: 2018-03-05 Monday

> Continuing to play with Bootstrap 4 and Laravel for my fictitious Knight University! http://virtual-laravel-twbs4.herokuapp.com/ R2D22/#100DaysOfCode

## R2 Day 21: 2018-03-04 Sunday

> Got a simple Laravel app running on Heroku. Learning about pulling views into layouts, added in FontAwesome and some Bootstrap overrides. R2D21/#100DaysOfCode http://virtual-laravel-twbs4.herokuapp.com/

## R2 Day 20: 2018-03-02 Friday

> TGIF! Today learning about Laravel controllers from [Lynda's Laravel 5 Essential Training](https://www.lynda.com/Laravel-tutorials/Laravel-5-Essential-Training-1-Basics/604257-2.html). Looking forward to some Halo 4 🎮 LAN partying tonight! R2D20/#100DaysOfCode

## R2 Day 19: 2018-03-01 Thursday

> Learning some of the Laravel file structure and got Bootstrap 4 working on my welcome blade! (I need to get used to running my commands from my Vagrant terminal.) R2D19/#100DaysOfCode

Playing with getting Bootstrap 4 up and running within Laravel 5.6. Shoved some BS4 HTML within the welcome "blade." Some useful code bits to get it working:

CSRF Token seems to help calm a console error. 

```html
<meta name="csrf-token" content="{{ csrf_token() }}">
<link href="{{ asset('css/app.css') }}" rel="stylesheet">
```

JS after footer:

```html
<script src="{{ asset('js/app.js') }}"></script>
```

I've added some more scss changes to the `resources/assets/sass` folder. 

From the ssh on Vagrant, run `npm install` and then compile using `npm run dev` or `npm run watch-poll` (since it doesn't work with just `npm run watch` on my VM). More on these commands from the [Laravel 5.6 docs](https://laravel.com/docs/5.6/mix#sass)

## R2 Day 18: 2018-02-28 Wednesday

> Woohoo! I finally have Laravel running on a local Vagrant instance. @jcs224 I hope you are proud! 🎉 It only took me since October. R2D18/#100DaysOfCode

I am probably flip-flopping around too much, but I really want to start building a Bootstrap 4 template of an existing design. I'm hoping to do it using some smart setup, and now I'm researching Laravel again. With Vagrant. With VirtualBox, and Composer.

I got stuck on the [install instructions](https://laravel.com/docs/5.6/homestead), thinking that cloning the Homestead repo was if the vagrant homestead library didn't work correctly, but now I understand. ScotchIO's [Getting started with Laravel Homestead](https://scotch.io/tutorials/getting-started-with-laravel-homestead) also helped me over some setup hurdles.

Currently, I'm to the point where I have set up some overrides for my Homestead yaml:

```yaml
# ~/Homestead/Homestead.yaml
---
ip: "192.168.10.10"
memory: 2048
cpus: 1
provider: virtualbox
mariadb: true

authorize: ~/.ssh/id_rsa.pub

keys:
    - ~/.ssh/id_rsa

folders:
    - map: ~/code
      to: /home/vagrant/code

sites:
    - map: homestead.test
      to: /home/vagrant/code/test/public

    - map: laravel1.test
      to: /home/vagrant/code/laravel1/public

databases:
    - homestead
```

And as luck would have it--now I'm learning how to write better code blocks in Markdown! :)

- [Handy Vagrant commands](https://www.drupal.org/node/2008794)


Now I can `vagrant ssh` and run `composer global require "laravel/installer"`

~~In my folder /home/vagrant/code/test I'm running `laravel new public`...~~

That wasn't exacty right.... Laravel creates it own public folder, so I should run `laravel new test` instead from /home/vagrant/code

But... There is a Laravel homepage showing! This is the furthest Laravel progress I've made.


## R2 Day 17: 2018-02-27 Tuesday

> Learning about Unity and the object controls. R2D17/#100DaysOfCode

Finished "Learn" tutorials from Unity's homescreen 3/4

## R2 Day 16: 2018-02-26 Monday

> Finished the third part of SoloLearn's C# tutorials. Might start playing with Unity this week thanks to suggestions from @idwardis R2D16/#100daysofcode

- http://catlikecoding.com/unity/tutorials/

## R2 Day 15: 2018-02-25 Sunday

> Continuing to learn C# on SoloLearn. Getting more practice at the pre-increment and post-increment functions--a little tricky! R2D15/#100daysofcode

## R2 Day 14: 2018-02-24 Saturday

> Learning C# this weekend on @SoloLearn thanks to their fantastic mobile app. R2D14/#100DaysOfCode

## R2 Day 13: 2018-02-23 Friday

> Started learning D3 for charts. Loved the Scrimba video but can't quite understand the API docs. Going to need more tutorials to figure this out! #freecodecamp R2D13/#100DaysOfCode

https://codepen.io/virtual/pen/MQqwby

## R2 Day 12: 2018-02-22 Thursday

> Kept thinking about this Game of Life setup between dreaming, haha. 👾 Feels awesome to complete a #freecodecamp React game challenge in three days! (Now to catch up on that sleep!) R2D12/#100DaysOfCode https://fcc-game-of-life.herokuapp.com/

Also enjoyed implementing a range slider--I've never done that before (maybe a little overdue)!

## R2 Day 11: 2018-02-21 Wednesday

> Continuing to work through the Game of Life #freecodecamp. The logic isn't quite right yet, but it does transform enough to make me feel semi-productive! R2D11/#100daysofcode https://fcc-game-of-life.herokuapp.com/

## R2 Day 10: 2018-02-20 Tuesday

> 🎲 Set up the game board for the #freecodecamp [Game of Life](https://fcc-game-of-life.herokuapp.com/) challenge<br/>
> ✈️ Lifted the state & refactored data using a multidim array with on/off passed down as a prop to each square<br/>
> R2D10/#100daysofcode

## R2 Day 9: 2018-02-19 Monday

> Began a Software Dev course on EdX and took a peek at the requirements for the next #freecodecamp challenge--Game of Life. (Fascinating stuff!) R2D9/#100DaysOfCode https://www.edx.org/micromasters/software-development

Started looking at [EdX - Software Development](https://www.edx.org/micromasters/software-development) for understanding good software design as recommended by Smai. 

_Course >  1a: Beginning Student Language  > Expressions >  Expressions, pt 1_<br>
Dr Racket is taking a bit too long to download so I'll have to continue that another time. 

Began looking at FreeCodeCamp's [Game of Life challenge](https://codepen.io/freeCodeCamp/full/reGdqx).

## R2 Day 8: 2018-02-18 Sunday

> Created a #javascript30 Clock (02) using CSS transforms and JS. 🕑 A good review of the date functions too! R2D8/#100DaysOfCode

[02-Clock Code](https://github.com/virtual/javascript30/tree/master/02-clock)

## R2 Day 7: 2018-02-17 Saturday

> Edit on update and save completed for my #freecodecamp Recipe App and *submitted!*--all before breakfast! (Since I want some of my data pretty, it only works on new additions.) https://fcc-recipe.herokuapp.com/ R2D7/#100DaysOfCode

Some issues, but I'm so done with this for now:

- Search is no longer functioning; the data is pulling but it gets lost on the way (I think indexing problem)
- Some color accessibility
- Edit form can be prettier

## R2 Day 6: 2018-02-16 Friday

Working on edit functionality for #freecodecamp Recipe box; maybe I'll get the save/update to work tomorrow... No wonder this thing hasn't been finished yet. 😪 R2D6/#100DaysOfCode

✅ Transform text to inputs on form<br/>
✅ Implemented logic for client to pass updated data<br/>
❌ Input boxes need states so they can change<br/>
❌ Server route/Mongo query needed for update <br/>


## R2 Day 5: 2018-02-15 Thursday

> 📚 Another round of working on my media catalog app <br/>
> 🕰️ Added in more session checking <br/>
> 🛍️ Rewrote dashboard so users can view their own collection of movies<br/>
> R2D5/#100DaysOfCode

## R2 Day 4: 2018-02-14 Wednesday

> Finished rewriting [Cat Clicker Premium](https://github.com/virtual/js-design-patterns) using MVC structure. It's such a foreign structure to me... It's so tidy. Seriously digging this @Udacity course from @benjaffe! R2D4/#100DaysOfCode https://classroom.udacity.com/courses/ud989 

(Sick today 🤒 but made it through work and finished a giant spreadsheet.) Also registered with Shoreline to go to OmniUpdate conference this March, so that is super exciting!

### Model
The data. Make a nice object literal and stick the information in it. The view should never modify the model directly, and vice versa.

### View
The objects users see on the screen and interact with. If there is a common structure, put it into the HTML. The view functions can then populate those DOM elements.

### Controller
The link between the View and the Model. If someone clicks on an item in the view that changes the data, the _controller_ must be the one to update the model. Controller functions might cause re-renders of views after the data has been changed.

## R2 Day 3: 2018-02-13 Tuesday

> 🐱 Working through MVC reorganizing challenges from Udacity Design Patterns with Lesson 2 - Cat Clicker Premium! https://classroom.udacity.com/courses/ud989 R2D3/#100DaysOfCode 

## R2 Day 2: 2018-02-12 Monday

> 🎥 Reorganized my code so my collections can reference IMDb IDs more easily<br/>
> 🔲 Logged in users can click a button-wow!<br/>
> 🎨 Did a little art with a poster placeholder graphic<br/>
> R2D2(🤖 hehe)/#100daysofcode

Learned about __5-4-3-2-1__ from @smaifullerton-wk: "5,4,3,2,1 is to motivate yourself to do something when you don’t have motivation - all it means is you say in your head 5, 4, 3, 2, 1 and then without further thought you get up and start working on the thing. it sounds kinda nutty and obvious but it really works, because it doesn’t give your brain an opportunity to argue against doing whatever it is you don’t feel motivated to do but know you should. It doesn’t really create motivation, it builds discipline to push past resistance to doing good things."

## R2 Day 1: 2018-02-11 Sunday

> Starting Round 2 of #100DaysOfCode with my React/MySQL project! Join me 😉 <br/>
> ❌ No progress on listing a user's movie collection<br/>
> ☑️ Moved some functions into a React store for better data accessibility<br/>
> 🤔 Planning to do mostly app dev & Javascript30

- Starting a new round! (Commencing Tuesday May 22, 2018)
- Attempted to display a movie tagged in user collection but ran into state errors; I'll need to do a refresher on initialized state, Promises etc.
- Moved movie functions to a new Movie Store on [LibWorx](https://github.com/virtual/libworx)

--------

## ⭐ ⭐ Round 2 begins ⭐ ⭐

--------

### [Blog: No Turning Back: A Journey through Montana Code School](https://www.satinflame.com/blog/2017/12/no-turning-back-montana-code-school/)

With a large amount of experience and self-study under my belt, I was ready to commit to finally getting the full exposure of modern web development with Montana Code School. Discover what I learned and view the projects my teams created. [Read more...](https://www.satinflame.com/blog/2017/12/no-turning-back-montana-code-school/)


--------

## Day 100: 2017-12-01 Friday

> 🎉 Day 100/#100DaysOfCode 🎉 It's been a great ride! https://virtual.github.io/100daysofcode/ 
 
- Teach others as you can–it's the best way to solidify a concept
- Learn github well & contribute!
- Always consider your team's thoughts

@digitalocean #hacktoberfest 💙 #freecodecamp

## Day 99: 2017-11-30 Thursday

> Does this count as my first iphone? 😜 Working in xcode is amazing for #ReactNative. No more issues with connectivity and rebooting Expo all the time. Did styling & history updates. #mtcs07boz 99/#100DaysOfCode

## Day 98: 2017-11-29 Wednesday

> 🏆 Updating my sites to use the holy grail layout with #flexbox 🃏 Learning Jest with Enzyme for #javascript testing 🎈 Celebrating my birthday with good food & friends! 98/#100DaysOfCode

## Day 97: 2017-11-28 Tuesday 

> Added validator & zxcvbn password strength checker (amazing!) to sign up form and tweaked styles. (Took me awhile to realize that's named after the bottom row of the keyboard!) ;P 97/#100DaysOfCode https://github.com/dropbox/zxcvbn 

## Day 96: 2017-11-27 Monday

> Moving along with this coffee app, added in more Material Design and MomentJS. Going to try out xcode instead of Expo for React Native tomorrow--tired of fighting connections. 96/#100DaysOfCode

## Day 95: 2017-11-26 Sunday

> Not feeling so ambitious this holiday weekend so enjoying a fun "game" of zombie destruction with Flexbox Zombies! Thanks for the recommendation @PeteCapeCod ;) 95/#100DaysOfCode #ReactNative https://geddski.teachable.com/p/flexbox-zombies

## Day 94: 2017-11-25 Saturday

> Looking into @omniupdate's gadgets, and I'm very impressed with @jesseclark's public repos and kind sharing of gadget code. (Thank you!) I'm excited that I may be able to put my recent learning to use in OU. 94/#100DaysOfCode

## Day 93: 2017-11-24 Friday

> Know some #React but curious to understand how #VueJS works? This great vid @traversymedia goes through an overview of the similarities and how to set it up! https://www.youtube.com/watch?v=z6hQqgvGI4Y 93/#100DaysOfCode #freecodecamp

## Day 92: 2017-11-23: Thursday

🦃 Thanksgiving 🦃

> Happy Thanksgiving everyone! I'm #ThankfulFor @freeCodeCamp #100DaysOfCode @udemy @mtcodeschool @LambdaSchool and all my fellow coders for the motivation and inspiration throughout this year! 😘

- Need to check out [Github Passport Authentication](https://github.com/CalebCox/VotingApp)

## Day 91: 2017-11-22: Wednesday

> ☕ MobX with React Native for a Coffee app = working! Experiencing Python/Pi fun with my @mtcodeschool project teammate and a four-letter pHAT. Ready for a four-day weekend. #mtcs07boz 91/#100DaysOfCode

- [React Native with MobX — Getting Started](https://medium.com/react-native-training/react-native-with-mobx-getting-started-ba7e18d8ff44)
- [Passing props to StackNavigator](https://github.com/react-community/react-navigation/issues/876)

## Day 90: 2017-11-21: Tuesday

> React Native: moving forward. 🚀 Sign up and login routes working; learning about the navigator and refreshing my flexbox muscles! 90/#100DaysOfCode

- Idea: Make 100DaysOfCode day generator (Day 1 - 100 with day)
- Watching [React Native from Tyler McGinnis](https://egghead.io/lessons/react-start-building-a-react-native-application)

## Day 89: 2017-11-20: Monday

> I don't think mobile apps are for me. Another frustrating day trying to develop in React Native. 😥 89/#100daysofcode

- [React Native SVG Converter](https://github.com/goopscoop/svg-to-react-cli)

## Day 88: 2017-11-19: Sunday

> Started developing with React Native: successfully added a button... Also, played around with my new Raspberry Pi! 💻 88/#100DaysOfCode

- Code School: GoLang

## Day 87: 2017-11-18: Saturday

> My afternoon was "abducted" by @codeschool's Close Encounters with #PHP! (Next up: more Laravel!) https://www.codeschool.com/courses/close-encounters-with-php 87/#100DaysOfCode

## Day 86: 2017-11-17: Friday

> Yay! Got a form file input saving uploaded images to an S3 Bucket with help from @heroku's great walkthrough. https://devcenter.heroku.com/articles/s3-upload-node 86/#100DaysOfCode #javascript #womenintech

## Day 85: 2017-11-16: Thursday

> Got out for a fun @DTNBZN Ladies Night in between 8 hours of integrating Material Design, SVG animation, S3 configurations and a nice #javascript Meetup with @jcs224! 85/#100DaysOfCode https://codepen.io/virtual/pen/Ebbxae

- Never count on users reading documentation
- [Intro.js](https://introjs.com/) • [Installation](https://introjs.com/docs/getting-started/install) provides a interactive way for users to learn how to use your site
- [Intro.js React wrapper NPM](https://www.npmjs.com/package/intro.js-react)
- Keep track if it should run (stepsEnabled) with a newUser flag or similar on user accounts

## Day 84: 2017-11-15: Wednesday

> Great @mtcodeschool Q&A with @Wisetail about learning new technology, using domain modeling & design patterns, along with book recommendations like Clean Code & The Pragmatic Programmer. #mtcs07boz 84/#100DaysOfCode

- Visit from Wisetail Q&A
- Visit from Zoot Enterprises
- [CodeSchool.com - Try Laravel](https://www.codeschool.com/courses/try-laravel)
- [Status Errors](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes#4xx_Client_errors)
- [Manually sending response code](https://stackoverflow.com/questions/26066785/proper-way-to-set-response-status-and-json-content-in-a-rest-api-made-with-nodej)

## Day 83: 2017-11-14: Tuesday

> Raspberry Pis, post-its, and messing more with @socketio & @materialdesign. Lots of learning today, but maybe not so much progress 😛 83/#100DaysOfCode #javascript

- [Cofee Pot Pi on Heroku](https://coffee-pot-pi.herokuapp.com/)

## Day 82: 2017-11-13: Monday

> Starting our second round of @mtcodeschool apps today. Giving @materialdesign another try; will be using React, PostgreSQL, Express, Node and feature coffee! ☕ #mtcs07boz 82/#100DaysOfCode

☕ Starting new project! ☕

- [Coffee Pot Pi](https://github.com/bbalconi/coffee-pot)
- [React Material Design - M Laursen](https://react-md.mlaursen.com/components/buttons)
- [Template Literals for long queries](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)
- [Countdown Timer](http://pughpugh.github.io/react-countdown-clock/)
- [Introduced to React Native](https://github.com/react-community/create-react-native-app)
- [Expo - Easily build apps with React Native](https://expo.io/)

## Day 81: 2017-11-12: Sunday

> So close to finished with this app-just realizing I don't have an edit function. 🍲 Added meta, error message and XSS cleaning for inputs. https://fcc-recipe.herokuapp.com/  81/#100DaysOfCode #freecodecamp

- [Udemy - Raspberry Pi Workshop 2017 Become a Coder / Maker](https://www.udemy.com/raspberry-pi-workshop-become-a-coder-maker-inventor/)
- [Secure XSS Filters](https://github.com/yahoo/xss-filters)

## Day 80: 2017-11-11: Saturday

> Ordered a Raspberry Pi and reviewing Python from @SoloLearn to prepare for a possible next project! (Any suggestions for newbie Pi tutorials?) 80/#100DaysOfCode

- Helped dev with [Flexbox](https://code.sololearn.com/WYze7OQhrS5E/#html)
- [SoloLearn Python 3](https://www.sololearn.com/Course/Python/)
- [https://www.raspberrypi.org/](https://www.raspberrypi.org/)
- [9 amazing projects where Arduino & Art meet!](http://arduinoarts.com/2014/05/9-amazing-projects-where-arduino-art-meet/)
- [Top 10 Raspberry Pi Projects for Beginners](https://lifehacker.com/top-10-raspberry-pi-projects-for-beginners-1791002723)

## Day 79: 2017-11-10: Friday

> Eee! Recipe app finally up and running on @Heroku! My buddy was even kind enough to add his favorite recipe. Needs a little more TLC tomorrow. https://fcc-recipe.herokuapp.com/  79/#100DaysOfCode

- [Recipe Collector - Heroku](https://fcc-recipe.herokuapp.com/)
- Added in dynamic inputs for ingredients

## Day 78: 2017-11-09: Thursday

> Back to working on my @freeCodeCamp #RecipeApp I started in April! Satisfying to finally understand enough to finish it. 78/#100DaysOfCode

## Day 77: 2017-11-08: Wednesday

SQL: Structured Query Language. 

- [Mark's super awesome app](https://github.com/virtual/simple-postgresql-app)
- [Getting Started with PostgreSQL on Mac OSX](https://www.codementor.io/devops/tutorial/getting-started-postgresql-server-mac-osx)
- [Node Postgres](https://node-postgres.com/)
- Heroku can use PostgreSQL
- [Yellowstone Odyssey refactored using PostgreSQL for Login & Sights pages](https://github.com/virtual/yellowstone-odyssey-postgresql)

## Day 76: 2017-11-07: Tuesday

> #Javascript Promises! 🎁 Wish I learned about these earlier.  https://developers.google.com/web/fundamentals/primers/promises https://davidwalsh.name/promises 76/#100DaysOfCode #freecodecamp

- [Yellowstone Odyssey refactored using MobX](https://github.com/virtual/Buffaloed)

## Day 75: 2017-11-06: Monday

> #Thankful for my @mtcodeschool teacher for helping me get Passport working w/ MobX for React (& baking cookies! 🍪) 75/#100DaysOfCode

- [Happy Songs with MobX](https://github.com/virtual/happy-songs)

## Day 74: 2017-11-05: Sunday

> Brain tired; think I'm catching a cold... 😴  pushed thru & submitted exercism_io pangram! http://exercism.io/submissions/8af111c3a4354108bc4e7243299c301d 74/#100DaysOfCode

## Day 73: 2017-11-04: Saturday

> Finished #javascript simple-cipher exercise at exercism_io - Leave me a nitpick at http://exercism.io/submissions/618f04a913e34fa0849395540189581b 73/#100DaysOfCode

## Day 72: 2017-11-03: Friday

> Learned more about Workiva's Missoula team; started working through MobX and problems on exercism_io #mtcs07boz 72/#100DaysOfCode

## Day 71: 2017-11-02: Thursday

> Great connections at our @mtcodeschool demos tonight! Thanks to everyone who came out for support 🎉 #mtc07boz 71/#100DaysOfCode

⭐ Demo Day ⭐

- Yellowstone Odyssey App
- CRUD for Sights administration
- Quizzes save to database
- Scores work and update successfully
- Geolocation worked well
- Asked about authentication framework (Passport)

Wishlist

- Manage state better, possibly with MobX or Redux
- Better authentication
- Check on why Facebook share didn't work
- Cuter badge for Twitter

## Day 70: 2017-11-01: Wednesday

> One day until our demos for @mtcodeschool #mtcs07boz! Refactored code & took team pics 📷 https://yellowstone-odyssey.herokuapp.com/contactinfo  70/#100DaysOfCode

- Refactored Contact page to use Array of info
- Added in Google Analytics
- Fun team photos!

## Day 69: 2017-10-31: Tuesday

> Implemented geolocation w/ Haversine formula calculations to find the closest landmarks! 🗺️ https://en.wikipedia.org/wiki/Haversine_formula 69/#100DaysOfCode

- Haversine NPM to display closest location
- Cleaned up React warnings, added keys
- Added in Save animation for Edit Sights page and redirect to /admin listing

- Finished Hackoberfest 2017 with 11 PRs! Ordered t-shirt!

## Day 68: 2017-10-30: Monday

> My first ever deployment to @Heroku today for a quiz app. To do: Route fixing. https://yellowstone-odyssey.herokuapp.com/  68/#100DaysOfCode #mtcs07boz

- Fixed all A tags to [Link tags](http://knowbody.github.io/react-router-docs/api/Link.html) to keep Router working
- Deployed to [Heroku](https://yellowstone-odyssey.herokuapp.com/)
- Changed all fetch calls to use Axios
- Added in dotenv NPM package and set ENV routers 
- Changed all paths to secure (https)

- Missed dentist appointment 🤷

-----------

Week 6 Complete of Montana Code School (Halfway Through!)

----------

## Day 67: 2017-10-29: Sunday

Spent a few too many hours trying to fix my login only to break my signup page.  Time for a lazy Sunday afternoon. 67/#100DaysOfCode

- Signup with Passport working
- Trying to clean up and get login working for a simple login template, but can't get both signup and login cooperating.

📚 Reading: How to Win Friends and Influence People in the Digital Age 

## Day 66: 2017-10-28: Saturday

> Better understanding React state & comps with Colt Steele's Advanced Bootcamp & reading up! https://reactjs.org/docs/thinking-in-react.html 66/#100DaysOfCode

A few takeaways from [Thinking in React](https://reactjs.org/docs/thinking-in-react.html)

- Designer's Photoshop layer names may end up being the names of your React components.
- Components that appear within another component in the mock up design should appear as a child in the (folder) hierarchy.
- Build a static version in React (without state) first, and then add in state after all components are ready

And in deciding state, ask three questions about each piece of data:
1. Is it passed in from a parent via props? If so, it probably isn’t state.
2. Does it remain unchanged over time? If so, it probably isn’t state.
3. Can you compute it based on any other state or props in your component? If so, it isn’t state.

## Day 66: 2017-10-27: Friday

> Built out more CRUD for our Quiz project (MERN app) and played show-and-tell with #mtcs07boz Hello, weekend! 🎉 65/#100DaysOfCode

### MCS

- Created a sights dashboard that allows users to edit and save changes for each 
- Possible to-do: Option to create and delete sights

## Day 64: 2017-10-26: Thursday

> Working on sessionStorage and scoreboards for our Yellowstone quiz app. #mtcs07boz 64/#100DaysOfCode

## Day 63: 2017-10-25 Wednesday

> Built out the logic to save & update scores for our Yellowstone Quiz (MERN) App. #mtcs07boz 63/#100DaysOfCode

## Day 62: 2017-10-24 Tuesday

> Working to understand #reactjs lifecycles, and when to use (or not use) state. + Good company from jakedolan 🍻 62/#100DaysOfCode

- Began [Colt Steele's Advanced Web Dev Bootcamp](https://www.udemy.com/the-advanced-web-developer-bootcamp)

## Day 61: 2017-10-23 Monday

> Continuing to plug away at developing our @mtcodeschool apps. #Bozeman demos 11/2 at @Wisetail! #mtcs07boz 61/#100DaysOfCode

- Reviewed user stories
- Revised MongoDB schemas to include quiz types and scores
- Updated Quiz to resolve scores
- Still working through, not feeling hopeless, but still not all sure of ourselves and what we can/can't do

## Day 60: 2017-10-22 Sunday

> Today trying out some game dev with @melonJS & Tiled Map Editor. Slow-going but satisfying! http://melonjs.github.io/tutorial-platformer/ 60/#100DaysOfCode

Game development with melonJS! 

- [melonJS Platformer Tutorial](http://melonjs.github.io/tutorial-platformer/)
- [melonJS boilerplate](https://github.com/melonjs/boilerplate)
- [Tiled Map Editor](http://www.mapeditor.org/)

## Day 59: 2017-10-21 Saturday

> Had trouble working with an NPM quiz module, so I spent the day writing my own to work the way I wanted! 🎊 #ReactJS 59/#100DaysOfCode

- Met up with Emily at Coldsmoke and worked through some updates ☕
- Updated and optimized images
- Learned you can make a fork of an NPM and manage it independently as an NPM resource
- You must restart react manually if you make a change to JS outside the scope of normally watched files (eg NPM)
- Decided to write Quiz module ourselves so we could manage it and implement things that didn't seem to work in the included NPM 

## Day 58: 2017-10-20 Friday

> Neat tool for CORS workarounds: https://crossorigin.me/  Implemented Passport and attempted local storage 58/#100DaysOfCode #mtcs07boz

### MCS 

- Working with [Axios](https://www.npmjs.com/package/axios) for fetches - Promise based HTTP client for the browser and node.js
- Working through CORS issues (unresolved) with National Parks API
- Spent most of the day implementing [Passport for authentication](http://www.passportjs.org/docs)
- Began implementing local storage / sessions but it doesn't seem quite integrated
- Randomized featured cards using React props for order and limit

## Day 57: 2017-10-19 Thursday

> Implemented @LeafletJS and looked into the national parks API (nice docs but CORS issues!) 57/#100DaysOfCode #mtcs07boz

- [React LeafletJS](https://github.com/PaulLeCam/react-leaflet)
- Learned how to request additional fields from the [National Parks API](https://www.nps.gov/subjects/digital/nps-data-api.htm)
- Developed out single Sight info page for Yellowstone Odyssey

## Day 56: 2017-10-18 Wednesday

> A long but productive day: implemented mLab to have a shared mongodb for our team, added data and routes 56/#100DaysOfCode #mtcs07boz

- [mLab for external MongoDB](https://mlab.com/home)
- Long day of getting information to pull for one sight. (Very frustrating!) Missing the understanding of tying React routes to the Express routes (working in Postman!)
- With Mark's help used a different named route to get information for a single sight: /sightInfo instead of /sight/:id

## Day 55: 2017-10-17 Tuesday

> Starting on group projects and building out our @balsamiq wireframes for @mtcodeschool / #mtcs07boz 🐃 55/#100DaysOfCode

- Implemented javascript-quiz-using-json and rebuilt to allow for element to be placed inside a div
- Developed quiz questions
- Added feature card components 

## Day 54: 2017-10-16 Monday

> What do you do when you enjoy using @semanticui but start developing in #ReactJS? 🎉 Celebrate! https://react.semantic-ui.com/elements/button  54/#100DaysOfCode

### MCS 

- [Semantic UI for React](https://react.semantic-ui.com/usage)
- [Jest](https://facebook.github.io/jest/) for TDD in React
- Open Space Technology to generate ideas and processes for project pitching, voting, and team formation

## Day 53: 2017-10-15 Sunday

> So much to learn about #Javascript & web dev; at least we'll never be bored 😉 53/#100DaysOfCode #freecodecamp 

- [freeCodeCamp - Timestamp Microservice](https://www.freecodecamp.org/challenges/timestamp-microservice)
- Headfirst Design Patterns, Observer Pattern (Subject & Subscribers)
- [Six Simple Mind Tricks to Help You Learn JavaScript Faster](https://www.sitepoint.com/mind-tricks-to-learn-javascript-faster/)
- [The MVC Design Pattern in Vanilla JavaScript](https://www.sitepoint.com/mvc-design-pattern-javascript/)

## Day 52: 2017-10-14 Saturday

> Completed #freecodecamp's learnyoumongo challenge & checked out glitch for app dev. 52/#100DaysOfCode

- [Glitch Timekeeper App](https://timestamp-ms-virtual.glitch.me/)
- [learnyoumongo](https://github.com/evanlucas/learnyoumongo)

## Day 51: 2017-10-13 Friday

> Presented our music apps today. Any #recommendations for tuts on using #reactjs with Mongo/Express? 51/#100DaysOfCode #mtcs07boz

## Day 50: 2017-10-12 Thursday

> Halfway through! 🏆 50/#100DaysOfCode Continued working through an app using the @Spotify API https://github.com/virtual/happy-songs #mtcs07boz

## Day 49: 2017-10-11 Wednesday

> We were warned we'd reach a low point during @mtcodeschool. React/Mongo (Upside: it can only get better?) #mtcs07boz 49/#100DaysOfCode

- [Why Learning to Code is So Damn Hard](http://www.vikingcodeschool.com/posts/why-learning-to-code-is-so-damn-hard)

## Day 48: 2017-10-10 Tuesday (45)

Spent a full day tying pieces together for a 🎵 project using the @Spotify API! #mtcs07boz montanacodeschool 45/#100DaysOfCode (48)

### MCS

- [Github Happy Songs Repo](https://github.com/virtual/happy-songs)

## Day 47: 2017-10-09 Monday (48)

> Refactored code and "lifted the state" for this small React app. Beautiful photos from unsplash giphy 48/#100DaysOfCode #mtcs07boz

### MCS

- Use React ["exact" option](https://github.com/ReactTraining/react-router/blob/master/packages/react-router/docs/api/Redirect.md) for home route
- [React Router Intro](https://github.com/virtual/reactRouterIntro)
- [React Weather App (lifted state)](https://github.com/virtual/reactWeatherApp)

## Day 46: 2017-10-08 Sunday (47)

> Submitted 4th PR for #Hacktoberfest & watched videos from @mpjm on functions & promises 🐱🐱🐱 47/#100DaysOfCode

- [Catch Me Github Repo](https://github.com/lap00zza/catch_me/pull/30)

## Day 45: 2017-10-07 Saturday (46)

> My project is currently a mess of React and EJS... but I've got an API loading & @semanticui to make it pretty! 👩‍🎨 46/#100DaysOfCode

### MCS 

- [Broken API - Express Routing](https://github.com/virtual/broken-api)

## Day 44: 2017-10-06 Friday

> Researching how to store keys & secret squirrel passwords in project's config.js. Starting a video library project! 44/#100DaysOfCode

- [Best Practices for Writing React Components - Musefind](https://engineering.musefind.com/our-best-practices-for-writing-react-components-dec3eb5c3fc8)

## Day 43: 2017-10-05 Thursday

> Angered the API gods by accidentally calling React components from each other's template. (Loop!) ☁️ Lesson learned! 43/#100DaysOfCode

### MCS
 
- [React Weather App using OpenWeatherMap API](https://github.com/virtual/reactWeatherApp)
- [Passing Props](https://facebook.github.io/react-native/docs/props.html)
- Arrow functions allow you to run a callback without changing scope
- [Lifting State Up](https://reactjs.org/docs/lifting-state-up.html)

## Day 42: 2017-10-04 Wednesday

> My first #hacktoberfest pull request resulted in a nice note! 🌮🌮 Anyone else trying some? 42/#100DaysOfCode https://hacktoberfest.digitalocean.com/ 

- Pull Request (accepted!) for [AlgoWiki](https://github.com/vicky002/AlgoWiki/pull/75)

### MCS

- New [server setup](https://github.com/virtual/basicExpressWebServer) with server side fetch for Giphy API

## Day 41: 2017-10-03 Tuesday

> 🌈 Because unicorns vomiting rainbows & @reactstrap make ReactJS app development that much more fun. 🌈 41/#100DaysOfCode #mtcs07boz

### MCS

- [reactStuff](https://github.com/virtual/reactStuff/tree/solutions) unicorns and super stahs!

## Day 40: 2017-10-02 Monday

> 2nd round redoing today's suite of @mtcodeschool exercises on async callbacks--it's slowly making sense! 40/#100DaysOfCode #mtcs07boz

### MCS

- [Intro to ES6](https://github.com/virtual/es6Exercises): [Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes), [let](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let), [const](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const), [arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions) and [import/export](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import)
- [Quokka.js](https://quokkajs.com/docs/index.html) - enabled per file

## Day 39: 2017-10-01 Sunday

> Built Colt Steele's RESTful Blog App with fellow #mtcs07boz student Emily! (The blog theme was easily inspired. ☕) 39/#100DaysOfCode

- [RESTful Routing: Hot Cocoa Blog](https://github.com/virtual/restful-routes)
- [RESTful Routing - Udemy Web Developer Bootcamp](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/3919760?start=0)

| Name | Path | HTTP Verb | Purpose | Mongoose Method |
| ---- | ---- | --------- | ------- | ----------------|
| Index | /dogs | GET | List all dogs | Dog.find() |
| New | /dogs/new | GET | Show new dog form | N/A |
| Create | /dogs | POST | Create a new dog, then redirect somewhere | Dog.create() |
| Show | /dogs/:id | GET | Show info about one specific dog | Dog.findById() |
| Edit | /dogs/:id/edit | GET | Show edit form for one dog | Dog.findById() |
| Update | /dogs/:id | PUT | Update a particular dog, then redirect somewhere | Dog.findByIdAndUpdate() |
| Destroy | /dogs/:id | DELETE | Delete a particular dog, then redirect somewhere | Dog.findByIdAndRemove()|

## Day 38: 2017-09-30 Saturday

> Reviewing Express, routes, MongoDB and Ajax. Next up, more practice fetching endpoints with $.get. 37 & 38/#100DaysOfCode #mtcs07boz

## Day 37: 2017-09-29 Friday

### MCS

- [f.lux® screen temperature](https://justgetflux.com/)
- Collaborated & presented [expressMongooseReview](https://github.com/robherrm/expressMongooseReview)

## Day 36: 2017-09-28 Thursday

> A slightly frustrating day trying to figure out MongoDB & CRUD w/ Ajax. I'll be excited when it makes sense! 36/#100DaysOfCode #mtcs07boz

- [jQuery.ajax()](http://api.jquery.com/jquery.ajax/)
- [Using HTTP Methods for RESTful Services](http://www.restapitutorial.com/lessons/httpmethods.html)

## Day 35: 2017-09-27 Wednesday

> Created an Express/Mongo app featuring some of my favorite actresses! 35/#100DaysOfCode #mtcs07boz #javascript https://github.com/virtual/celebrity-app

### MCS
- [RoboMongo](https://robomongo.org/download)
- [Firebase](https://firebase.google.com)

## Day 34: 2017-09-26 Tuesday

> Learning asynchronous vs synchronous executions with 🎉 partying camels 🐫 & postmanclient! 34/#100DaysOfCode #mtcs07boz #javascript

- [Express Updating Route](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/3861604?start=0)

### MCS 

- [Bootstrap 4](https://v4-alpha.getbootstrap.com/) (use script includes on homepage)
- [jQuery](https://code.jquery.com/)

## Day 33: 2017-09-25 Monday

> Playing with crazy, nested timed fading text and word replacement functions! How would you set it up? ;D 33/#100DaysOfCode #mtcs07boz

- Finished [What the Flexbox](https://github.com/virtual/What-The-Flexbox) from Wes Bos!
- [Enlightening the rainbow of its colors](https://medium.com/montanacodeschool/enlightening-the-rainbow-of-its-colors-a3b0f6ba9b0f)
- [John Allwine's Puzzle Popsicle Sticks](https://www.allwinedesigns.com/blog/puzzle-popsicle-sticks)

### MCS (Week 2)

- Review [Chrome Inspect Debugger](https://developers.google.com/web/tools/chrome-devtools/javascript/)
- Chrome [Make a minified file readable](https://developers.google.com/web/tools/chrome-devtools/javascript/reference#format)
- Working through exercises on [JS Basics](https://github.com/virtual/JsBasicsMTCSFT07)
- [Updating a fork to match master](https://gist.github.com/CristinaSolana/1885435)
- [fadeTo() jQuery function](https://api.jquery.com/fadeTo/)

## Day 32: 2017-09-24 Sunday

> Studied with mtcodeschool students to work through #javascript challenges & teach them about innerHTML! 32/#100DaysOfCode #mtsc07boz

## Day 31: 2017-09-23 Saturday

> Developed a small #express app with @semanticui to demo the power of #XSLT to #mtcs07boz! ⚡ https://github.com/virtual/xsl-transform-demo 31/#100DaysOfCode

- [XSLT Demo App](https://github.com/virtual/xsl-transform-demo)
- [Everything you wanted to know about JavaScript scope](https://toddmotto.com/everything-you-wanted-to-know-about-javascript-scope/)

## Day 30: 2017-09-22 Friday

> Finished week 1 of mtcodeschool! Happy (but a bit fried) from all the tools and concepts we've learned. #mtcs07boz 30/#100DaysOfCode

- All [OmniUpdate tagged repos](https://github.com/search?utf8=%E2%9C%93&q=topic%3Aomniupdate+user%3Avirtual&type=Repositories&ref=advsearch&l=&l=)

### MCS

- Review week's topics: Mob programming, TDD (Mocha & Chai), Express, Servers vs. Clients, Node & NPM, Terminal, HTML, DRY (Don't Repeat Yourself) & Inheritance, Hot Keys, Git & Github, Trello, Dependencies, and JS Basics (looping, higher-order functions, string manipulation, conditionals)
- Paired programming & presentation on [consonantsOnly()](https://github.com/Montana-Code-School/FirstWeekReviewMTCS07)

## Day 29: 2017-09-21 Thursday

> Full day of #Javascript! Building "Space Dawgz" app, servers w/ #Express, more #ChaiJS. 29/#100DaysOfCode https://github.com/virtual/mtcs-spacedawgz

- Developed code for [OmniUpdate Image Snippet](https://github.com/virtual/omniupdate-image-snippet)
- JS Meetup: Presentation from jcs224 on [Adonis](https://adonisjs.com/) (MVC Framework for Node.js to write webapps with less code), and Drone app libraries: [Electron](https://electron.atom.io/), [Leaflet](http://leafletjs.com/), [Vue](https://vuejs.org/)

### MCS

- Practiced more [mob programming with testing](https://github.com/Montana-Code-School/JsBasicsMTCSFT07)
- Introduction to Express and setup of [Space Dawgz app](https://github.com/virtual/mtcs-spacedawgz)
- Review of Node & Node Package Manager
- [Enneagram of Personality](https://en.wikipedia.org/wiki/Enneagram_of_Personality)

## Day 28: 2017-09-20 Wednesday

>  Upgrading our test-driven dev programs from plain JS to #MochaJS & #ChaiJS libraries! #mtcs07boz 28/#100DaysOfCode

### MCS

- "Upgraded" [our TDD tests](https://github.com/virtual/tdd-js) to use [Mocha](https://mochajs.org/) and [Chai](http://chaijs.com/)
- Worked on mob programming for [Counting the number of selected letter in string](https://github.com/Montana-Code-School/JsBasicsMTCSFT07) using TDD
- [String.prototype.includes()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/includes)
- [Array.prototype.forEach()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
- [Array.prototype.filter()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
- [Basic vi Commands](https://www.cs.colostate.edu/helpdocs/vi.html)

## Day 27: 2017-09-19 Tuesday

> Learning JS TDD (test-driven development).
> Write test; if passes, write another! 27/#100DaysOfCode https://github.com/virtual/mtcs-tdd #mtcs07boz

### MCS

- Worked on [Test-driven Development](https://github.com/virtual/mtcs-tdd) and mob programming
- Updated [Meteoright App](https://github.com/Montana-Code-School/meteoright)
- Trello for project management

## Day 26: 2017-09-18 Monday

> Day 1 of mtcodeschool / #mtcs07boz! Watched ES6 L1 from LambdaSchool & worked more on #flexbox with wesbos. 26/#100DaysOfCode

### MCS
- Learned Agile processes; used our Kanban board to move tasks around
- Discussed the state of flow and learning
- Intro to the Terminal; made directories, searched for files and set up colors
- Intro to Git / source control using clones
- Practiced mob programming; multiple students around a computer. One to type, one to drive, and the rest to collaborate and work through ideas

### Inspriation

- [Mob Programming video](https://www.youtube.com/watch?v=dVqUcNKVbYg)
- [Flow (vs. Panic vs. Boredom)](http://alifeofproductivity.com/how-to-experience-flow-magical-chart/)
- [Modern Agile](http://modernagile.org/)
- [Bash Completion with Tab](https://debian-administration.org/article/316/An_introduction_to_bash_completion_part_1)
- [What the Flexbox](https://github.com/virtual/What-The-Flexbox)
- [Lesson 1: Learn JavaScript ES6 Mini Bootcamp by Lambda School](https://lambdaschool.com/mini-bootcamp/archive)

---

Start of Montana Code School 2017-09-18 

---

## Day 25: 2017-09-17 Sunday

> (Very belated) improving #Flexbox skills with Wes Bos's great video tutorial. https://flexbox.io 25/#100DaysOfCode #css

- [What the Flexbox WIP](https://github.com/virtual/What-The-Flexbox)

## Day 24: 2017-09-16 Saturday

> Reviewing #Sass on Codecademy & learning more fancy tricks! Use the common part of a property name & colon (:) 24/#100DaysOfCode

- [Reviewing Sass](https://github.com/virtual/sass-play)
- [Designing for Interfaces - online book](http://designingforperformance.com/)
- [Mr. Rogers and the Power of Persuasion](https://www.youtube.com/watch?v=_DGdDQrXv5U) 
- [Flexbox tutorial](https://flexbox.io/) recommended by Gildara (Twitter)

## Day 23: 2017-09-15 Friday

> Added [mobile interaction](https://virtual.github.io/udemy-web-dev-bootcamp-patatap/) & made a github [#100DaysOfCode log](https://virtual.github.io/100daysofcode) for the first 23 days! 

- Update [Patatap](https://virtual.github.io/udemy-web-dev-bootcamp-patatap/) to be mobile friendly (displays random circle & sound)
- Begin developing out [100daysofcode](https://virtual.github.io/100daysofcode/) log


## Day 22: 2017-09-14 Thurs

> Sounds! 🎵 Colors! 🎨 Built an interactive page with PaperJS & [Colt Steele's Patatap](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/3973786?start=0) course. 22/#100DaysOfCode

- Created [Patatap](https://virtual.github.io/udemy-web-dev-bootcamp-patatap/) demo

### Inspiration

- [Counting Grains of Sand with Friends](https://medium.com/montanacodeschool/counting-grains-of-sand-with-friends-8ab777a01aa1)


## Day 21: 2017-09-13 Wed

> Working through a [To-Do from Colt Steele's Web Dev Bootcamp](https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/3861520?start=0). Nice tips on remove() after fadeOut() & on vs click 21/#100DaysOfCode

### Inspiration

- [After the flood - Spark lines](http://aftertheflood.co/projects/atf-spark)


## Day 20: 2017-09-12 Tues

> Start projects using what you know; refine later using what your project needs. https://youtu.be/DFP6UDgVJtE  20/#100DaysOfCode


## Day 19: 2017-09-11 Mon

> I really don't understand it, but I somehow made it through the exercise. #EloquentJS Ch.4 arrayToList() 19/#100DaysOfCode 


## Day 18: 2017-09-10 Sun

> Building up a page using semanticui; mocking up a virtual community news page. Fun to try out all the components! 18/#100DaysOfCode  


## Day 17: 2017-09-09 Sat

> Tried out both materialdesign and semanticui. Definitely loving semanticui's documentation more! 17/#100DaysOfCode


## Day 16: 2017-09-08 Fri

> Taking time to practice making and approving pull requests in github with other mtcodeschool students! #mtcs07boz 16/#100DaysOfCode


## Day 15: 2017-09-07 Thurs

> With help of StackOverflow, I refactored my redundant XSL into dynamic templates. (Managing this was insane before!😓) 15/#100DaysOfCode  


## Day 14: 2017-09-06 Wed

> Submitted my prework for @mtcodeschool and made a simple [Inch/CM converter tool](https://s.codepen.io/virtual/debug/XawEqe/bZAQWyeYVQzM) 14/#100DaysOfCode #mtcs07boz


## Day 13: 2017-09-05 Tues

> Worked on setting up my dev environment on my new MacBook Air & worked through prework for mtcodeschool 13/#100DaysOfCode #mtcs07boz 


## Day 12: 2017-09-04 Mon

> Finished Pairwise & completely finished with #freecodecamp's Front End Development! 🎉 12/#100DaysOfCode  


## Day 11: 2017-09-03 Sun

> WIP ~ Still working on solving pairwise with reduce--last advanced algorithm I have yet to complete! #freecodecamp 11/#100DaysOfCode 


## Day 10: 2017-09-02 Sat

> No repeats please! ☑️ Spent more time fixing regex than I did learning & implementing Heap's algorithm! 10/#100DaysOfCode #freecodecamp 


## Day 09: 2017-09-01 Fri

> Attended a great 406creatives talk on authenticity, innovation & culture diff from googlemaps builders Garima & Alysia. 9/#100DaysOfCode  


## Day 08: 2017-08-31 Thurs

> Finished Symmetric Difference that I gave up on over a year ago! I also may have reworked the modal 👑 #freecodecamp 8/#100DaysOfCode  


## Day 07: 2017-08-30 Wed

> Finished some exercises on #EloquentJS. Met up with a fellow coder to develop ideas for projects this fall! 7/#100DaysOfCode 


## Day 06: 2017-08-29 Tues

> Finally understanding [higher-order functions](https://www.youtube.com/watch?v=BMUiFMZr7vk) with vids from mpjme / Ch. 5 #EloquentJS 6/#100DaysOfCode 


## Day 05: 2017-08-28 Mon

> Finally—that green lock of glory from @letsencrypt! Also ex. 38-42 from [A Smarter Way to Learn JavaScript](http://www.asmarterwaytolearn.com/js/index-of-exercises.html) 5/#100DaysOfCode  


## Day 04: 2017-08-27 Sun

> Completed [ex. 29-37--date conversions & functions](http://www.asmarterwaytolearn.com/js/index-of-exercises.html) & migrating sites to digitalocean ❤️ 4/#100DaysOfCode 


## Day 03: 2017-08-26 Sat

> Learned correlation & finished ch. 4 of #EloquentJS (& Migrated email to zoho—great docs!) 3/#100DaysOfCode  


## Day 02: 2017-08-25 Fri

> Backing up files from site5. Thinking of moving to digitalocean & zoho for SSL support. Ch4/arrays of #eloquentjs 2/#100DaysOfCode 


## Day 01: 2017-08-24 Thurs

> Finished my [portfolio migration from #Wordpress to GoHugoIO](http://www.satinflame.com)  Next up: implement letsencrypt 1/#100DaysOfCode
