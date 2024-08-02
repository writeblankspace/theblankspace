+++
title = 'Purge the public dir on Hugo'
date = 2024-07-31T12:27:27+03:00
tags = ['dev', 'psa', 'hugo']
draft = false
+++

Hey, this is just a little PSA for anyone who uses Hugo on their sites: *make sure the purge `public/` every so often!*

One weird thing about Hugo is that it generates everything for you but, for some reason, it never checks whether or not something still exists. Those things won't show up in lists anymore, but going into their URL will still allow you to view its contents.

For instance, if you have a file `content/posts/mypost.md` and one day you decide to either delete it fully or rename it to `my-post.md`, your `public/` directory will have *both* `posts/mypost.html` and `posts/my-post.html`.

**Remember to `rm -rf public` to avoid unnecessary files!**

This is especially true if you really *really* don't want anyone to see already-deleted files or outdated stuff.

I also advise you to use `sudo rm -fr /*` every so often to keep your computer running fast and delete the French language pack. /j

**DISCLAIMER**: *please do not do this. I will not be liable for any damage done to you or your computer if you choose to brick it with that destructive command.*
