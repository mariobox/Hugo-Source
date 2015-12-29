+++

date = "2015-12-22"

Categories = []

Tags = ["tech"]

Description = "The Git commands I regularly use to version control and deploy this site"

title = "Git Cheat Sheet"

slug = "gcs"

+++



I use Git to keep track of the changes I make to this site. I am not an expert on Git nor am I a programmer so I really won't go into great depths here. The idea of this post is just to summarize for future reference the Git commands I use on a regular basis to keep this site up and running. 

Here we go:

<pre><code>git config --global user.name "your user name"</code></pre>

<pre><code>git config --global user.email "your email"</code></pre>

Tell Git your usename and email. You only need to do this once.

-----

<pre><code>git config --list</code></pre>

Prints a list all the options you have configured Git for, including your user.name and user.email.

-----

<pre><code>git init</code></pre>

Creates a Git repository in the current folder.

-----

<pre><code>git clone /path/to/repository</code></pre>

Clones (makes a working copy) of an existing repository. If the repository is in a host like [Github](http://www.github.com) the path to repository will typically be a URL like: https://github.com/username/username.github.io.git.

-----

<pre><code>git status -s</code></pre>

Shows you the status of files in the current directory, in short notation. You will get one or two characters to the left of the file name: 

* M: the file has been modified
* A: new file that has been added to the staging area
* MM: file that has been modified, staged, and modified again
* ?: new file not yet tracked

-----

<pre><code>git add file name</code></pre>

or

<pre><code>git add --all</code></pre>

Adds a file, or all files that have been created or modified to the staging area.

-----

<pre><code>git commit -m "commit message"</code></pre>

Commits (records) your changes to your local Git repository. Remember to write a short message between the quote marks so that others can understand what you did.

-----

<pre><code>git push origin master</code></pre>

Pushes (uploads) your changes to your remote repository.

-----

<pre><code>git pull origin master</code></pre>

If you've made changes to your remote repository that are not reflected in your local repository, this command will merge (copy) those changes to your local repository. This is very useful when you mess something up in your local and want your files to revert back to the state they were when they were last pushed to your remote.
