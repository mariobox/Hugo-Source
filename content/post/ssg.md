+++

date = "2015-04-03"

Categories = []

Tags = ["tech"]

Description = ""

title = "Understanding Static Site Generators"
url = "/ssg"
+++



When I started building websites from scratch using plain HTML and CSS one of the hardest concepts for me to grasp was how a static site generator (SSG) worked. 

<mark>When you use a SSG, the HTML/CSS site is the end product. To get there, you need two other components: a) the source files, and b) the SSG itself</mark>.

The source files are the raw material, so to speak, and the SSG is the machine that processes it. Once the static site generator performs its magic, a website made entirely out of HTML, CSS and Javascript is created.

In summary, you can't just deploy the source files and expect the website to render in your browser. You have to run them through the SSG first.

There are [hundreds](http://www.staticsitegenerators.net) of SSGs to choose from. Depending on the static site generator you choose, you may need to download other programs (or dependencies), like Python or Ruby, that are necessary for the SSG to work. 

Now, back to the source files. There are two kinds of source files: content files and templates. The content files are your blog posts and pages, which can be written in [Markdown](http://daringfireball.net/projects/markdown/). The templates determine the way your content is displayed, and are written in a combination of HTML and the programming language your SSG is written on. 

Templates are great because they enable the SSG to automatically update all common elements of your site (headers, footers and menus), generate a post list, and add any new post to that list.

Once you run the SSG, it places the static site's files in a special folder. Depending on the SSG you are using, this special folder may be called /_site or /public or something else.

Additionally, you can command your SSG to "serve" the site in your local environment (that would be your computer or laptop). To see the result, you need to open your browser and type "localhost:xxxx", where "xxxx" is a four digit number determined by the SSG you are using.

Everything we've talked about so far takes place in your computer or laptop. After that, you need to deploy your site to the web by uploading your static files to a web host like Amazon, Dropbox, Github Pages or other (each of them will give you detailed instructions on how to do it). 

If you are deep into digital self-reliance, you may choose to deploy your site to a VPS (virtual private server). You will first need to install the SSG (plus the programs that enable it) on your VPS. You can then upload the source files, run the SSG, and if you've done everything right your newly created static site should then be live on the web. 

In order to use a SSG you will need to learn, at a bare minimum, the basics of HTML and CSS, a few key Linux-style commands, how to write in Markdown, and have access to a Linux-style terminal emulator.

For this site, I am currently using a SSG called [Hugo](http://www.gohugo.io). It is lightning fast and doesn't require you to download any program other than the Hugo executable. Since I'm working in a Windows box, I use a terminal emulator called [Git Bash](https://msysgit.github.io/). I am deploying the resulting static files in [Github Pages](https://pages.github.com/) using [Git](http://git-scm.com/) for version control and to push (upload) my site to Github Page's server.

**Update:** Read [this article](http://davidwalsh.name/introduction-static-site-generators) for a more comprehensive explanation of how static site generators work.