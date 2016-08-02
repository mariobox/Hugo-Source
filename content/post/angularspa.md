+++

date = "2016-08-02"

Categories = []

Tags = ["tech"]

Description = ""

title = "Building a SPA with Angular.js"

slug = ""

draft = "false"

+++


A few weeks ago I came across the concept of SPA, or [Single Page Application](https://en.wikipedia.org/wiki/Single-page_application), and learned that they can be created with [Angular.js](https://angularjs.org/), a JavaScript library supported by Google.

Most definitions of SPA you can find online are very technical and full of jargon, so perhaps the best way a newbie web developer like me can understand it is with an example:

Suppose you have an index.html web page with three different sections: the header (where the navigation menu is), the content area, and the footer.  The header and the footer remain the same all over the website, so the only thing that really changes when you go from the index page to, say, the about.html page is the actual page content. What a SPA does is to allow the header and the footer to stay right where they are, while it calls only the actual content of the about.html page and sticks it right between the header and footer. No new page is loaded (that's where the Single Page part of Single Page Application comes from).

The switch between the content of your index.html and your about.html page is done on the fly by the browser of the person viewing your site, by following the Angular.js directives embedded in the page code.

I wanted to test building a SPA by creating a barebones, basic brochure site, using Angular.js to generate four page views: Home, About, Contact and Resume.

I found an [excellent tutorial](https://www.airpair.com/angularjs/building-angularjs-app-tutorial) online. After reading it carefully several times I started by creating the index template, which contains the Angular directives to make the site work, and which acts as a template for the whole site. I then created bare-bones html files for the other three pages of the site: About, Contact and Resume (nothing fancy, just a couple of <code>\<h1></code> tags and a paragraph). 
I then tweaked the main.js file to refer to my four pages: /home, /contact, /about, and /resume, instead of all the different pages listed in the tutorial (which uses a bloated website template that I decided not to follow, for simplicity's sake. I also didn't use the Bootstrap style sheets suggested by the author, opting instead for a much simple style sheet based on [Skeleton](http://getskeleton)). 

The main.js file is where the real magic happens: it contains the Routes, which are basically the instructions that Angular.js gives the browser: if user clicks on "/about" do this; if user clicks on "/contact" do that.

If you want to try it yourself I recommend that you read and follow the tutorial. The author is obviously a very capable programmer and can explain things much better than I can.

You can also clone the site I created. Here is the Github repo: [http://github.com/mariobox/angulartestsite](http://github.com/mariobox/angulartestsite/).

Finally, I also created a [Live Demo](http://mariobox.github.io/angulartestsite) so you can try it out on your browser.