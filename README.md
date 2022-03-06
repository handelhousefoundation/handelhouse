## Welcome

The HHFA site is built using hugo.

To run the site locally simply the following command in the project root.

`hugo server`

The theme is a port of a port, and is attributed at the bottom of the site.
Please don't remove any attributions of this work, unless you are fully rebuilding the site from scratch.

To update any aspects of the theme, you will need to cd into `handelhouse/themes/hugo-story`
There you will find the submodule in control of the structure and styles. 
If you wish to make edits, you will need to get access from 144.mdgross@gmail.com
See the submodules section for more info

## How To Deploy Changes

1. You will need a github access token setup with access to this repo. 
2. After all your changes in your branch are ready, run the `hugo` command to generate static assets for the deploy.
3. Commit and push those changes from running the command.
4. Merge your branch into the `main` branch. 
5. Since the website runs on gh-pages, your changes merged to main will be trigger a build of recent work.
6. You can check when the last deploy happened [here](https://github.com/handelhousefoundation/handelhouse/actions/workflows/gh-pages.yml)

Note: if you forget to run and commit the changes from the hugo command, your styles will not be applied.


## Working with the Submodule

https://github.com/144mdgross/hugo-story

Submodules can be a little strange to work with. They are a git repo within a git repo.
While working in the code, it is easy to travel between the 2 repos and then realize afterwords you need to reconcile
that the work actually lives in two spots. 

Once you accept that, it is pretty easy to work with.
When you make changes in the `hugo-story` dir, you'll notice you are in a new repo.

1. Simply create a new branch there then commit and push your changes. 
2. Merge the changes back to `master` (because it's an older repo).
3. cd back out to the parent project
4. then you can run `git submodule update` to tell your outer repo to use those new changes. 
5. after that, run `hugo` to rebuild with the changes, and commit all changes from the last two steps
6. once you merge these changes back to `main` they will all appear.

