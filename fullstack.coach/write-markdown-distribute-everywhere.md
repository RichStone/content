# How to Write & Cross Post your Markdown Content

This is your _Ultimate Guide_ that proposes a solution to write your blog in markdown and to cross post it to different platforms. Here you will find tips on how to set up your IWE (Integrated Writer's Environment) and even a few goodies on marketing as well as on content creation.

I warn you, this is a monstrous piece of content, so here's the rough outline:

1. Some cross posting, SEO & hosting theory
1. Markdown writing tips (Integrated Writer Environment)
1. Content distribution  
  GitHub  
  Webflow  
  dev.to  
  Medium  
  codementor

By the way, the original title of this post was:

## The Perfect Setup to Write your Software Developer Blog Content in Markdown and CrossPost it to Webflow, dev.to, GitHub, Medium & codementor

However, this one was a bit over the [recommended 60 max. chars](https://www.mheroes.com/that-blog-title-is-too-long-are-you-counting/) for blog titles...

From this longer title, you'll see that this post will be of special interest to you if you use webflow to host your blog.

**And** if you have some sort of a software developer or technical blog content since we go deeply into things like code syntax highlighting proper hosting, and developer-focused content platforms.

**Or** maybe you just ❤️ markdown?

**Or** you'd like to open source your blog on GitHub too?

By the way, I just always wanted to write that something's an _"Ultimate Guide"_, but actually, it's just a bunch of paragraphs. It will be probably an eternal WIP, considering all the platforms and different tastes involved. If you are a happy person, i.e. you are reading this on its original place of spawning ([fullstack.coach](https://fullstack.coach/post/how-to-write-and-cross-post-your-markdown-content)) or in the post's very core root on [Github](https://github.com/RichStone/content/blob/content/fullstack.coach/write-markdown-distribute-everywhere.md) (YOU NERD!) or on dev.to, then you will always have the most up to date version of it. Congrats!🎉

> In case you start to wonder now: This article is published on all the mentioned platforms with as much automation as currently possible. The original article was published on [fullstack.coach](https://fullstack.coach/post/how-to-write-and-cross-post-your-markdown-content) and then a few days later, after Google has done its dirty indexing stuff, on all the other platforms including some best practices and canonical URLs. Here you will find out how in fullest of detail!

## Why cross post your content at all

If you are in the beginning with your blog, writing can feel lonely. Especially if you took the hard route and decided to self-host your blog, as opposed to using a blogging platform like dev.to or Medium, you will lack essential engagement and feedback which are crucial to nurturing your writing and motivation. Additionally, potential readers won't ever get to know about the useful things you are talking about :/

This is why I propose to go out there and make your content as visible as possible on different platforms, especially in the beginning.

But how do you keep your posts **consistent on the different platforms**? What if you have a badass blog post that you want to **extend or update over time**? What if you want to make your blog **open source** so that your content becomes a community effort? How do you keep SEO happy? And probably the most important question, how do you keep your **writing in the beloved markdown**??

## Enter CrossPost 🔮

CrossPost is a tool that I wrote on some occasional free time slots. Like a magic ball, it's intended to mystically solve some of the issues above. At the moment, it has great capabilities to let you write markdown in your favorite editor and then (almost) automatically publish your articles on webflow as well as dev.to.

Medium and codementor don't have public APIs for publishing articles but I will outline how to make your life easier if you decide to go the extra mile to publish there too. In the end, you can't be sure where your best audience will be unless you try them all out.

I am open to integrating new platforms with CrossPost or describing them here in more depth, feel free to suggest anything or fire up a pull request!

## Theoretical Prerequisites

Let's talk some serious stuff first so that we have a common standpoint when we speak about systematic cross-posting.

### content consistency

Unless you are a daily news agency, you'll probably want to write so-called pillar content. That is to say, content that stays relevant over long periods. This type of content, your guides and tutorials and evergreen stories, sometimes, needs updates and upgrades!

That's very painful if you always have to do it manually on all platforms. Those magic platforms that offer a public API are the good guys who give you the possibility to automate your content updates.

### canonical URLs

Google & Co. do not like the same content on different platforms and hosts. The canonical URL is one way to tell Google the original source of the content. You set it once, e.g. in the head of the HTML page where your duplicate content lives and everyone's happy:

```html
<link rel="canonical" href="https://fullstack.coach/" />
```

But I guess Google will be able to [explain it in more detail](https://support.google.com/webmasters/answer/139066?hl=en&ref_topic=6080547).

### self-hosting a blog

With self-hosting, I don't mean you need to deploy your blog on a Linux server. I mean owning your content more than you would do at dev.to or Medium.

You own your content more, as soon as you use a platform that allows you to provide additional content in other formats that could interest your readers and if you can place a newsletter subscription somewhere.

Ultimately, if you "own" your content space, at least for a bit, you'll be able to turn on some ads in case you become a traffic magnet at some point (although I wouldn't go with anything else than a trusted platform like [carbonads](https://www.carbonads.net/), especially with a developer blog).

You might find dev.to, Medium and codementor handy now but you won't be able to do any of the above with them later.

In this context, we can consider platforms like WordPress already self-hosted, because you own it enough. I can't cope with the plugin environment of WordPress which is also the reason why I actively advise for a [developer-friendly alternative that I use myself](https://www.alioned.com/post/webflow-for-developers-my-personal-experience-building-our-agency-website-on-webflow): Webflow ([affiliate 🤩 link](https://webflow.com/?rfsn=4246649.252ab0&amp;utm_medium=affiliate)).

> Congratulations 🎉 We've learned a ton about what I think I understand about some blog marketing topics, so now it's time for dirty hands-on work.

## IWE - Integrated Writer Environment

Every piece of art starts with an atelier or workshop. This is how my optimal writer atelier looks like:

1. as distraction-free as possible
1. ... but simultaneously supportive with grammar and style
1. markdown-friendly
1. format-friendly

Writing directly in Grammarly will probably make you the Hemingway of developer blogs, but actually, it won't. I find it very destructive when the all-knowing and all-mighty Grammarly is throwing grammar and orthography errors at me on every third word that I'm bringing to life...

It's not a secret that especially the first draft should be written in some kind of flow that reflects your own thoughts and style. That's why my writing and editing routine looks something like this:

1. write the [shitty first draft](http://www.debbiereberwritingcoach.com/the-art-of-the-shitty-first-draft-why-and-how-to-write-it-2/) in VSCode
  Completely distraction-free
1. full proof-read and edit not earlier as the next day
  Now, turn on the Grammarly plugin inside VSCode
1. Another edit sometime later on the target platform
  You'll have another fresh look at the final format of your writing

Checking your spelling and grammar with Grammarly can be tricky, especially if you are writing in rich text formats since copy/pasting ~~can~~ will mess up your format.

The Grammarly app seems to work fine with copy-pasting markdown. But there is also a plugin for VSCode so that you don't have to leave your editor ever 🤓. You've got to be a bit patient with this plugin sometimes, though. Try it out!

You will also install the markdownlint plugin so that you are always kept up to date about any issues you introduce to your beautiful markdown files by chaotically typing things.

![typing cat gif](https://raw.githubusercontent.com/RichStone/content/0d2fd292c648ab85c7504ab08ba4574cf67d4450/fullstack.coach/images/write-markdown-distribute-everywhere/typing-cat.gif)

A super cool feature of blogging in VSCode with markdownlint are links and images.

I would hate to interrupt... (Wow that's scary, as I wrote the word "interrupt" my wife called to ask me about whether I've bought some corn 🌽) ...interrupt the writing flow to search for some links or to upload some images into the cloud. You can just write your markdown like this in markdown:

```markdown
Never know where that damn ([affiliate 🤩 link]() is,
so, I just procrastinate with it, until the final edit.

Sometimes, I also don't like adding pictures on the fly,
especially if I have to upload them first, so,
in all agility, I do this:

IMAGE TITLE - markdownlint does not appreciate this:
![]()
```

So that in the end, it looks something like this:

![markdownlint validation example](https://github.com/RichStone/content/blob/content/fullstack.coach/images/write-markdown-distribute-everywhere/MARKDOWNLINT%20VALIDATION.png?raw=true)

This is impossible to miss on your final edit, no matter how late or early it is that I'm writing this stuff (and yeah, I missed lots of them in the past). It's a fail-safe system :troll: (even better: For the next version of CrossPost, I plan an automation where you will only need to add the local path to VSCode. WIN-WIN.)

Or even better, use some HTML in your markdown, like: `<img alt="I'll add this picture after the 'holidays'🤭">`. If you ever publish your content before the holidays, there will be the classic broken picture image with your alt description.

Take whatever you prefer.

Another thing I like is the 80 character max limit for my writing in markdown but I need the process automated. I tried the VSCode Rewrap plugin, but it created some weird newlines that were displayed in dev.to and webflow in an ugly way. So for now, I'm OK writing everything strung together. VSCode's soft wrap still lets me write and watch the content conveniently.

> Huh, this was a wild IWE ride. Since you are all set up with your markdown and Integrated Writer Environment now, let's bash your content out to the different spaces and places 🚀

## GitHub

Especially if you are a developer, GitHub might be a very interesting platform for your content. I use GitHub for various reasons:

1. it makes collaboration on content potentially easier
1. it lets me open-source my content to share the authorship with others
1. it lets me version control my content
1. it supports markdown

Make sure you don't have your content in the master branch of your repository since these are indexed by Google and there is no technical possibility, that I'm aware of, to set a canonical URL in GitHub for the master repo.

> How I did it for this post: I wrote the post in a separate branch and went through the well-known developer process:

```bash
~ git add .
~ git commit -m"Add awesome post"
~ git push
```

I have a [GitHub repository](https://github.com/RichStone/content) where I store all my published content in the `content` branch. As mentioned, you shouldn't have it in the `master` branch. Otherwise, you risk getting ranked down by Google & Co. because of duplicate content.

By the way, using GitHub for your content, could also be a way to host your pictures (which is always a big issue: How and where do you keep your pictures? IN ONE PLACE... FOREVER!?!?). Just make sure you use the [permalink to the image](https://docs.github.com/en/github/managing-files-in-a-repository/getting-permanent-links-to-files) after you've uploaded it to GitHub! As I understand it, the image links will only break in one case: if, somewhen, you'll decide to get rid of your `content` branch.

## .github.io

Maybe you'd like to host your blog completely on `bloggo.github.io`?

There are many different approaches and I don't host on `.github.io` at the moment myself, so there are no concrete CrossPost automations for now. But let me know if you'd be interested in something like this and I will see if I can build a solution there :)

> How I did it for this post: I don't use .github.io for hosting yet...

## Webflow

When it comes to a full stack developer portfolio or blog, my take is:

1. Don't fiddle too much with your portfolio - Your resources are better spent on real web applications!
1. It has still to look well-designed - By default!
1. It has to be low maintenance - And still fully controllable!

This is what I get from webflow (except, if you don't count the times when I build custom integrations for it 😅).

I'm writing blogs since 2011 and I've used tons of different approaches and platforms already(WordPress, Wix, Jimdo, a public forum, and Jekyll on my own server). Webflow just gets the best parts of all of them for me at this stage of my technical understanding. However, you should not touch it, if you are afraid of learning curves or pricing. For no-budget blogs go with a `.github.io` hosting. For low learning curves go to WordPress (but don't tell afterward that I haven't warned about the off-turn plugin ecosystem!)

There are some more tips in the pipeline on how webflow was useful to my portfolio page, so keep tuned! 📻

If you like the idea of webflow already, make sure to register [via my link](https://webflow.com/?rfsn=4246649.252ab0&amp;utm_medium=affiliate): and let me know if you did so (You'll be honored with big kudos :))). At the very least, being a developer, you should like this slogan:

> "Design and develop at the same time."

## 🚀

> How I did it for this article: I wrote the article in markdown and sent it to webflow via CrossPost

Anyway, webflow does not support markdown by default. That's a major issue if you are a badass developer who uses code to write code about code 💪. There are workarounds and hacks to make it work. I tried some of them and they all came with major drawbacks that made it unusable for me in the end.

**This was one of the reasons for me to create [CrossPost](https://github.com/RichStone/crosspost-markdown)**.

The basic idea of CrossPost is to have a CLI tool to **send and update your markdown content** to your webflow blog (and other platforms) with one command:

```
# go to your article's location
~ cd content/
# send your markdown to webflow
~ crosspost article your-amazing-writing.md --to webflow

your-amazing-writing.md found in your current directory! 👍
✅ webflow API key is present
✅ webflow collection ID is present
✅ webflow Articles URL is configured👍
✅ devto is configured👍
   ____                              ____                  _               
  / ___|  _ __    ___    ___   ___  |  _ \    ___    ___  | |_             
 | |     | '__|  / _ \  / __| / __| | |_) |  / _ \  / __| | __|            
 | |___  | |    | (_) | \__ \ \__ \ |  __/  | (_) | \__ \ | |_   _   _   _ 
  \____| |_|     \___/  |___/ |___/ |_|      \___/  |___/  \__| (_) (_) (_)
                                                                           
...to all configured platforms!🚀
Could not find your-amazing-writing.md.json
Creating your-amazing-writing.md.json...
Your article's individual configurations will now be stored in the your-amazing-writing.md.json ✅
You will need to keep them together for consistency.
Published a new article on webflow! 🎉🎉🎉
```

If you want to update your article on all platforms, you can just do again:

```bash
~ crosspost article your-amazing-writing.md
```

All you need to do is to install CrossPost it on your computer:

```bash
# You will need NPM installed on your computer.
~ npm install crosspost -g
```

And to configure CrossPost once:

```bash
~ crosspost configure --help
```

### Configuration steps & caveats with Webflow

**Before publishing on webflow**, you'll need to set up CrossPost with webflow:

```bash
~ crosspost configure --only webflow
```

It's just a few steps actually if you make use of the [webflow CMS
API](https://developers.webflow.com/#authentication):

1. ✅ Get webflow API key
1. ✅ Get site ID  
  With the API key, you can get your site IDs
1. ✅ Get collection ID of your content CMS collection  
  With your site ID, you can get the collection ID of your blog content
1. ✅ Add the full URL to your webflow articles  
  E.g. the base URL of the [fullstack.coach](https://fullstack.coach) content is `https://fullstack.coach/post`(don't ask why 😅)

After everything went fine, your `crosspost configure` output should look something like this:

```bash
~ crosspost configure

✅ webflow API key is present
✅ webflow collection ID is present
✅ webflow Articles URL is configured👍
✅ devto is configured👍

ℹ️ run `crosspost configure --help` to see all the specific options ℹ️
```

### Add syntax highlighting to webflow

You will need to add something like prism to enable syntax highlighting. This is how I quickly did it:

1. Add a stylesheet your collection's custom head code:

```html
<link href="https://cdn.jsdelivr.net/npm/prismjs@1.20.0/themes/prism.css" rel="stylesheet" />
```

2. Add the prism javascript and autoloader to your end of body collection's custom code:

```html
<script src="https://cdn.jsdelivr.net/npm/prismjs@1.20.0/components/prism-core.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/prismjs@1.20.0/plugins/autoloader/prism-autoloader.min.js"></script>
```

You can have a different theme, by simply checking out the different default themes on jsdeliver.net or configure your own theme over at [prismjs](https://prismjs.com/download.html).

To figure this out, I used the [instructions provided by prism](https://prismjs.com/#basic-usage-cdn).

> All the Prerequisites are now fixed, let's look at what to do after you've successfully run `crosspost article`. Let me know if you get stuck on any of the configuration steps!

---

**After publishing on webflow** for the first time, your articles will be in Staged mode. You will still need to make adjustments like setting your custom fields, images, a post summary, etc. (integrations for that are on the [wishlist in GitHub](https://github.com/RichStone/crosspost-markdown/issues))

When you update your posts, CrossPost will only update your article body and your title (if you changed any of them). If you'd like to have more granular control, we'll need to issue some Pull Requests to CrossPost ;)

Other than that, if you update an existing post, it will be in staged mode first. This way you can still review your changes before publishing them to your live environment (a `--live` tag to publish directly to production is on the wishlist too).

If you click inside the webflow editor of your published blog post text and then the "Save" button, **webflow will mess up the formatting** because it will delete the HTML metadata that we've sent over with CrossPost. This means:

- Don't click inside your webflow blog post editor and then "Save"
  - If you publish with CrossPost, you can't make use of the webflow editor anymore to change your Rich Text blog post content (you still will be able to change other data inside the CMS view, like images, summary, authors, etc.)
  - If you still did it by mistake, just republish from CrossPost, this will update the content with the correct HTML again (e.g. `~ crosspost article test.md`)
  - If you still make changes to your article content inside webflow, CrossPost will overwrite them with the contents of your markdown file on the next publish.
- Once your article is on webflow, you might encounter weird behavior inside the webflow editor.
  - For example, I can't see the ordered list and unordered list items inside the editor, but it displays correctly in the published version. Since you want to keep your article writing outside of webflow anyway, it shouldn't be too big of a deal.
- The integration relies on you keeping to make updates to your articles via CrossPost.

> It's lots of stuff to keep in your head for the aftermath, but actually, it's simple: If you publish content with CrossPost, you don't touch the Rich Text Field inside webflow anymore and do all your future changes to the content via CrossPost. If you still do, it might mess up the format and you'd need to republish with CrossPost again.

### Add additional CSS to your content collection

You may also want to add some extra CSS to your blog posts collection, e.g. to add some extra margins on headings and paragraphs (h1, h2, p tags, etc.). In my experience, the raw HTML headings looked a bit pressed together but adding CSS to a collection is done quickly in webflow so that you can add that premium whitespace that everyone's longing for so hard.

Make sure your changes don't conflict with existing posts (if you have any).

This is how my collection CSS kind of looks like:

```css
<style>

h1, h2, h3, h4, .heading-h1 , .heading-jumbo , .heading-h2, .heading-h3, .heading-h4 {
    overflow-wrap: break-word !important;
    word-wrap: break-word !important;
    -webkit-hyphens: auto !important;
    -ms-hyphens: auto !important;
    -moz-hyphens: auto !important;
    hyphens: auto !important;

    margin-top: 16px !important;
    margin-bottom: 16px !important;
}

code {
    font-size: .8em !important;
}

p, li, ul, ol, pre, blockquote, div {
    margin-bottom: 16px !important;
}

img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
}

</style>
```

Basically, I've just added some margins to the HTML elements. If you have a content-heavy site, you'd be doing this anyway. The word-wrap/hyphen stuff is, I think, webflow-specific: It's so that your layout does not get broken, especially on mobile, with big long heading titles...

I also center images as a default, if you need anything vastly different, you can write HTML in your markdown file, give it a special class and then write the CSS class for it inside webflow. Dev.to will center them for you automatically, though.

> Wow, this was a lot of webflow stuff! The setup is not a pony ride, but after it's done there will be a new milestone in your writing productivity.

## dev.to

There is no place like dev.to for software developers and technical bloggers!

Now, I could just copy-paste my beautiful markdown to dev.to and it would work. But that's very burdensome, especially considering that in VSCode I am so close to the terminal.

But even more importantly, **what happens if you want to update your content**? I don't know about you, but I want to write long-living content, guides, and tutorials. If they get outdated or corrected by your readers and reviewers, you'd probably want to make the changes as quickly as possible. For some articles, this can become a frequent thing to do. And now copy-pasta becomes really annoying, boring, untasty, and even dangerous.

Your solution, again:

```bash
# go to your article's location
~ cd content/
# get your content out there
~ crosspost article your-amazing-writing.md --to devto
# ... lots of cool output ...
CrossPost...
...to dev.to!🚀

Successfully updated your dev.to article.👍
```

And again, to update your existing article on all platforms:

```bash
~ crosspost article your-amazing-writing.md
# ... lots of cool output ...
CrossPost...
...to all configured platforms!🚀

Updated your article 👍
Successfully updated your dev.to article.👍
```

### Configurations and Caveats with dev.to

As of now, with CrossPost your article will be published as a Draft. You will still need to log in and perform some additional configurations, like:

- adding tags
- adding a header image
- switching the article from Draft to Published

After that, CrossPost will update your content on every `~ crosspost article your-writing.md` leaving any other meta information untouched.

Please let me know if you'd like us to add more automated configurations like this inside CrossPost or feel free to issue a Pull Request, so we'd never have to leave the terminal again 😅

> How I did it on dev.to for this post: I already had my article up there for a while and used `~ crosspost article write-markdown-distribute-everywhere.md` to update it together with the webflow article. When I felt good and ready about the webflow article I went up to dev.to and clicked that cool "Publish" button! 💪 Updates are easy, just doing `~ crosspost article write-markdown-distribute-everywhere.md` again and again.

## General CrossPost Caveats & Fun Facts

- CrossPost will overwrite everything if you should ever add anything manually inside dev.to's or webflow's editor.
- When you publish with CrossPost, an additional configuration file gets created.
  - You'll need to store this file together with your posts to keep using CrossPost. Consistency can only be achieved if CrossPost knows about the article IDs on different platforms.
- **Your post has to start with an h1 markdown title ('#') in the very first line of your .md file**. 
  - It's a useful markdownlint convention and CrossPost also relies on it to set the title of the posts correctly.
  - The titles from the first line of your file will be automatically before sending them to webflow or dev.to. 
  - Those titles will be set via the API so that you don't have the title duplicated as an h1 element inside your article's body!
- Your markdown files will be converted with [showdown](https://github.com/showdownjs/showdown) to [GitHub flavored markdown](https://docs.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax) before pushing up to space 🚀.

For more technical details on how CrossPost works, current issues and planned features, check out the [GitHub repo](https://github.com/RichStone/crosspost-markdown) or ping me with any doubts :)

## Medium

I wouldn't say I despise Medium. But so many developers gave their lives to Medium. And still, in 2020, there is no syntax highlighting possible for code? Really?

And that's just the bird crap on the tip of the iceberg of Medium's crimes. 🐧

But they do allow for a canonical URL and article imports which did positively surprise me, really. And they have users, tons of readers, potentially even people that might find usefulness or joy in your content.

So, if you still want to be seen there, we'll need to add some additional steps to our ignorance and do some manual cross posting work:

...first, you'll need to import your post via [Medium's import function](https://medium.com/p/import)...

...next, go through your article and watch out for formatting issues...

...and lastly, you might want to make your code syntax highlighted with something like this [tool](https://medium.com/@Maluen0/how-to-add-code-highlighting-in-medium-articles-without-leaving-the-editor-8f24f5a88d28). (Which I obviously haven't tried yet...)

Medium will set the [canonical link for imported articles automatically](https://help.medium.com/hc/en-us/articles/360033930293-Set-a-canonical-link).

> How I did it for this post: I struggled, as any other developer does too… First it looked good and I just saw some redundant newlines. But then all the code blocks were messed up completely, some codeblocks were missing, some lists (when they contained links) were missing too. Wow.

## codementor

Codementor - last and probably **least**, since the codementor blogging space has not won any popularity awards yet. Please, correct me if I'm wrong.

It has a nice markdown editor, but I don't have the feeling of big blogging activity on the platform yet. In any case, an additional pair of eyes at your content won't hurt, and you will find that you are in the right place if you have some fitting coaching, mentoring, or problem-solving articles going down! With the right content, a codementor article will go kind of viral too!

As of now, codementor's API doesn't give a damn about POSTing your article's there in an automated way so that you will actually (even at this developer-focused place) need to take the mouse in your hands and click around (sad and boring, I know).

I've had an email chat with the nice codementor in-charge folks, and these are your options:

### codementor option 1

Codementor has an [import feature](https://www.codementor.io/posts/import), which will set the canonical URL automatically but could theoretically mess up your format.

### codementor option 2

Having written your blog in markdown already, you could copy it and then paste it into codementor's markdown editor. The only issue is that you'd need to go the extra mile and hit up the codementor support, so that they add the canonical URL manually, which is not only weird but can also take a few days... (Thus, if you have more than 1 article, they recommend sending them over all your articles at once so that their workload and your waiting time goes down ;)

> How I did it for this post: I went the import route, and the content looks fine. Like Medium, it looks at first as if there were redundant newlines, but the endresult seems actually to be perfect out-of-the-box. And guess what, code syntax is included! Good work codementors!

## Your Custom Platform

Are you using WordPress, strapi, GitLab, or other platforms with APIs for your content?

Let me know if you'd like them integrated with the IWE or with CrossPost and I can look into it!

## Resources

- [CrossPost repo](https://github.com/RichStone/crosspost-markdown)
- [CrossPost wishlist](https://github.com/RichStone/crosspost-markdown/issues)

And now go let your content be seen! 🚀🚀🚀

---

Images Attribution:

- _Header Illustration by [Freepik Stories](https://stories.freepik.com/design)_
- _Typing cat gif by [tenor](https://tenor.com/view/typing-laptop-cat-gif-5822667)_
