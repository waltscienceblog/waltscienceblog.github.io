---
layout: post
image: /images/pipeline.jpg
page.image: /images/pipeline.jpg
summary: Yes, but not in the direction you might think.
excerpt: Yes, but not in the direction you might think.
time: 3 minute read
title: Is sentiment among academic job seekers in ecology changing?
tags: academics sentiment PhD Tableau R regression data-wrangling
dat: July 24, 2020
---
If you have ever been on the academic job market, you know how demoralizing it is. If you haven't had the pleasure, I can paint you a quick picture in two steps: 

 1. Imagine summarizing your life's work in 50+ unique ways each year in the hope that you are good enough in every possible way to get an interview at *any* school that might remotely seem a good fit for your work. 
 
 2. Now imagine never hearing from any of those schools again, except when someone you know gets interviewed for a position you applied for.

[Applying to academic jobs is a heart-wrenching slog](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiMz9XM2OLqAhWXQs0KHWhgCQYQFjACegQIAxAB&url=https%3A%2F%2Fwww.washingtonpost.com%2Foutlook%2F2019%2F04%2F15%2Fjob-market-academics-is-nightmare-heres-one-way-fix-it%2F&usg=AOvVaw2dt-SSfHG5ZI6LD-5xQnqA). And most often, it leads nowhere.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/pipeline.jpg" />
</p>
<div align="center"><em>Pipeline diagram showing the fate of biology PhDs. In this model, less than 8% of biology PhDs will end up as tenure-track faculty.</em></div>

<br>

The vast majority of PhDs don't end up as tenure-track faculty. One survey report from the Royal Society estimated [about 0.45% of UK science PhDs ended up as professors](https://royalsociety.org/~/media/royal_society_content/policy/publications/2010/4294970126.pdf).

The low success rate of PhDs on the academic job market is a due to a decades-long increase in supply of PhDs and a relatively flat number of tenure-track faculty jobs.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/phdvsjobs.jpg" />
</p>
<div align="center"><em>Life and health science PhDs employed by sector, and the number of PhDs awarded in those disciplines over the same time period.</em></div>

<br>

Given these odds, and the ever-increasing length of job application packets, I expected the sentiment among academic job seekers to become more negative through time.

<br>

### How do you measure sentiment among academic job seekers?
***

I chose to measure sentiment in my own field of ecology. Since 2009, ecology has had a public wiki that serves as a job and discussion board for ecologists.

The wiki has two discussion sections, general discussion and venting. The general discussion is a place to ask and answer any questions about the job search process. Venting is a place to commiserate about any aspect of the academic job search.

To test whether sentiment has changed through time, I compared the net sentiment of each thread in each discussion section for all the ecology wikis from 2009-2019. I used the [AFINN Sentiment Lexicon](https://rdrr.io/cran/textdata/man/lexicon_afinn.html), which ranks the sentiment of words from -5 to 5. 

<br>

### The trend of sentiment through time
***

Separately, the sentiment in the general discussion and venting sections of the wiki don't show any trend. But taken together, they reveal a slight uptick in positive sentiment over the past decade.

<br>

<iframe src="https://public.tableau.com/views/netsentiment/netsentiment?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Net sentiment in general discussion and venting threads of ecology job wikis.</em></div>

<br>

The graph shows **sentiment became more positive among academic job seekers using the ecology wiki since 2009**.

<br>

### What could explain the increase in positive sentiment?
***

The academic job market was likely hit hard in the late 2000's and early 2010's by the great recession of 2008. Perhaps, the job search process has gotten better since 2009 and the increase in positive sentiment reflects that?

Others have proposed that [academia shares many characteristics with cults](https://www.washingtonpost.com/outlook/academia-is-a-cult/2018/10/31/eea787a0-bd08-11e8-b7d2-0773aa1e33da_story.html). Maybe the academic cult leaders have gotten better at indoctrinating their disciples? I am joking, of course. *Sort of*. 

<br>

### Why are so many people on the academic job market?
***

There are signs that academics are starting to realize just how improbable becoming a professor is. One major sign - for the first time ever, [the portion of STEM PhDs working in industry is equal to the portion working in academics](https://www.sciencemag.org/careers/2019/03/first-us-private-sector-employs-nearly-many-phds-schools-do). 

Another sign that academics are recognizing the absurdity of the academic job market is the beginning of graduate-level training specifically designed for non-academic jobs. 
Considering so few PhDs end up in tenure-track positions, **training for careers outside of academia should be the norm**. 

Speaking from both my own experience and the experiences of my friends and colleagues, there are two major barriers to leaving the academic job market:

 - When academia is all you know, learning how to find work outside of it takes serious effort. 
 
 - Attending school and working tirelessly on research most of your life becomes your most distinguishing characteristic. 

For many, imagining ending their academic journey outside of the academy makes them feel like the sacrifices they made were done in vain. Even worse, settling for anything less than a professorship requires giving up, at least, a portion of your [identity](https://www.insidehighered.com/advice/2017/01/30/academics-can-and-should-stop-equating-their-identity-work-essay). 

**These personal barriers, the ones that keep people fighting for tenure-track jobs, may be the only reason there is *any* positive sentiment for the academic job market**.

<br>

*Ecology sentiment text source: Ecology job wiki discussion and venting section threads, 2009-2019. Collected by the author*

*Data and R code available on [GitHub](https://github.com/waltscience/ecosentiment)*
<br>

{% include twitter_card.html %}
