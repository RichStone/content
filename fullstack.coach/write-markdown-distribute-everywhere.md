# The Pefect Set Up to Write your Content in Markdown and CrossPost it to Webflow, dev.to, GitHub, Medium & codementor

This is Your ultimate guide that proposes a solution to write your blog in
markdown and to cross post it to different platforms. There are tons of tips on
how to set up your IWE (Integrated Writer's Environment) and even a few goodies
on marketing as well as on content creation.

It will be of special interest to you if you use webflow to host your blog. But
you will also find big interesting bites if you have a developer or a technical
blog which come with their own pecularities and fun parts. Or maybe you'd like
to open source your blog too?

By the way, I just always wanted to write that something's an "Ultimate Guide",
but actually it's just a bunch of paragraphs. It will be probably an eternal
WIP, and if you are a happy person, i.e. you are reading this on its original
place of spawnment ([fullstack.coach]()) or on GitHub(YOU NERD!) or on dev.to,
then you will always have the most up to date version of it. Congrats!

> In case you start to wonder now: This article is published on all the
> mentioned platforms with as much automation as possible. The original article
> was published on [fullstack.coach]() and then a few days later, after Google
> has done its dirty indexing stuff, on all the other platforms including some
> best practices and canonical URLs. Here you will find out how, in fullest of
> detail!

## Why cross post

If you are in the beginning with your blog, writing can feel lonely. Especially
if you took the hard route and decided to self-host your blog, as opposed to
using a blogging platform like dev.to or Medium, you will lack essential
engagement and feedback which are crucial to nurture your writing and
motivation. I'd like to propose to go out there and make your content as visible
as possible on different platforms.

But how do you keep your posts **consistent on the different platforms**? What
if you have badass blog post that you want to extend or update over time? What
if you want to make your blog open source so that others can contribute to your
work? How do you keep SEO happy? And probably the most important question, how
do you keep your writing in the beloved markdown??

## Enter CrossPost 🔮

CrossPost is a tool that I wrote on some occasional free time slots. Like a
magic ball, it's intended to solve all the issues described above. At the
moment, it has great capabilities to let you write markdown in webflow,
automatically publish your articles on webflow and on dev.to.

Medium and codementor don't have public APIs for publishing articles but I will
outline how to make your life easier if you decide to go the extra mile to
publish there as well. In the end, you can't be sure where your best audience
will be, unless you try it out.

I am open to integrating new platforms with CrossPost or describing them here in
more depth, feel free to suggest anything or fire up a pull request!

## Perequisites

Let's talk some serious stuff first, so that we have a common standpoint when we
speak about systematic cross-posting.

### content consistency

Unless you are a daily news agency, you'll probably want to write so called
pillar content. That is to say, content which stays relevant over longer periods
of time. This type of content, your guides, tutorials and evergreen stories
sometimes need updating too.

That's very painful if you always have to do it manually on all platforms. Those
magic platforms that offer a public API are the good guys who give you the
possibility to automate your content updates.

### canonical URLs

Google & Co. do not like when content is duplicated at different platforms and
hosts. A way to tell Google the original source of the content, the canonical
URL. You set it once, e.g. in the head of the HTML page where your duplicate
content lives and everyone's happy:

```html
<link rel="canonical" href="https://fullstack.coach/" />
```

But I guess Google will be able to [explain it
best](https://support.google.com/webmasters/answer/139066?hl=en&ref_topic=6080547).

### self-hosting a blog

With self-hosting I don't mean you need to deploy your blog on a Linux server. I
mean owning your content more than you would do at dev.to and especially Medium.

You own your content more, whenever you use a platform that allows you to
provide additional content in other formats that could interest your readers and
if you can place a newsletter subscription somewhere.

Ultimately, if you "own" your content space at least for a bit, you'll be able
to turn on some ads in case you become a traffic magnet at some point (although
I wouldn't go with anything else than a trusted platform: [carbon
ads](https://www.carbonads.net/) especially with a developer blog).

You might find dev.to, Medium and codementor handy now but you won't be able to
do any of the above with them later.

I consider platforms like Wordpress already self-hosted, because you own it
enough. I can't cope with the plugin environment of Wordpress which is also the
reason why I actively advise for a [developer-friendly alternative LINK TO BLOG
POST OF THE GUYS]() that I use myself: Webflow ([affiliate 🤩 link]()).

> Congratulations 🎉We've learned a ton about what I think I understand about
> various blog and marketing topics I probably heard about somewhere, so now
> it's definitely time to stop theorizing and get right to the dirty hands-work.

## IWE - Integrated Writer Environment

Everything starts with your work place, or write place in this case. I'd suggest
the following perequisites:

1. distraction-free as possible
1. help with your grammar and style
1. markdown-friendly
1. format-friendly

Writing directly in Grammarly will probably make you the Hemingway of developer
blogs, but in fact it won't. It's super destructive, if the all-knowing and
all-mighty Grammarly is throwing you something in the face after every 3 words
that you write.

It's not a secret that especially the first draft should be written in some kind
of a flow that reflects your own thoughts and style. That's why editor routine
looks like this:

1. write the first draft in VSCode
1. full proof-read and edit not earlier as the next day
1. check your writing with Grammarly

Checking your spelling and grammar with Grammarly can be tricky, especially if
you are writing in rich text formats since copy/pasting ~~can~~ will mess up
your format.

Grammarly seems to work fine with markdown, though. And there is even a plugin
for VSCode, so that you don't have to leave your editor ever.

You will also install the markdownlint plugin, so that you are kept up to date
about any issues you introduce by chaotically typing things.

A super cool feature of blogging in VSCode with markdownlint are links and
images. I would hate to interrupt... (Wow that's scary, as I wrote the word
"interrupt" my wife called to ask me about whether I've bought some corn 🌽)
...interrupt the writing flow to search for some links or to upload some images
into the cloud. You can just write your markdown like this in markdown:

```markdown
Never know where that damn ([affiliate 🤩 link]() is,
so, I just procrastinate with it, until the final edit.

Sometimes, I also don't like adding pictures on the fly,
especially if I have to upload them first, so,
in all agility, I do this:

IMAGE TITLE - markdownlint does not like this:
![]()
```

So that in the end it looks something like this:

MARKDOWNLINT VALIDATION.png
![]()

This is impossible to miss on your final edit, no matter how late or early it is
that I'm writing this stuff (and yeah, I missed lots of them). It's a fail-safe
system :troll: (even better: For the next version of CrossPost, I plan an
automation where you will only need to add the local path to VSCode. WIN-WIN.)

Finally, consider installing the Rewrap plugin. It will help you wrap your
writing at 80 characters to keep your markdown smoothly pressed together into a
nicely readable chunk of bytes. It's maybe not the most friendly solution, but
it's what I have at the moment for that.

> Since you are all set up with your markdown and IWE now, let's bash your
content out to the different spaces and places 🚀

## GitHub

Especially if you are a developer, GitHub might be a very interesting platform
for your content. I use GitHub for various reasons:

1. it makes collaboration on content potentially easier
1. it lets me open source my content to share the authorship with others
1. it lets me version control my content
1. it supports markdown

Make sure you don't have your content in the master branch of your repository
since these are indexed by Google and there is no technical possibility, that
I'm aware of, to set a canonical URL in GitHub for the master repo.

> How I do it: I wrote the post in a separate branch and went through the
> well-known developer process:

```bash
~ git add .
~ git commit -m"Add awesome post"
~ git push
```

I have a master [GitHub repository]() where I store all my published content in
the `content` branch. As mentioned, you shouldn't have it in the `master`
branch, otherwise you risk to get voted down by Google & Co. because of
duplicate content. Usually, to write a new post, I'll branch out from `content`
and work on the draft until it's finished.

## .github.io

Maybe you'd like to host your blog completely on `your-user.github.io`? Since
there are many different approaches and I don't host on .github.io at the moment
myself there is no concrete CrossPost automation for now. But let me know if
you'd be interested in something like this and I will see if I can build a
solution there :)

> How I do it: I don't use .github.io for hosting yet...

## Webflow

When it comes to a full stack developer portfolio or blog, my take is:

1. Don't fiddle too much with your portfolio - Your resources are better spent
   on web applications!
1. It has to look well-designed - By default!
1. It has to be low maintenance - And still fully controllable!

This is what I personally get from webflow. While building my portfolio/blog
page, it somehow turned into [fullstack.coach](https://fullstack.coach), but no
worries I'll set up a portfolio sample soon to give you an example.

I'll post more on this in my coming portfolio guide, keep tuned! 📻 If you like
the idea of webflow already, make sure to register via my link and let me know
if you did so (You'll be honored with big kudos :))).

> How I did it for this article: I wrote the article in markdown and sent it to
> webflow via CrossPost

Anyway, webflow does not support markdown by default. That's a major issue if
you are a badass developer writing about code using markdown code. There are
workarounds and hacks to make it work but they all come with major drawbacks.

**This was one of the reasons for me to create [CrossPost]()**.

The basic idea of CrossPost is to have a CLI tool and send your articles to your
webflow blog with one command:

```bash
# go to your article's location
~ cd content/
# get your content out there!
~ crosspost article your-amazing-writing.md --to webflow
```

If you want to update your article on all platforms, you can just do:

```bash
~ crosspost article your-amazing-writing.md
```

All you need to do is to configure CrossPost once.

```bash
~ crosspost configure --help
```

And of course to install it on your computer:

```bash
# You will need NPM installed on your computer.
~ npm install crosspost -g
```

There are things to keep in mind when using CrossPost, so please check out the
docs before you dive into it or ping me with any doubts :)

## dev.to

There is no place like dev.to for software developer and technical bloggers!

Now, I could just copy-paste my beautiful markdown to dev.to and it would work.
But that's very burdensome, especially considering that in VSCode I am so close
to the terminal.

But even more importantly, **what happens if you want to update your content**?
I don't know about you, but I want to write long-living content, guides and
tutorials. If they get outdated or corrected by your readers and reviewers,
you'd probably want to make the changes as quickly as possible. For some
articles, this can become a frequent thing to do. And now copy-pasta becomes
really boring and untasty.

Your solution, again:

```bash
# go to your article's location
~ cd content/
# get your content out there!
~ crosspost article your-amazing-writing.md --to devto
```

And again, to update your existing article on all platforms:

```bash
~ crosspost article your-amazing-writing.md
```

Again, read up on the [CrossPost docs]() a bit before installing CrossPost and
wildly using it ;)

## Medium

I wouldn't say I despise Medium. But so many developers gave their lives to
Medium. And still, in 2020, there is no syntax highlighting possible for code?
Really?

And that's just the bird crap on the tip of the iceberg of Medium's crimes. 🐧

But at they do allow for a canonical URL which did positively surprise me,
really. And they have users, tons of readers, potentially even people that might
find usefulness or joy in your content.

So, if you still want to be seen there, we'll need to add some additional steps
to our ignorance and do some manual cross posting work:

> How I did it for this post: I struggled, as any other developer does too...

...first, you'll need to import your post via [Medium's import function]()

IMPORT YOUR ARTICLE TO MEDIUM.png
[]()

...next, you will add the canonical URL to your post.

ADD CANONICAL URL MEDIUM.png
[]()

...and last, you might want to make your code syntax highlighted with something
like this [nice tool](). (Which I obviously skipped, because that's too big of a
struggle still.)

## codementor

Codementor - last and probably **least**, since the codementor blogging space
probably has not won any popularity awards yet. Please, correct me if I'm wrong.

It has a nice markdown editor, but I don't have the feeling of big blogging
activity on the platform yet. In any case, an additional pair of eyes at your
content won't hurt, and you will find that you are in the right place if you
have some fitting coaching, mentoring or problem-solving articles going down!
With the right content, a codementor article will go kind of viral too.

As of now, codementor's API doesn't give a damn about POSTing your article's
there in an automated way, so that you will actually (even at this developer
focused place) need to take the mouse in your hands and click around (sad and
boring, I know).

> How I did it for this post: I went the copy pasta route

Codementor has an import feature, which will set the canonical URL automatically
but might mess up your format.

Having written your blog in markdown already, the easiest way to publish it on
codementor is to copy and then to paste it into codementor's markdown editor.
The only issue is that you'd need to go the extra mile and hit up the codementor
support, so that they add the canonical URL manually, which can take a few
days...

## Your Custom Platform

Let me know if you'd like a platform of yours integrated with the IWE or with
CrossPost and I can look into it!

And now go write that content!
