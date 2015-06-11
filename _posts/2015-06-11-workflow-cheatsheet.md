---
title:  "Workflow Cheatsheet"
date:   2015-06-11 10:27:17
categories: 
---

##Setting Up Your Repo

Find the repo you want, get the SSH code

{% highlight bash %}

$ git clone <git@github:something>
$ cd <REPO>
$ git checkout master 
$ git checkout develop
$ git flow init

{% endhighlight %}

You'll be asked to set some settings. Accept the defaults (hit "Enter" key until it stops doing stuff). So it should look like this:
{% highlight bash %}

$ Branch name for production releases: [master]
$ Branch name for "next release" development: [develop]
$ Feature branches? [feature/] 
$ Release branches? [release/] 
$ Hotfix branches? [hotfix/]

{% endhighlight %}

The first time you enter the repo, you need to pip install some stuff.
{% highlight bash %}

$ virtualenv ve
$ source ve/bin/activate
(ve)$ pip install <something - check the readme file>

{% endhighlight %}

For the unicore repos, the pip install commands are like so:

{% highlight bash %}

(ve)$ pip install -r requirements.txt
(ve)$ pip install -r requirements-dev.txt

{% endhighlight %}

You're set up :)

##Using the repo
every time you enter your repo
{% highlight bash %}

$ source ve/bin/activate

{% endhighlight %}

##Creating a New Feature Branch
Make sure your repo is up to date

{% highlight bash %}

git checkout develop
git pull

{% endhighlight %}

Create or find the relevant issue, get the issue number:

{% highlight bash %}

$ git flow feature start issue-<ISSUE NUMBER>-<BRIEF DESCRIPTION, SEPARATED BY DASH "-" >
$ git branch (just to check which branch you are on)
$ git flow feature publish issue-<ISSUE NUMBER>-<BRIEF DESCRIPTION, SEPARATED BY DASH "-" >

{% endhighlight %}

##Creating a Pull Request
Make sure the relevant issue has been created within the repository, get the issue number that has been assigned and then:
{% highlight bash %}

(ve)$ git push
(ve)$ hub pull-request -b develop -i <ISSUE NUMBER>

{% endhighlight %}

##Checking what other branches exist
This will show local and remote branches. Remote branches (branches on Github) begin with `origin`.
{% highlight bash %}

git branch -a

{% endhighlight %}

##Merging a Branch
Make sure you've gotten a +1 or thumbs up in your pull request
{% highlight bash %}

(ve)$ git checkout develop
(ve)$ git pull
(ve)$ git checkout feature/<BRANCH NAME>
(ve)$ git pull origin develop
(ve)$ git flow feature finish <BRANCH NAME>
(ve)$ git push

{% endhighlight %}

##check your branch merge settings and details
Navigate to root of the repo
{% highlight bash %}

cd .git
nano config

{% endhighlight %}

Use whatever text editor you want, not nec `nano` to open `config`

##To Delete a Local Branch
{% highlight bash %}

git branch -d <LOCAL BRANCH NAME>

{% endhighlight %}


##To revert a commit
Navigate to the repo
{% highlight bash %}

git log

{% endhighlight %}

This will display you your last commits and their messages
Find the uuid for the commit you want to undo

{% highlight bash %}

git revert <UUID>

{% endhighlight %}

Git will reverse the commit you made and apply that as a new commit

{% highlight bash %}

git push

{% endhighlight %}

and my personal favorite, but only to be used when you have messed up beyond comprehension . . .

## When Things Have Gone to Shit

{% highlight bash %}

rm -rf <REPO NAME>

{% endhighlight %}

[Then start again](something)