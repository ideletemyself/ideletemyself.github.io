---
layout: post
title:  "Adventures In Python Web Blogging Part 1"
desc: "The ups and downs of using python ORMs & why I decided not to use any."
keywords: "python, flask, mongodb, web dev, ORM"
date: 2017-02-02
categories: [Work]
tags: [blog]
icon: fa-bookmark-o
---


<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/Python_logo.svg.png" alt="Python"></div>
<br>


Like many IT technicians and network admins I'd used a bit of [Python](https://www.python.org/) here and there for various tasks. Usually simple scripts that did one task, maybe a couple but not much more than that. In college I remember hearing about the luxuries the language provided. At the time since I was knee deep in [C++](http://www.cplusplus.com/) and [OpenGL](https://www.opengl.org/), things like automatic clean up and all kinds of error catching seemed like a fresh cool clean river to drink from after gulping down the swill I was so used to by then. Shoot I even remember our [C++](http://www.cplusplus.com/) teacher at the time was telling us all the glories of [C#](http://www.learncs.org/). This was like 2005-ish, had I listened to him and the venerable [Dave Arneson](https://en.wikipedia.org/wiki/Dave_Arneson) of [D&D](http://dnd.wizards.com/dungeons-and-dragons/what-is-dd) fame and started making games for cell phones (**_not smartphones, cell phones member those? lol_**) I'd probably be a rich man by now. Ah but I digress.

<br>
<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/flask.png" alt="Python Flask"></div>
<br>

The most experience I have with [Python](https://www.python.org/) would be from working with [Django](https://www.djangoproject.com/) on the few web development gigs I've had over the years. If it was [Python](https://www.python.org/) then it was almost always [Django](https://www.djangoproject.com/) and while [Django](https://www.djangoproject.com/) is a joy to work with it definitely likes things done **_it's_** way. Since I'd just listened to an old podcast of [PythonTalk](https://talkpython.fm/) about [Python Flask](http://flask.pocoo.org/) with [Miguel Grinberg](https://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world) on his own personal adventure in creating a micro blog in [Flask](http://flask.pocoo.org/). I thought why not see what [Flask](http://flask.pocoo.org/) was all about, which is letting you do things more or less your own way.


<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/mongodb.png" alt="Mongo DB"></div>


Oh let me count the ways I dislike [SQL](http://www.w3schools.com/sql/). [MySQL](https://www.mysql.com/), [SQlite](https://www.sqlite.org/), whatever flavor I've just never liked them all that much. Nobody ever said how much of a joy it is to work with a [MySQL](https://www.mysql.com/) table. Or how wonderful it is to keep all the different aspects that might go wrong in your head when considering a SQL task. If someone has said these things, please, deal with them in the best way you know how(lol). [MongoDB](https://www.mongodb.com/) on the other hand *IS* a joy to work with for the most part. It's very forgiving. It just plain works with not much effort which is the best we can hope for in life and programming. Whenever I go to test some new web technology be it in some Javascript framework or whatever I always use [MongoDB](https://www.mongodb.com/) for my database. Unless I'm testing something like [TinyDB](https://github.com/msiemens/tinydb) I guess but usually it's [MongoDB](https://www.mongodb.com/). The only time I find it wanting are in various examples perhaps but only compared to articles or tutorials using [MySQL](https://www.mysql.com/) and that's only because [MySQL](https://www.mysql.com/) is still so prevelent. Hopefully someday soon we can move away from relational databases altogether.


<h1 style="text-align: center;">To ORM Or Not To ORM?</h1>
<br>

On the topic of examples. When I got things going with my little micro blog I began to notice something afoot. Almost every example I would find online inevitably used the [MongoAlchemy](http://www.mongoalchemy.org/) [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping) to get their [Flask](http://flask.pocoo.org/) web apps working. Ugh [MySQL](https://www.mysql.com/)... Oh, I was able to find a handful of really good [Flask](http://flask.pocoo.org/) web apps using [MongoDB](https://www.mongodb.com/) too but again there are just so many more examples using [MySQL](https://www.mysql.com/). On one hand I do see the practicality of teaching early [Python](https://www.python.org/) programmers to use the technology in use most today. If I had to guess I'd say the majority of [Python](https://www.python.org/) gigs would be using some form of a [SQL](http://www.w3schools.com/sql/) server and not something like [MongoDB](https://www.mongodb.com/) unless it was a company making web technology products of some kind itself. I'm totally guessing here though. Anyways, I know how to work with [MySQL](https://www.mysql.com/) and I know there's tons of tools and guides out there should I need to which is why I like using [MongoDB](https://www.mongodb.com/). I'm never going to put myself in the position again to miss out on the next big thing like I did with not pursuing cell phone games more than a decade ago now.

So then what did I do? Well, let me tell you I tried just about *every* [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping) for [Python](https://www.python.org/). From old [mongoengine](http://mongoengine.org/) examples all the way up to [MongoAlchemy](http://www.mongoalchemy.org/). I just didn't enjoy using them particularly. You see I'd already built much of my blog's logic in an object oriented way. Not like that's a big deal but it did start causing issues when trying to use all these different [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping)s. They always want you do do things in a very specific way. Which is fine if you've already been doing things in that way. If you haven't then you might start seeing areas where kinda big code overhauls or moving hunks of code to and fro starts happening. Suddenly things aren't getting initialized or ojects aren't getting recognized because you aren't doing things just so. One big problem of mine admittedly is looking too much at other people's code. Afer a while I just have to stop and start from scratch and just think it through myself. I mean I see what they're doing and understand it but usually it's not the way my mind wants to do it, so I struggle. Then I hop from example to example looking for that holy grail answer that usually just never shows itself, much like the actual holy grail.

After contemplating a bit of harry carry I came across this question & answer on [Stackoverflow](http://stackoverflow.com/questions/9447629/mongokit-vs-mongoengine-vs-flask-mongoalchemy-for-flask). The question was on which of the three [MongoKit](http://namlook.github.io/mongokit/), [mongoengine](http://mongoengine.org/) or [MongoAlchemy](http://www.mongoalchemy.org/) was the best [Python](https://www.python.org/) [ORM](https://en.wikipedia.org/wiki/Object-relational_mapping) to use. It was spooky the person who answered the question spelled out exactly how I'd been feeling using these tools. To the T. I let out an audible "YEP!" and scared my pets. This guy gets it I thought. With that I decided to turn back to my laptop and my [PyCharm](https://www.jetbrains.com/pycharm/) project waiting for me. Took a deep breath and exhaled.

# *To Be Continued...*

**_Brandon_**
