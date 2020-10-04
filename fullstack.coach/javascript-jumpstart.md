# Writing JavaScript Code & Structuring Your Project When You Don't Have Much Time

__This is an open-source Work In Progress, living [on GitHub]() and cross-posted with [CrossPost](), any valuable feedback and suggestions will be incorporated in the next 3 weeks. Thank you for reading and supporting! 🙏 Read the original article over at [fullstack.coach]()__

It's a very common situation: Maybe you are an entrepreneur, a student, or even something like a backend developer. You are living your life and doing your everyday work.

Suddenly, you have an idea! Or someone else has. This idea needs to be shown to the people. So, you download a well-looking bootstrap template and off you go! As the idea grows, you get more inspirations on what cool stuff you could implement to showcase your idea.

Probably want to add some badass animation to amaze your visitors, a cool interaction to bind them in and some interesting facts that you decide to pull from an API.

Even more suddenly, you feel like the extentsion of the website's JavaScript feels cumbersome and not an easy walk. You are faced with a huge eco-system of...

* different advise
* evolving EcmaScript standards and APIs
* people screaming which JavaScript framework is the best
* Node.js stuff
* NPM packages
* an empty `/js` folder
* vanilla ice

But no reason for desperation, since we have the yummi ice, mmmhh...

## Where should I start?

In the above situation, where you don't have much experience with frontend JavaScript developemnt and you also don't have much time, your best bet is to execute on the one thing that will bring you up to speed most quickly.

["Vanilla JavaScript"]() is powerful and it's baked into every browser. You won't need to care about anything but learning and applying the fundamentals of it to realize your project.

VanillaJS has its downsides too because it seems like you can just build anything with it. Other people do. But since it's probably world's most flexible "framework", you'll have to make almost **all of the decisions** about almost everything **on your own**! In my dark far past I haven't put any thought into **HOW** to build a pure JS project. 

I was like,

> "I know the basics! What can go wrong? Hack away!"

Presently, those projects are all lying dead, in a non-human-readable and non-machine-readable mess of spaghetti (sorry, if you get really hungry by now).

So, making the choice to go with VanillaJS won't be a "Just jump in coding". But going this route, we have already eliminated major evil roadblocks that otherwise would constantly occupy our mental memory:

* different advise on coding best practices
* evolving EcmaScript standards and APIs
* ~~people screaming which JavaScript framework is the best~~
* ~~Node.js stuff~~
* ~~NPM packages~~
* an empty `/js` folder
* vanilla ice

At least for now, we won't need to think much about this stuff. Although, people will still scream a lot, that's just unavoidable.

So let's get the yummi vanilla ice and fill the empty `/js` folder with it!

## Structure the /js folder

I'd assert, a `/js` or `/scripts` folder comes with nearly every random web boilerplate or template you've chosen (unless you are using [the motherfucking website framework](https://motherfuckingwebsite.com/) maybe). Sometimes it's found inside an `/assets`, `/static` or `/resources` folder.

The naming doesn't matter too much, choose your preference.

### Directory structure

Consider something like this for structuring your project:

```bash
projec-root/
├── static/
│   ├── js/
│   │   ├──main.js
│   │   ├──index.js
│   │   ├──other.js
│   │   └──lib/
│   ├── css/
│   ├── img/
│   ├── data/
│   └── vendors/
├── index.html
└── other.html
```

### Entry points for `<scripts>`

Whenever you write scripts or rely on 3rd party libraries or plugins, you load additional JavaScript to your page.

Generally speaking, when you do load your the easiest and most obvious way is to do it right in your HTML:

```html
<script src="./static/js/main.js"></script>
<script src="https://www.gruggletagger.com/gtag/js?id=UA43-1"></script>
```

If you add scripts like this to every one of your pages, your scripts become scattered all over the place and you have to keep an eye on the order.

As your site grows, this becomes unmaintainable and also: What if you need to orchestrate your JS modules, plugins, and objects? E.g. if one script creates an object which generates output that's used by another script.

In the above case, you'll need to checkout the single files and make sense of it. If you centralize this process, let's say in a `main.js` or in a `page.js`, then you'll be able to better follow the process.

So now, in your `index.html` you have just 2 scripts:

```html
<!-- Manages third party libraries and plugins that are used on every page -->
<script src="./static/js/main.js"></script>
<!-- Manages all the objects and events that make your index.html so cool and unique -->
<script src="./static/js/index.js"></script>
```

If you have less entry points your program flow becomes clearer to you, other developers, and the weakest player: your future You ;)

### Loading `<scripts>` inside `<head>` or inside `<body>`

Scripts in `<head>`

> Scripts to be executed when they are called, or when an event is
> triggered, are placed in functions.
>
> Put your functions in the head section, this way they are all in one
> place, and they do not interfere with page content.

Scripts in `<body>`

> If your is not placed inside a function, or if your script writes page
> content, it should be placed in the body section.  It is a good idea
> to place scripts at the bottom of the `<body>` element. This can
> improve page load, because script compilation can slow down the
> display.

Right from [this thread](https://stackoverflow.com/a/38407984/5925094).

#### main.js

You will often see a `main.js` file in client-side JS projects and it's often used to run logic that is applicable to all views on your website. What do you think is more sexy, importing your 78 tracking, cookie handling and whatever `<scripts>` on every page one by one or having it all nicely bundled in one file?

Now, you can imagine that `main.js` could grow immensily over time. This is why it'd be even better to have a `main/` directory, where you can modularize your `main.js`. You still don't want to have a dozen of `<script src='main/*.js>` tags, importing all the scripts. A good practice here is to concatenate all the files inside `main/` to a single `main.js` using a build tool (like gulp) [as described below](#Build Tools).

#### A script per view or per functionality

Inside the `/js` folder you can have scripts named according to the view that will import them if it does something very specific to that view.

Let's look at an example for that as well.

If you need a Script that interactively replaces a specific `<p>` tag with some cool text if the user does something specific in your `other.html`, then I'd suggest creating a `other.js` and put the logic in there. However, if you start using the same logic on another page, it's time to factor it out to its own file maybe something like a `replace.js` in `static/js/lib/` will do.

Another great use for `lib/` is [building abstractions](#Abstractions) around 3rd party APIs, data stores and other tight coupling evil-doers.

#### /vendors

If you've downloaded the whole bootstrap, jQuery or whatever other plugin or library, vendors is a good place to gather them. For smaller libraries, plugins, and code thefts you can still use something like the `lib/` directory.

#### /data

Some of your logic might rely on data bits, like .JSONs, .XMLs, and so on. Consider to have a neat place like that for them. A good idea is not access your data files directly, but again, build abstractions around them.

E.g. if you have a `countries.json`, you probably might want to have a `countries.js` with hip functions like `getAllCountries()` and `pickRandomCountry()`.

### Synchronous vs. asynchronous loading of <scripts>

Importing via `<script>` is a synchronous action, make sure to use something like `<script async src="awesome.js">` or `<script defer src="moreAwesome.js">` where you can so that page load times are not as affected.

## Consistent code style

Pure JS has many ways to do things, so consistency becomes even more indispensable as it is anyway in programming. But which style to take for the different fundamental parts?

### Semicolons

Let's start with something supposedly easy.

Folks are surprised when they see JS code without semicolons. I was a short while ago.

Semicolons are kind of optional. Some people on the internet present edge cases where things break when you don't use them. Check'em out and decide for yourself.

I play it agile and enjoy the freedom of aesthetic as long as I don't run into problems (works so far). This also has the nice side-effect that it made me desist from copy-pasting code snippets :))

### Function definitions

With today's JS you'll see functions defined in many ways, like for example:

```js
function doStuff() {}

var doStuff = function() {}

var doStuff = () => {}
```

Which one to use? The short answer: any.

The key here again is:

> "Consistency"

So, pick one and follow through.

The long answer, you'll find in books and [awesome blog posts](https://dmitripavlutin.com/6-ways-to-declare-javascript-functions/) ;)

### var, let, const

Pick whichever you like best! I prefer the `let`/`const` approach since it lets you think a bit more about your application architecture and gives you additional type safety. Even if you [scope as mentioned below](#Scopes), choosing your types gives you additional type safety inside your scoped modules.

### Abstractions

Abstractions get the most out for readability and structure inside your code!

#### abstracting JavaScript

In contrast to yummmii real life vanilla ice, pure JS is sometimes ugly and yukki...

```js
setInterval(function () {
  hunt()
}, 2000)
```

Does this look like human readable code? If you need to set lots of timeouts in one of your modules, people will hate you for this type of code. A little abstraction would be:

```js
// in a module like wait.js
function wait(milisecs, callback) {
  setInterval(function () {
    callback()
  }, 2000)
}
// then you can execute it like this:
wait(2000, hunt)
```

All you will get now is love and praise. Isn't it so much nicer? 😋🍨

#### abstracting Your thoughts

Clearly, our mental models sometimes result in heavy script files. Making things work sometimes requires too much mental energy and time.

If your project is to succeed, refactoring code into more modular and readable entities like objects, data structures and fucntions is indispensable. With time, if you like, it's also imaginable to go more object-oriented as your codebase grows. A bit more on that later.

#### abstracting APIs

A common case in the web is making lots of 3rd party API requests, it's not unusual to abstract them away too if you don't want ugly stuff polluting your Vanilla! Let's say you'd like to communicate with this popular Maps API:

```js
// e.g. in your lib/ directory inside a GoogleMapsAPI.js
const GruggleMapsAPI = {
  url: 'https://api.gruggle.com/maps/v1/',

  handleError(response) {
      return response.ok ? response : Promise.reject(response.statusText);
  },

  get(endpoint) {
      return window.fetch(this.url + endpoint, {
          method: 'GET',
          headers: new Headers({
              'Accept': 'application/json'
          })
      })
      .then(this.handleError)
      .catch( error => { throw new Error(error) });
  }
}

// then you can call it like this
GruggleMapsAPI.get('places?type=ice-cream&location=localhost')
```

🍨🍨🍨

#### abstracting config files and data stores

Communicating with config files or data stores is also best performed via an abstraction since you want to make these things easily replaceable and manageable in one place.

As [mentioned before](#A-script-per-view-or-per-functionality), a good place for your abstractions is the `lib/` directory.

### Classes

### Callbacks

If you are rather new to programming or come from a language where callbacks are not that popular (Java?), you'd need to wrapt your head around this first.

### Async

Killed the TMF project story.

## Scopes

One of the first things you should understand well are scopes. This is the actual deeper level structure that will make your code less coupled and more modular.

### variables & functions

### this

## Window

## Events

### .stopPropagation()

### .preventDefault()

## Persisting State

Killed the rs.me project story

## Documentation

I'm not a fan of excessively documenting projects you don't know will take off or looked back at. If you can't think of an audience at all to read your documentation, it's wasted time. Should your project indeed take off, you could still go through it and add necessary docs. It will hurt if you need to document an existing codebase, but in the longterm this strategy will save you time. In this case, just document the parts that the code is not able to explain.

Possible audience:

* the future You
* other developers joining your project

* Inline documentation
* External docs, use the headers of this post to make decisions about how you structure your project and code: new developers will be grateful, your future you will be grateful too.

## OOP

## Testing and Test Driven Development with client-side Vanilla JavaScript

Honestly, it seems like testing and Test Driven Development (TDD) are still second-class citizen in the frontend eco system and especially purely client-side JS applications.

Testing without a build tool is kind of a hack but sometimes, depending on your experience with build tools and backends, it's the easiest way to get the testing journey started. And [arguably](https://medium.com/javascript-scene/tdd-changed-my-life-5af0ce099f80), it's what will make your life most fabolously in the longterm.

## Next steps

Once you've made your first steps with your JS project, it grows in size, and you've ate a good bunch of vanilla ice, you can start branching out and wrap your head around stuff that will make you move faster and even more structured:

### Build Tools

gulp & Co. for

* minifying
* automating
* stitching together

etc.

### Testing and TDD

Just get into it ASAP (a note to my lazy ass) :D

### Backends and servers

(if you need data or throughput heavy functionality)

### Frameworks

(if your use case **really** requires it)
