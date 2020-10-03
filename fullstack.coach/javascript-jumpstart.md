# Writing JavaScript Code & Structuring Your Project When You Don't Have Much Time

__This is an open-source Work In Progress, living [on GitHub]() and cross-posted with [CrossPost](), any valuable feedback will be incorporated in the next 3 weeks. Thank you for reading and supporting! 🙏 Read the original article over at [fullstack.coach]()__

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

I'd assert, a `/js` folder comes with every random web boilerplate or template you've chosen (unless you are using [the motherfucking website framework](https://motherfuckingwebsite.com/) maybe).

### Basic structure

## Consistent ice cream style

Pure JS has many ways to do things, so consistency becomes even more indispensable as it is anyway in programming. But which style to take for the different fundamental parts?

### Function definitions

With today's JS you'll see functions defined in many ways:

The key here is:

> "Consistency"

Which one to choose? Pick one and follow through it.

### Abstractions

### Classes

## Scopes

One of the first things you should understand well are scopes. This is the actual deeper level structure that will make your code less coupled and more modular.

### variables & functions

### this

## Window

## Events

### .stopPropagation()

### .preventDefault()

## Persisting State

## OOP

## Testing and Test Driven Development with client-side Vanilla JavaScript

Honestly, it seems like testing and Test Driven Development (TDD) are still second-class citizen in the frontend eco system and especially purely client-side JS applications.

Testing without a build tool is kind of a hack but sometimes, depending on your experience with build tools and backends, it's the easiest way to get the testing journey started. And [arguably](https://medium.com/javascript-scene/tdd-changed-my-life-5af0ce099f80), it's what will make your life most fabolously in the longterm.

## Next steps

Once you've made your first steps with your JS project, it grows in size, and you've ate a good bunch of vanilla ice, you can start branching out and wrap your head around stuff that will make you move faster and even more structured:

* gulp & Co. for minifying, stitching together etc.
* testing
* node backends (if needed)
* look at frameworks (if your use case requires it)
