### Install Jekyll and its dependencies:

- Get a new-ish version of ruby. You can use the first part of this guide to install rbenv, which allows to run a newer version of ruby side-by-side with the older version that came with Linux. https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-with-rbenv-on-ubuntu-16-04 Just follow their explanation until you hit the "Working with Gems" section. </br>

- After that, you can install "bundler" and "jekyll" via the gem system. 'gem install bundler jekyll' </br>

"	For more info on this, check out: http://bundler.io/ and https://jekyllrb.com/docs/installation/

### Create a new project:

- Every Jekyll project consists of something called a Gemfile, where you list all the versions of Jekyll and any themes/plugins you'd like to use. Via the 'bundle install' command, everything will be set up for you. </br>

- For a theme: </br>

there's a number of different ways to get it working: either copy their Github directory, install it via the Gemfile OR install it via the Gemfile but specifically aimed at Github pages. **So, keep note of what the documentation you're reading is describing exactly, to avoid confusion!**

### Tweak the contents to your liking: </br>

- Everything in Jekyll is based on a number of .html lay-outs for different "types" of webpages (main landing page, blog posts, archives, etc.), some liquid templates that allow for easier referencing between files and templates, CSS templates, etc.

- The only thing you really need to do yourself is write the page contents in markdown files and configure the main settings in the _config file (unless you want to tweak the lay-out further of course, like adding things to the footer of your site). 

- The minimal-mistakes documentation is a superb resource for this, and it should carry over to other templates, for the most part. Definitely check out the _config explanation, or take a look at the one we're using. A very important aspect is the url and baseurl entry.

- You can look at a local copy of your site via: bundle exec jekyll serve or build it using bundle exec jekyll build. This'll create a _site directory containing the plain HTML files you'll need to host your site.

- Another unique property of the minimal mistakes theme is that, if you ever want to tweak the default lay-out or CSS, you'll need to copy the settings from your system-wide theme config folder, to your current working directory. You can find their locations by running bundle show minimal-mistakes (as described here: https://mmistakes.github.io/minimal-mistakes/docs/overriding-theme-defaults/).

### Hosting on the RSG domain: </br>

Use FTP/SSH access to our own subdomain, and just copy the contents of the _site directory into the /home/rsgsweden/rsg-sweden.iscbsc.org/directory
