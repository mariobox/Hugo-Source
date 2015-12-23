+++

date = "2015-12-23"

Categories = []

Tags = ["tech"]

Description = "How to create a barebones but functional Hugo site"

title = "How To Create a Minimal Hugo Site"

url = "/minimalhugo"

+++


These are the instructions to create a minimal, functional Hugo site. For more information read the [Hugo Documentation](http://gohugo.io/overview/introduction/)

#### Download Hugo 

You can download Hugo for many different platforms from the [Hugo site](http://gohugo.io).

-----

#### Install hugo in a work folder like C:\Users\Project

Go to your terminal and from your root go to your /Project folder:

<pre><code>cd Project</code></pre>

-----

#### Create a new Hugo site in a subfolder of Project called /projecthugo:

<pre><code>hugo new site ~/Project/projecthugo/</code></pre>

-----

#### Go to your Hugo site folder:

<pre><code>cd projecthugo</code></pre>

-----

#### List the contents of the /projecthugo folder:

<pre><code>ls</code></pre>

You should now see a skeleton with the basic structure of a Hugo site but no content or any of the folders or files:

<pre><code>archetypes  config.toml content layouts static data</code></pre>

-----

#### Installing Hugo in your path.

Copy the hugo.exe into your /projecthugo folder.

Do <pre><code>ls</code></pre> 

again and you should now see the hugo executable:

<pre><code>archetypes  config.toml content layouts static data hugo.exe</code></pre>

-----

#### Create some posts

<pre><code>hugo new post/post1.md</code></pre>

Open post1.md with your favorite text editor and you will see three fields already pre-written in the top section of the file, called "front matter" (between the +++ marks). By default, Hugo includes:

* Description
* Date and 
* Draft 

You can add more parameters later. For example, you may want to add a Title (if not, Hugo will "guess" the title from the file name).

Update the Description field and write some content below the second +++ line (leave one or two lines blank at the beginning).

If you want your post to go live change <pre><code>draft = true</pre></code> 

for 

<pre><code>draft = false</code></pre>

Create another post called post2.md following a similar process.

-----

### Create a couple of main pages that are not posts

These are pages like **about** or **contact**

<pre><code>hugo new about.md</code></pre>

and

<pre><code>hugo new contact.md</code></pre>

Open your favorite text editor and create some content for about.md and contact.md

-----

#### Create _default templates

You will create four templates and place them in a folder called /layouts/_default:

- single.html
- list.html
- summary.html
- li.html

* Single is for your individual content (e.g. posts or pages)
* List is to create a list of posts.
* Summary and li are views that will be used in your List template, depending if you just want a list of posts titles or a summary of each post in addition to the title.

The Hugo documentation provides instructions on what code to use in each of them.

You can create section specific templates if your site is larger but for now _default templates are all we need.

-----

#### Create partial templates

These are good for the common areas of your site. Go ahead and create:

* header.html (includes a link to the style sheet and the site's navigation)
* footer.html (for copyright or similar info)

Place this templates in a folder called /layouts/partials/. These partial templates can be called from any other template (for example from single.hmtl or list.html) by simply using the following code within those templates:

<pre><code>{{ partial "header.html" . }}</code></pre>

or 

<pre><code>{{ partial "footer.html . "}}</code></pre>

-----

#### Create an index.html template

This template is only used for the home page. Create it however you want your home page to look and place it in the root of the /layouts folder. 

-----

#### Create a /static/css folder and upload a style sheet.

Don't forget to link to the style sheet from the header.html partial template:

<pre><code>< link rel="stylesheet" type="text/css" href="/css/style.css" ></code></pre>

-----

#### Create a /static/images folder and upload some images.

Self explanatory.

-----

#### Update your config.toml file

Just add the URL of your site and your site's description. That's all you're going to need to start. You can add more parameters later.

-----

#### Try out your site

Once you have created content and templates it's time to view your site. Type the following command:

<pre><code>hugo server -w</code></pre>

If everything went well Hugo will generate your website and you will be able to see it at http://localhost:1313 . 

#### Get your site ready to upload

Once you're satisfied with the way your site looks, run the hugo command by itself:

<pre><code>hugo</code></pre>

You are now ready to upload or git push your site to your web hosting service.

-----

*Update:*

If you don't want to start from scratch, I have created a Minimal Hugo Site and git pushed the [source code](https://github.com/mariobox/MinimalHugoSite) to github.

You can simply clone the repository by running:

<pre><code>git clone https://github.com/mariobox/MinimalHugoSite.git</code></pre>



