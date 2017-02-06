---
layout: post
title:  "Adventures In Python Web Blogging Part 2"
desc: "The second part of beginning my pure PyMongo micro blog."
keywords: "python, flask, mongodb, web dev, ORM"
date: 2017-02-05
categories: [Work]
tags: [blog]
icon: fa-bookmark-o
---

<h1 style="text-align: center;">Standing On Shoulders</h1>
<br>

The famous phrase has been spoken for hundreds of years. Almost nine hundred by 
some [estimates](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants). 
It's most famous user, however, is [Isaac Newton](https://en.wikipedia.org/wiki/Isaac_Newton). What's not known by
most is the controversy surrounding the quote by Newton. The prevailing [theory](https://www.brainpickings.org/2016/02/16/newton-standing-on-the-shoulders-of-giants/) has
been that Newton was trying to complement the person the letter was for, [Robert Hooke](https://en.wikipedia.org/wiki/Robert_Hooke).
By telling Hooke that without his work on colors and light that he, Newton, wouldn't 
have been able to advance his own work on the same subject. There are a growing 
number that now think ole Isaac may have been using a bit of dry English sarcasm.

This is definitely **_not_** the case here. Without the work of the thousands nay 
millions(**?**) of people who've worked on [Python](https://www.python.org/) there's no way I could already have 
a functioning micro blog. Just to think of trying to do this without the *_many_* 
packages now available makes me smile knowing I won't have to. 

Remembering back I'd found a pretty good user login example for [Flask](http://flask.pocoo.org/) and [MongoDB](https://www.mongodb.com/)
using just the [PyMongo](https://api.mongodb.com/python/current/) distribution. It was the [FlaskLogin-and-pymongo](https://github.com/boh717/FlaskLogin-and-pymongo) repo by [Alberto 
Coletta](https://github.com/boh717) on [GitHub](https://github.com/). It didn't take much to get going. Just had to update some of the 
packages that had depricated like:

```python
from flask.ext.login 
```
to

```python
from flask_login
```

and

```python
from flask.ext.wtf
```

to

```python
from flask_wtf
```

Gutted the file `config.py` but left it just in case since it'd be easy to get rid of later.
Added my own `database.py` to the *app* directory. Deleted the old `populateDB.py` file.
Updated the `view.py` file to use my new MongoDB database object *Database* in the login route and then 
ran the `run-dev.py` file to see if it worked. After probably fixing some minor changes (I can't 
exactly remember at this point anymore, lol) this is what awaited me in Firefox:

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/pymongo-ss1.png" alt="PyMongo-Blog"></div>
<br>

Success!


# *To Be Continued...*

**_Brandon_**
