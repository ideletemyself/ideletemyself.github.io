---
layout: post
title:  "Havasu, Heroku & Hari Kari"
desc: "When things get rough just keep going."
keywords: "python, flask, tinydb, web dev, web scraping"
date: 2017-02-14
categories: [Work]
tags: [blog]
icon: fa-bookmark-o
---

<h1 style="text-align: center;">A Soup Full Of Code</h1>
<br>

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/BsMainPagePic.jpg" alt="BeautifulSoup badge"></div>
<br>

I'm sure there's a cute story behind that picture. Or maybe not. Why the 
people who maintain the documentation for the Python library Beautiful
Soup chose that picture I haven't a clue. It kind of gives a proper 
impression of the library, a bit strange, a bit quirky and with an air
of mystery surrounding it. Surely though my take on it has to be colored 
by the fact I had no experience with web scraping in general. Actually, 
I had heard of the practice before and had looked into it briefly. Distinctly 
I remember coming across Scrapy and the concept of web spyders I'd heard 
of before. The people I was working for at the time had other pressing 
needs and so that project was shelved.
 
<h1 style="text-align: center;">These Times They Are A Changin'</h1>
<br>

So this all began because I'm trying to drum up some solid work. Despite 
what some might say, not all have rode any kind of rising tide. Like all 
things though I choose to turn these kinds of times into a positive as best 
I can manage. Why not try learning Python and giving programming another go?
I haven't got anything to lose. With that spirit in mind I girded myself and 
remembered a potential client a friend had told me about a year or so ago.
It was a realtor here in Lake Havasu City and apparently they needed help. 
Maybe I could be that help.

<h1 style="text-align: center;">Choices Can Be Tough</h1>
<br>

They had a story as old as time, in tech anyways. Their old IT technician
and webmaster flew the coup and they were essentially stuck in a bad spot.
Not really any fault on the tech, this stuff just happens in life especially 
in a town like Havasu where people come and go. When I spoke with them last year
they were actually ready to make a change but were unsure which route to go. 
Basically their choices were either me, a programmer in India or pay a bunch 
of money to the company who hosts the data for their rent billing system to build
the website. As with so many choices we make in life, Lord knows I've made em, 
they made the wrong choice.

<h1 style="text-align: center;">Trying To Go That Extra Step</h1>
<br>

They chose the programmer in India. Spent a couple thousand dollars, have no
new website and now their old site is no longer functioning properly. I can't tell
you how many times I've heard this story as an IT technician myself. I understand
why someone would make that decision, they look at big corporations getting a
quality of work from people in other countries and think it's the thing to do.
IBM uses them so why not me? I won't go into all that because that would be an entire 
blog unto itself let alone a single post. Suffice it to say these situations rarely
work out for people and companies that don't work with technology themselves. With 
that horror story in mind I thought it would be a good idea to have something to show
them before I even ring them up on the phone to talk. In fact that's something I'm 
going to be doing from now on. I'm going to just go ahead and build quick mock ups 
for businesses and organizations that I like or that I see could use a new website. 
Might as well kill two birds with one stone and hopefully impress the potential client
as well as add another project to my portfolio.

<h1 style="text-align: center;">Geocities Style!</h1>
<br>

Wow, I had forgotten just how badly these people needed a new website. Just take a 
look for yourselves, here's their banner:
<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/hr-oldbanner.png" alt="Havasu Vacation Rentals banner"></div>
<br>

Before you get concerned don't feel bad they know they need an upgrade. Also, the site 
is functionally inactive. They're just paying to keep the domain ranked as highly on Google 
search results as it is currently. That's what seventeen years on the web will do for you. 
They have a decent number of backlinks I guess but honestly the only reason they are ranked so 
highly has got to be their age online. It certainly isn't getting any points for being responsive
because obviously it's not. This should give budding web developers and designers some hope.
Yes, there are still thousands upon thousands of these kinds of sites still on the internet. 
With people and businesses behind them. We can help these people if they would only let us. We 
can't blame them for their hesitation though. It's like if I went to go buy some serious piece 
of art. I'd have no idea what makes a smart investment in that field. It would take a good couple 
weeks of hardcore studying to even get a feel for what all that would entail. The same if not more 
goes for our work no matter how much art or math and science goes into it. It all seems like magic
to a layperson.

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/keep-calm-and-web-scrape.png" alt="Keep Calm And Web Scrape"></div>
<br>

Web scraping can be difficult. Don't let anyone tell you differently. Sure, it can be super easy. Like 
when you watch the countless YouTube programming mentors fire up their IDLE
and in five lines of code have you thinking that's how easy it is to start 
scraping the web. In a way, sure but honestly I think that's kind of disingenuous. Again, I fully
understand why this happens. They want you to throw down on their online courses. Or maybe show you 
just enough so you'll keep watching more trying to learn as much as possible. Most of 
them do say they'll help anyone who asks in the comments and as far as I can tell they do. 
Granted many of them even tell you it's a very basic example. I ask why do the same tutorial 
that the other ten or how ever many other relevant programming mentor YouTube channels there are 
have already done? This is just a problem YouTube creators have in general.

It's just don't tell me loading those ten lines of HTML you lovingly formatted just so is 
anything like someone would find in the real world. A world filled to the brim with bad code, bad 
practices and just plain bad programmers. Oh really, you can pull data from the Yellow Pages web site?
Marvelous bro, we might as well just learn using API's released by companies themselves. Which I actually 
am doing and highly recommend. But I want to learn about web scraping and more importantly real world
use cases in drilling down for text. Drill baby drill! Sorry I had to.

<h1 style="text-align: center;">I've Got A Plan</h1>
<br>

The plan as it stands is to have my mock website web scrape data from the old/current website. It should
only do this once a day and only if a user visits the home page. Only one of those functions is currently 
working but it's the most important one. I'll show you my code then tell you the story:
<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/havasu-rentals-code.png" alt="Havasu Rentals Code"></div>
<br>

If you look at the code on my Github you'll see I've got a Property class that I'm not even using currently.
At any rate, that little diddy above took me about two days to come up with and I can't count how many Github commits.
I tend to be commit crazy like that. At first I had one master for loop with two or three loops nested within. That 
just didn't work or rather I got MOST of it working but just one other part wouldn't work as it should. Basically what 
I am trying to get at are all the property unit numbers, then page URL links for each rental property. Then all the image links for each one of those
properties. Last is to get the property's description which includes what seasons it's available for as well as the daily, weekly and 
monthly rates if they have them.

In the end I want all of that data to be dynamically updated to the page when a user first visits the 
home page as I've said before. As of this blog posting the data was statically loaded straight from the HTML source code.
The reason for that is that I knew I could just pull the source code and get something up on the web before I got this 
web scraping and dynamic data loading down and working. So I went and started looking at some Bootstrap templates for
inspiration. I found one called "Modern Business" that looked pretty good and since it was free I went ahead and downloaded it.
<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/w3schools.png" alt="W3 Schools"></div>
<br>

After a little messing around I started to get something going. Soon though I ran into a road block. The template's Bootstrap 
image carousel just would not display properly for me. I ended up spending far too long trying to get it to display just as 
I wanted it and it never got there. This and other things led me to actually end up choosing to go with W3's css file instead. 
You see I'd been using W3's awesome site for instructions on Bootstrap and would continually see how much easier and logical 
to my mind W3's way was compared to Bootstrap's. First let me just say that this or any of these blog posts I make, none of them
are in any way supported by or influenced by any of the companies I'll mention. At least not yet HA! If I mention them
it's because that's what I used at the time. If I choose one company or brand over another it's because that's what worked for me 
at the time. I hold no loyalties, I was a life long Pepsi drinker as a kid and then I drank Coca-Cola and it was great. Now 
I don't drink any soda at all so there ya go.

<div style="text-align: center;">
<img align="center" src="https://ideletemyself.github.io/static/assets/img/blog/blog images/tinyDBlogo.png" alt="TinyDB Logo"></div>
<br>

Now I had something. It wasn't the greatest site in the world. Far from it. Hell, it wasn't even fully responsive yet and it still isn't.
But it was something and it was clearly better than what they currently have. I decided it was a good time to give the potential client
a call before I continued with the project. They expressed interest and since they still were without a technician they
might want my help there as well. Seems they're still considering just going with the company who hosts their rent payment system. I
think me mentioning I already had a website to show them made a good impression as I heard they were surprised. Oh, I forgot to mention
that I uploaded what I had to Github and then deployed to Heroku. I'll be saving that whole experience, which has been great so far
and my TinyDB experience which has also been great but trying as well, for another post. We decided to keep in touch and revisit the idea over the next couple of months.

That wasn't what I was hoping for but was better than being told no. With the possibility of the venture taking place 
at some point in the future I felt it was okay to continue work on the site even if it never came to be at least I could 
use it as a learning tool and hopefully impress someone with what it does. Hopefully it won't make a bad impression 
but I'm preferring to just put my work out there such that it is. I mean people can just go to my Github account and see my commit history
so it's all out there anyhow. More to the point though I know it will show people that I'm learning and that I'm actually understanding 
what's going on. Because I know that I am learning. I've come so far in just the two or three weeks I've been at this now. Messing around 
with Beautiful Soup, pandas, TinyDB, deploying to Heroku, testing Mailgun with my other app the Pymongo-Blog microblog, Flask, regex 
and on and on and on. Let me just say finding out about regular expressions was the key to getting my web scraping to actually work and 
get at the text I actually wanted and being able to get just the text with no HTML tags or new lines or white spaces.

There's really no joy and fulfillment I can think of than the feeling I get from advancing or completing 
a coding project. The closest I can compare it to is after a really good yoga session or playing my guitar and keyboards or singing. Don't 
get me wrong there can me moments, no hours of sheer frustration. Times when you just have to walk away but then you do and come back ready 
to attack again. Maybe you defeat that problem or maybe you don't and you have to walk away again. There were times during this project so far 
when I'e considered just giving up and going to something else. I may put this project to the side but it will be because I'm at a good spot to stop
not because I couldn't advance the project. Next up now that I have my web scraped data loaded into TinyDB is to figure out how to apply that data. 
Perhaps by using my Property class I have ready to go. Then I can most likely get my saved data reproduced through Flask
and at that point I could build the entire new site and just load the data from the old site if that ever got working. Seems they're very concerned with
their spot on Google results as they should be but at the point they keep it there just so they get calls over
perhaps using a new website to drive business online not just by the phone. I think I'll also mess around
with media queries and get the site to be responsive and display properly which shouldn't take too much work but isn't a small task either.

# *To Be Continued...*

**_Brandon_**
