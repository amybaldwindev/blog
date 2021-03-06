---
layout: post
title: Updating with Git Rebase
postAuthor: Amy
authorTwitter: https://twitter.com/amyb008
gravatar: https://1.gravatar.com/avatar/d44fe63cf420551f2b70463077b14f06
---
I'm in the process of (finally) getting my blog up and running, though I've been writing the occasional article about my coding journey, I’ve had other priorities in life in the last six weeks. After much tinkering, I decided to put a commit in even though it's still very much a work in progress then headed over to the url to see that everything worked properly.

Nothing except my initial 'Hello, world!' placeholder was visible. I tried not to freak out took a couple of deep breaths and double checked the page on the local server. It all looked fine there. I wasn't sure what was going on?! I checked around on my other open project on my computer, they were unchanged. The commits appeared to be on github so I decided to delete my local copy, reboot my computer, and troubleshoot whatever was going on with a fresh clone. Once I cloned it though, the local server still looked as expected. It then dawned on me my changes were made in the master branch, and to use github pages you need to push up to the gh-pages branch. After Googling how to push the changes from my master branch to the gh-pages branch I found some information on git rebase. The process required me to subsequently Google some more stuff including how to resolve merge conflicts (there were quite a few since I'd done quite a bit of work on my master branch). 

Finally, everything was up-to-date on my branch, a simple git push should help right? Well, then git thought my branch was behind and tried to be helpful by running a git pull. I'm very happy I'm very familiar with what git pull does and knew that was not the right course to take and likely lead me in a circle back to where I started. A little more Googling and I learned that for my situation it was appropriate to rewrite the files by using the --force option. If you're new to using git know that this is inadvisable in most cases and you should proceed with caution.

I'm pleased to announce that I got my gh-pages branch up-to-date so that my work-in-progress blog that you're currently reading is visible to all. 

Update: After I got done doing this it occurred to me that I probably could have merged the main branch into the gh-pages branch, resolved the conflicts and done a push which would likely work better if there were many collaborators on the github repo. I've done a little reading and included a link below that does a pretty good job helping me understand the differences between these two options.

Additional reading: <a href="https://www.atlassian.com/git/tutorials/merging-vs-rebasing" target="_blank">Merging vs Rebasing tutorial from Atlassian</a>