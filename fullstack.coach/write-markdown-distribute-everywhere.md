# Write your Content in Markdown smoothly and CrossPost to Webflow, dev.to, GitHub, Medium and codementor

This guide proposes a solution to write your blog in markdown and to cross post it to different
platforms. You could also use it to make your blog open source. It will be of special interest to
you if you use webflow to host your blog. But you will also find interesting bites if you have a
developer blog which comes with its own pecularities.

## Why cross post

If you are in the beginning with your blog, writing can feel lonely. Especially if you took the hard
route and decided to self-host your blog, as opposed to using a blogging platform like dev.to or
Medium, you will lack essential engagement and feedback which are crucial to nurture your writing
and motivation. I'd like to propose to go out there and make your content as visible as possible on
different platforms.

But how do you keep your posts **consistent on the different platforms**? What if you have badass
blog post that you want to extend or update over time? What if you want to make your blog open
source so that others can contribute to your work? How do you keep SEO happy? And probably the most
important question, how do you keep your writing in the beloved markdown??

## Enter CrossPost 🔮

CrossPost is a tool that I wrote on some occasional free time slots. Like a magic ball, it's
intended to solve all the issues described above. At the moment, it has great capabilities to let
you write markdown in webflow, automatically publish your articles on webflow and on dev.to.

Medium and codementor don't have public APIs for publishing articles but I will outline how to make
your life easier if you decide to go the extra mile to publish there as well. In the end, you can't
be sure where your best audience will be, unless you try it out.

I am open to integrating new platforms with CrossPost or describing them here in more depth, feel
free to suggest anything or fire up a pull request!

## Perequisites

Here some crucial stuff we will need a common understanding about when we talk systematic cross
posting.

### content consistency

- particularly important as soon as you start writing pillar content

### canonical URLs

- Google does not like duplicate content

### self-hosting a blog

With self-hosting I don't mean you need to deploy your blog on a Linux server. I mean owning your
content more than you would do at dev.to and especially Medium.

You own your content more, whenever you use a platform that allows you to provide additional content
in other formats that could interest your readers and if you can place a newsletter subscription
somewhere.

Ultimately, if you "own" your content, you'll be able to turn on some ads, if you become a traffic
magnet at some point (although I wouldn't go with anything else than [carbon
ads](https://www.carbonads.net/) especially with a developer blog).

You might find dev.to, Medium and codementor handy but you won't be able to do any of the above with
them.

I consider platforms like Wordpress already self-hosted, because you own it enough. Although, I
despise the plugin environment of Wordpress which is also the reason why I actively advise for a
developer-friendly alternative that I use myself: Webflow ([affiliate 🤩 link]())

## IWE - Integrated Writer Environment

Everything starts with your work place, or write place in this case. I'd suggest the following
perequisites:

1. distraction-free as possible
1. help with your grammar and style
1. markdown-friendly
1. format-friendly

Writing directly in Grammarly will probably make you the Hemingway of developer blogs, but in fact
it won't. It's super destructive, if the all-knowing and all-mighty Grammarly is throwing you
something in the face after every 3 words that you write.

It's not a secret that especially the first draft should be written in some kind of a flow that
reflects your own thoughts and style. That's why editor routine looks like this:

1. write the first draft in VSCode
1. full proof-read and edit not earlier as the next day
1. check your writing with Grammarly

Checking your spelling and grammar with Grammarly can be tricky, especially if you are writing in
rich text formats since copy/pasting ~~can~~ will mess up your format.

Grammarly seems to work fine with markdown, though. And there is even a plugin for VSCode, so that
you don't have to leave your editor ever.

You will also install the markdownlint plugin, so that you are kept up to date about any issues you
introduce by chaotically typing things. Also, you'll never miss any links that you "will definitely add later" heavily underlined and ready to be populated.

Finally, consider installing the Rewrap plugin. It will help you wrap your writing at 80 characters to keep your markdown smoothly pressed together into a nicely readable chunk of bytes.

## GitHub

Especially if you are a developer, GitHub might be a very interesting platform for your content. I
use GitHub for various reasons:

1. it lets me version control my content
1. it makes collaboration on blog posts easier
1. it lets me open source my content so that others can help me correct and extend it
1. it supports markdown

Make sure you don't have your content in the master branch of your repository since these are
indexed by Google and there is no possibility to set a canonical URL in GitHub.
