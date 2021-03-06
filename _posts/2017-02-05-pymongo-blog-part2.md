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

<h1 style="text-align: center;">Standing On The Shoulders Of Giants</h1>
<br>

The famous phrase has been spoken for hundreds of years. Almost nine hundred by 
some [estimates](https://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants). 
It's most famous speaker, however, is [Isaac Newton](https://en.wikipedia.org/wiki/Isaac_Newton). What's not known by
most is the controversy surrounding the quote by Newton. The prevailing [theory](https://www.brainpickings.org/2016/02/16/newton-standing-on-the-shoulders-of-giants/) has
been that Newton was trying to complement the person the letter containing the quote was for, [Robert Hooke](https://en.wikipedia.org/wiki/Robert_Hooke).
By telling Hooke that without his work on colors and light that he, Newton, wouldn't 
have been able to advance his own work on the same subject. There are a growing 
number that now think ole Isaac may have been using a bit of dry English sarcasm.

This is definitely **_not_** the case here. Without the work of the thousands nay 
millions(**?**) of people who've worked on [Python](https://www.python.org/) there's no way I could already have 
a functioning micro blog. Just to think of trying to do this without the *many* 
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
ran the `run-dev.py` file to see if it worked. After adding the decorator code: 

```python
def login_required(f):
    @wraps(f)
    def decorated_function(*args, **kwargs):
        if g.user is None:
            return redirect(url_for('login', next=request.url))
        return f(*args, **kwargs)
    return decorated_function
```

to the *init* file, this is what awaited me in [Firefox](https://www.mozilla.org/en-US/firefox/new/):

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/pymongo-ss1.png" alt="PyMongo-Blog"></div>
<br>

Success!

The nav bar was updated to show the `register` and `login` links depending on if they're logging in or not.
I also updated the [Bootstrap](http://getbootstrap.com/) and [jQuery](https://jquery.com/) files while I was at it. The next step was to add 
the `blog.py` and `post.py` files from an old project along with their html template files. I then
had to add the `RegistrationForm`, `BlogForm` and `PostForm` classes to the `forms.py` file.

Some love had to be shown to the routes in `views.py` so I added the functionality to register
a new user with this code:

```python
@app.route('/auth/register', methods=['GET', 'POST'])
def register_user():
    form = RegistrationForm(request.form)
    if request.method == 'POST' and form.validate():
        User.register(form.email.data, form.password.data)
        User.login(form.email.data)
        flash("Registered successfully!", category='success')
        return redirect(request.args.get("next") or url_for("login"))
    else:
        return render_template('register.html', form=form)
```

After a little tweaking this was my result:

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/pymongo-ss4.png" alt="PyMongo-Blog regisration page"></div>
<br>

Not too shabby... Well now the blog and post routes were just begging to be created. You can check out
the code on [my GitHub](https://github.com/ideletemyself/PyMongo-Blog) for the rest as this isn't really a step by step tutorial, it's my story.
So after quite a bit of effort on my part I managed to get a user to be able to register to the MongoDB database, then login or login
if they already had an account, create new blogs along with new postings within each blog. Here's what the main blogs page
looks like, it's showing a list of blogs:

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/pymongo-ss2.png" alt="PyMongo-Blog blogs list"></div>
<br>


Overall I'm pretty happy so far with where I'm at. I made a few small improvements while watching/listening to the [Superbowl](https://twitter.com/SuperBowl)
today. Stuff like adding any commenting at all. Heh Heh. I'm usually better with stuff like that but I was so busy working on 
the nuts and bolts of it. So *usually* I try to comment everywhere possible. The list of things left to do is rather long still.
Like adding all the functionality for the `settings` page where the user will be able to change their email or password if they want to.
This is a good place to stop for now though. I'll be updating this project throughout this week.

# *To Be Continued...*

**_Brandon_**
