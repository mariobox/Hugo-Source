# mariosanchez.org

My personal website powered by [Hugo](http://gohugo.io).

-----

### Writing the content

Posts and page content are written in Markdown. Posts are saved in the <code>content/post</code> folder. Book reviews are saved in the <code>content/book</code> folder. Regular pages (about, contact) are saved directly in the <code>/content</code> folder root.

### Generating the site

After running the <code>hugo</code> command from the project's root folder, Hugo crawls the content and template folders to detect any changes, and generates/updates the site's HTML files, which are stored in the <code>/public</code> folder.

### Deploying the site

After running <code>git add</code> and <code>git commit</code> in my local computer, I <code>git push</code> the source files to this Github repository. I then do a <code>cd public</code> and <code>git push</code> the HTML files to a second Github repository: <code>mariobox.github.io</code>. This repository is powered by [Github Pages](http://pages.github.com) which deploys my site to the open web.

For more implementation details visit: http://mariosanchez.com/colophon/.

-----

Special thanks and kudos to [Steve Francia](http://github.com/spf13) for creating [Hugo](http://gohugo.io).
