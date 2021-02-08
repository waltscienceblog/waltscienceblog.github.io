---
layout: post
image: /images/calvin.jpg
page.image: /images/calvin.jpg
summary: Make a quote generator to text motivation to you every morning.
excerpt: Make a quote generator to text motivation to you every morning.
time: 3 minute read
title: How to automate daily motivation with a little Python
tags: Python web-scraping productivity
dat: February 8, 2021
---
February is here. And, if you are like me, you can be easily bummed-out by the short days and cold weather. 

To fight this bummer of a month, I set out to build an app to text me some daily motivation - in the form of an inspirational quote. It turns out this is an easy thing to do thanks to Python, a [nicely curated quote database](https://github.com/akhiltak/inspirational-quotes/blob/master/Quotes.csv), a [sweet picture of the day website](http://www.naturepicoftheday.com), and the SMS service [Twilio](https://www.twilio.com).

I call this app... the **Quotivator** (the name is still in beta).

<p align="center">
  <img src="{{ site.baseurl }}/images/darkmorning.jpg" />
</p>
<div align="center"><em>Those dark mornings, when it is hard to get moving.</em></div>

<br>

### How does the Quotivator work?
***

The Quotivator works in four easy steps:

 1. Select a random quote from a database
 
 2. Scrape the image from the picture of the day website
 
 3. Create a markdown file with the quote and image to push to my website
 
 4. Text the quote to my phone number
 
Thanks to the magic of Python, all of this happens in under 20 lines of code! Not that anyone is counting... 

After the python code is written, I simply create an executable file to run the code, and schedule that file to run once daily with Automator for Mac. If you use Windows or linux, you can schedule executable file runs using task scheduler or cron.

<br>

### What does the Quotivator do?
***

The Quotivator provides a daily update on my website to display the [quote and photo of the day](https://waltscienceblog.github.io/quote/). You can bookmark this page or set it as your browser's homepage if you would like a new inspirational quote to greet you daily.

The Quotivator also texts the daily quote to my phone. I see it when I wake up in the morning, and it motivates to exercise and tackle my day - even when it is really dark and cold.

<br>

### What is the Quotivator an example of?
***

Well, if you are just starting out coding in Python, the Quotivator is an example of many applications. Web scraping, database updating, texting from the console, and automation. All of these are powerful tools that are easily implemented using Python. 

<br>

### How can I get the Quotivator to text me?
***

To make the Quotivator yours, just fork my [GitHub Repository](https://github.com/waltscience/todays-quote) and enter your Twilio account and key into the Python script. Then simply automate your script through automator or cron.

If you don't want to code or just want see daily quotes on your browser, bookmark or set your homepage to [my daily quote and photo page](https://waltscienceblog.github.io/quote/).

<br>

*Quote database source: [Akhil Tak's inspirational-quotes repository on GitHub](https://github.com/akhiltak/inspirational-quotes/blob/master/Quotes.csv)*

*Image source: [Nature pic of the day website](http://www.naturepicoftheday.com)*

*SMS service for Python: [Twilio](https://www.twilio.com)*

*Data and Python code available on [GitHub](https://github.com/waltscience/todays-quote)*
<br>

{% include twitter_card.html %}
