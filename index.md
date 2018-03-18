# #100DaysOfCode

## R2 Day 35: 2018-03-18 Sunday

Played with creating a sprite in my [Toy Factory](https://github.com/virtual/toy-factory), eventually a part of the Dungeon Crawler app for freeCodeCamp R2D35/#100DaysofCode

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
