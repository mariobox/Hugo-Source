+++
Categories = []
Description = ""
Subtitle = ""
Tags = ["tech"]
date = "2016-05-12T18:00:39-04:00"
draft = "false"
slug = ""
title = "My Basic Git Workflow"

+++

This quick rundown portrays the basic workflow I go through when using [Git](https://git-scm.com/) to keep track of files. It assumes you have some basic knowledge of Git. If you don't, don't worry, there are plenty of resources online ([this is a good starting point](https://git-scm.com/book/en/v2)). It also assumes that you are using [Github](http://www.github.com) for your remote repositories. 

Here we go.

### Creating a repository from scratch 

* Open your Terminal and navigate to a folder you want to start tracking (if you don't know how to use the Terminal this [quick online course](https://www.codecademy.com/learn/learn-the-command-line) will show you the basics).

* Type <code>git init</code> to create a new subdirectory, called .git, where your file changes are going to be tracked.

* Create a new file, for example one called *grocery.txt* (a simple text file listing different grocery stores in your neighborhood) by typing <code>touch grocery.txt</code>.

* Open your favorite text editor, add some grocery store names and save the file.

* Add the file to the staging area by doing <code>git add grocery.txt</code>

* Commit your changes by doing <code>git commit -m "MESSAGE HERE"</code>. Don't forget to type your message in between quote marks explaining what you did to the file.  Since this is the first time you commit this file it is OK to just write "initial commit".

* If you want to push your file to a remote repository, you need to create the remote repository first: 

	* Go to Github and create a new project folder where you're going to place and track *grocery.txt*. You can call it *new-project*. 
	* Look around the screen for the URL of the project folder you just created. It should be something like <code>https://www.github.com/youraccount/new-project.git</code>  
	* Copy that URL, go back to your terminal, and type <br /><code>git add remote origin https://www.github.com/youraccount/new-project.git</code> 
	* Push your file to the remote repository with <code>git push origin master</code> (if at any point Github asks you for your username and password type them in).

Now you are tracking *grocery.txt* both in your local repository (your computer) and a remote repository!

Now, let's say that the next day you come back to your file and add some more grocery store names. Once you're done, do this:

* Save the file

* Do <code>git add grocery.txt</code> to add the changes to the staging area, and 

* <code>git commit -m "add grocery stores"</code> to commit your changes.

* To upload these changes to the remote repository simply type <code>git push origin master</code>. Type your username and password when prompted and the changes will be uploaded.

That's it.

### Cloning a remote repository

Cloning a remote repository means installing a copy in your local computer. You may want to clone one of your existing remote repositories to do some work on it locally, or you may want to clone a remote repository belonging to somebody else and use it as a template for your own project. In this case, first make sure you have permission from the repository owner. 

This is what you do: 

* Go to Github and follow the instructions to fork the repository to your profile. 

* If you want to call the repository something else, just rename it as you want. 

* Finally, clone the repository to your local computer by going back to the terminal and typing <code>git clone URL OF THE REPOSITORY</code>.  

Once you've cloned the repository and done some work on it, the process is the same as when you update a local repository created from scratch: you work on your files, make some changes, add them to the staging area, commit them, and finally push them back to the remote repository with <code>git push origin master</code>.
