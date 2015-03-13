# CIME-workflow
This will document the git-based workflow for CESM/CIME
Typical work cycle

---
fork a copy on github from the “master repo”, $CESM_GIT,  into your “sandbox” on github, $MY_CESM_GIT

````
fill this in
````

----
get a copy of the the remove repository on your local machine:

```
git clone $MY_CESM_GIT
````

your “origin” is $MY_CESM_GIT 

---
update your repo with the latest changes from the remote by pulling in changes on the github UI or add a remote on the command line.

````
$ git remote add cesm-git $CESM_GIT 
````

the above will add cesm-git as an alias for the url to CESM_GIT on github.

---
pull changes form the remove repository into your local repository
note - this will not update your working - this will only merge changes from the remote repository
into your local repository (in the .git)
````
$ git fetch origin

$ git fetch cesm-git
````
---
view contents of local repository for cam (may also enter URL/path into web browser)
see what cam branches are available in your local copy of the repo:
````
$ git branch --list *cam*
````
---
view contents of local repository for cam (may also enter URL/path into web browser)
see what cam tags are available in your local copy of the repo:
````
$ git tag -l *cam*
````
---
view contents of remote repository for cam (may also enter URL/path into web browser)
see what branches are available for cam in the central remote repo:
````
$ git branch --list -r cesm-git*cam*
````
---
view contents of repository for cam (may also enter URL/path into web browser)
see what cam tags are available in the central remote repo:
````
$ git branch --list -r cesm-git/cam/trunk_tags
````
