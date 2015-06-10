---
title:  "A Coding Overview"
date:   2015-06-08 17:34:48
categories: 
---
##Our Programming Language of Choice
Praekelt is primarily a Python shop. If you feel like you need a python refresher, I'd recommend doing a few online programming challenges to help remember some of the syntax structure. I use [Coderbyte](http://coderbyte.com/), but there are a [ton of options](http://codecondo.com/coding-challenges/) out there.

##OK, I can code, but how does the Internet work?
When I started as an intern at Praekelt, I knew how to program relatively small things like getting the palindromic primes between two numbers. It turns out that this is not particularly useful when you're supposed to work on a website. Pretty much everything we do is connected in some way to the web and web technologies. If you're familiar with things like HTML, Javascript and CSS, that's great. If not, that's also OK. Like me, you'll pick this stuff up as you go along. If there's something you don't understand, particularly in the first couple weeks, take your time and use Google, YouTube and other interns or devs to explain this stuff to you.

###Code style
If a bunch of people are writing and collaborating on code, it helps if there's a uniform style that everyone uses. We use [pep8](https://www.python.org/dev/peps/pep-0008) for our python code. We're pretty strict about it, in fact your builds will fail within the automated testing environment if you've failed to comply, like leaving trailing whitespace . This can be pretty frustrating, so get yourself an add-on to your text editor or IDE (like [this](https://github.com/SublimeLinter/SublimeLinter-pep8) or [this](https://atom.io/packages/pep8)) to check your code for mistakes or things that need to change. This takes the hassle out of learning all of the conventions and will make your life a lot easier.

There are a couple of concepts that you should get comfortable with:

-Web frameworks and what they are. I found [this article](http://en.wikipedia.org/wiki/Web_application_framework) and [this video](https://www.youtube.com/watch?v=b3p4rBZAwwE) helpful. The web applications that we use are [Django](https://www.djangoproject.com/) and [Pyramid](http://www.pylonsproject.org/) among others. Don't worry, you'll be given a lot of time to familiarize yourself with these technologies.

-Git and version control, which is dealt with in [this](BROKENLINK) article

-How to use the terminal or command line
