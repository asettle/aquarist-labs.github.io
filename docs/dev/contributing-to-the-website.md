---
layout: page
title: "Contributing!"
---

So glad you want to contribute to the Aquarist Labs website! Whether
it's a simple fix or an entirely new section, we welcome your feedback
and improvements.

# Intro

The website is hosted via [GitHub Pages](https://pages.github.com/)
and uses Jekyll with the default [minima
theme](https://github.com/jekyll/minima) for a clean, efficient look.

As with all GitHub Pages, this is driven from our [git
repository](https://github.com/aquarist-labs/aquarist-labs.github.io)
that you are free to open issues on - or to directly clone, checkout,
and open pull requests against like with every other Open Source
project.

Most of our content uses [simple
markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
for the content.

Before opening a Pull Request, we do ask that you try your contribution
locally to make sure it all builds and looks right.

The existing documentation on all these components is excellent, but can
be a bit daunting. This page will walk you through an easy guide
to get going locally, and quickly.

# Walk-through

You do need a local system with Linux installed, and we assume basic
familiarity with a Linux environment. This guide assumes `openSUSE`, but
we welcome additions for other distributions!

First, make sure you have the right packages installed - this step will
need to be completed as `root`:

```shell
zypper in ruby ruby-devel gcc-g++
```

Second, make sure that your user's environment is properly set up to
install Ruby gems locally:

```shell
mkdir ~/gems/
export GEM_HOME=~/gems/
export PATH=$GEM_HOME/bin:$PATH
```

You may want to add these `export` lines to your `~/.bashrc` or
equivalent to ensure these are always set up right.

Now, change to whatever directory you want your fork of the website
source code to live in:

```shell
# Check out the website repo:
git clone git@github.com:aquarist-labs/aquarist-labs.github.io.git
# (Obviously, if you've forked/cloned this on GH, change that URL.)
```

Now all that's missing it ensuring that you have the gems needed to
serve up the content locally:

```shell
cd aquarist-labs.github.io
bundle up
```

If the previous step complains about permissions, do not use `sudo`
(unless you really want to). This guide assumes that you want to set it
all up to run as your user, and not install all these gems system-wide.

And now you're almost done - by running the following command, you will
be able to view the website on your local machine!

```shell
bundle exec jekyll serve
```

This should yield output like this:

```
    Configuration file: /home/lmb/sources/aquarist-labs/aquarist-labs.github.io/_config.yml
                Source: /home/lmb/sources/aquarist-labs/aquarist-labs.github.io
           Destination: /home/lmb/sources/aquarist-labs/aquarist-labs.github.io/_site
     Incremental build: disabled. Enable with --incremental
          Generating... 
           Jekyll Feed: Generating feed for posts
                        done in 0.092 seconds.
    /home/lmb/.gem/gems/pathutil-0.16.2/lib/pathutil.rb:502: warning: Using the last argument as keyword parameters is deprecated
     Auto-regeneration: enabled for '/home/lmb/sources/aquarist-labs/aquarist-labs.github.io'
        Server address: http://127.0.0.1:4000
      Server running... press ctrl-c to stop.
```

*Congratulations!* If you now navigate your browser to the URL listed
after `Server address:` in this section, you should see exactly this
site.

# And without further ado ...

You are now reading to make local changes to the site, commit them, and
create pull requests!

Thanks for all your help.


