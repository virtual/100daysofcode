## Day 77: 2017-11-08: Wednesday

SQL: Structured Query Language. 

- [Mark's super awesome app](https://github.com/virtual/simple-postgresql-app)
- [Getting Started with PostgreSQL on Mac OSX](https://www.codementor.io/devops/tutorial/getting-started-postgresql-server-mac-osx)
- [Node Postgres](https://node-postgres.com/)
- Heroku can use PostgreSQL

## Day 76: 2017-11-07: Tuesday

> #Javascript Promises! 🎁 Wish I learned about these earlier.  https://developers.google.com/web/fundamentals/primers/promises https://davidwalsh.name/promises 76/#100DaysOfCode #freecodecamp

## Day 75: 2017-11-06: Monday

> #Thankful for my @mtcodeschool teacher for helping me get Passport working w/ MobX for React (& baking cookies! 🍪) 75/#100DaysOfCode

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
