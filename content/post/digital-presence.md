+++

date = "2015-02-19"

Categories = []

Tags = ["tech"]

Description = ""

title = "The Evolution Of My Digital Presence"
slug = "digital-presence"
+++



I've always been fascinated by the Internet. The idea of having a publishing platform capable of instantly reaching anybody in the world, with no gatekeepers, for free, is still mind boggling to me. Today, of course, everybody has a digital presence, although for most people that means a profile in one or more of the ubiquitous social networks that have taken the Internet by storm. 

When I talk about a having a digital presence, though, I'm not talking about being a tenant in Zuck's massive apartment complex, but rather of building and owning our own digital home: a website that we can deploy using our own domain, custom-designed and tweaked to our liking. 

### The Early Days ###

I've had a digital presence through self-deployed websites (mainly as a hobby) since the early 2000's. I started off by learning some basic HTML tags and hastily coding a website that I used to publish notes-to-self about search engine optimization, a topic I was deeply interested in back then. Then, Web 2.0 came along.

### The Wordpress Days ###
Web 2.0 brought us content management systems (CMS) like Wordpress, with their arsenal of plug-ins, customization options and interactive features. I was curious, so around 2008 I created a self-hosted Wordpress blog where I posted short musings about branding.

It didn't take me long to figure out that Wordpress was overkill for what I really needed: a simple personal blog with no bells and whistles. That's when I discovered [Posterous](http://en.wikipedia.org/wiki/Posterous). Good things don't last forever, though, and a short time later Posterous sold out to Twitter and closed down. I had to take my posts and move back to Wordpress, learning a valuable lesson in the process: never host your website in somebody else's platform.

By that time, however, Wordpress had lost its luster. Its notorious security vulnerabilities meant that I was spending less time writing, and more time weeding out blog comment spam and upgrading to newer versions of the software. Not fun. The straw that broke the camel's back was when someone hacked into my account and started sending mass email spam. I immediately deleted my blog and removed the WP installation from my hosting account.

### Back To The Future: Static Sites Make a Comeback ###

A few months after I obliterated my Wordpress site, I ran into a web design tutorial written by [Ev Bogue](http://www.evbogue.com) that re-acquainted me with the basics of creating web pages, and introduced me to the newer, much simpler iterations of HTML and CSS: HTML5 and CSS3. I got excited and decided to create a website from scratch, like in the early days. I diligently followed the instructions in the tutorial, tweaked a bit the basic style sheet and framework that Ev suggested, and a few days later my new plain vanilla HTML personal site was up.

While it felt great to finally have a site I could control, the problems were obvious: a hand-coded HTML site with no programming involved requires that you create and update each page individually. If you ever want to change, say, the footer or the navigation menu, you have to do it in every single page. If your site has only three or four pages it's not such a big deal, but if you start adding posts and your site grows it can become a real issue. There had to be a better way, and that way is to use a [static site generator](http://www.mattweldon.com/static-websites-have-made-a-comeback/).

### Blogging Like A Hacker: Static Site Generators ###

A [static site generator](../ssg/) is basically a program that takes your content, merges it with predefined templates and style sheets, and generates a site made of just HTML files. Depending on how you configure it, the program can create a blog post list for you, add new posts to that list, and update all your pages automatically when you make changes to the common elements of the site (navigation menu, footer, or sidebar). 

While using a static site generator is extremely easy, setting one up can be a royal pain for non-programmers like me. I definitely wanted to go this route, though, so I focused on acquiring the skills and tools to make it happen. The process took some time, some sweat equity, quite a bit of reading and plenty of trial and error, but in the end I succeded. 

The first static site generator I used was [Jekyll](http://www.jekyllrb.com). After a few months, though, I started to find Jekyll somehow limiting (it's a fairly old SSG), so I gave [Hugo](http://gohugo.io) a try and have been using it ever since. I am extremely happy with Hugo: it is fast, intuitive, and just needs one executable file to run (no complicated dependencies).

### The Tools of the Trade ###

In order to run my site using a static site generator I had to learn a few things: 

- [Markdown](http://daringfireball.net/projects/markdown/) to write blog posts and content in general (easy); 
- [HTML and CSS](http://www.htmlandcssbook.com/) to tweak the look and feel of the site (HTML is fairly easy; CSS is a little harder); 
- [Git](http://git-scm.com/book/en/v2) to record changes to the site and communicate with my web hosting server (hard to wrap your head around the concept, but not that difficult once you "get it"); and 
- [Linux-style command line essentials](http://cli.learncodethehardway.org/bash_cheat_sheet.pdf) to install the required software and to move quickly around my hard drive folders (easy). 

Aside from that, I had to download the following programs: 

- [Git for Windows](http://git-scm.com/download/win) to version control my site and access a command line emmulator called Git Bash; and
- The [Hugo](http://gohugo.io) executable.

Finally, I opened an account with [Github](http://www.github.com) to create the [site's remote repository](https://github.com/mariobox/mariobox.github.io) where I version-control the site's source files, and another repository to version and host the site's public files (those that get served to the web by Github pages to render the site in the browser).

I'm extremely happy with this set-up, and for the time being it is all I need: a simple way to generate, update and deploy a minimalistic personal website at $0 cost. 

