---
layout: post
title:  "Gitflow and workflow"
date:   2015-06-08 20:59:45
categories: 
---

So how do we use git, github and gitflow to create our work flow?


We need to think about branches. There are 3 types of branches; Master, Develop and Feature branches. This structure is not enforced by git or Github, but its the approach taken by gitflow.

So, our branches. Our 'busiest' branch is the develop branch. This is where the software product as a whole is developed, where things are tried out and the branch that all the devs are developing. When we're finished with what we've been working on, we can then create a 'release'. This is done by taking everything we've done in develop and merging it in to the master branch. The master branch is the final product, it's the software that the customer or user is allowed to use. In our case, it's the software that is uploaded to the servers. Each merge in to the master branch has a release number (e.g. v0.0.2 or v1.0)

But it would be too complicated for all the devs to be working on different ideas at the same time on the same branch. So to do this, each dev or dev team works on a different branch, a feature branch. So, say for example we're working on a website and we want to add search functionality, display a picture along with articles and we want to fix a bug. Finishing those objectives will constitute a release. A feature branch will be created for each of the features (surprise!).