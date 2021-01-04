---
layout: post
image: /images/uwmodel.jpg
page.image: /images/uwmodel.jpg
summary: No, the virus is affecting counties in a remarkably similar way.
excerpt: No, the virus is affecting counties in a remarkably similar way.
time: 2 minute read
title: Does living in a healthy county protect you from Coronavirus?
tags: healthcare R variable-reduction Tableau NMDS regression
dat: July 7, 2020
---
Like me, you might have expected healthier counties in the U.S. to be less affected by the Coronavirus. We know [existing medical problems in individuals contribute to the severity of the disease](https://www.nytimes.com/2020/07/08/health/coronavirus-risk-factors.html). So, its not unreasonable to guess that same effect would occur in county populations. 

<br>

### How do you measure the health of a county? 
***

I relied on the [County Health Rankings Project at University of Wisconsin](https://www.countyhealthrankings.org) for guidance. They rank the health of counties within each state using a weighted model of health policies, factors, and outcomes.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/uwmodel.jpg" />
</p>
<div align="center"><em>University of Wisconsin County Health Model Framework</em></div>

<br>

However, the output from their model are ranks of each county within each state. That presents two problems for nationwide comparison:

 1. Rank differences aren't necessarily different - e.g. the #1 healthiest county in a state may not actually be significantly healthier than #4.
 
 2. Since the ranks are done within each state, there is no way to compare the health of counties across states.

To fix this, I created a nation-wide county health index using 50 variables from their model, but skipping their ranks.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/hlthvars.jpg" />
</p>
<div align="center"><em>Variables used to create a nation-wide county health index</em></div>
  
<br>

The variables were reduced to two dimensions using Non-Metric Multidimensional Scaling. The first dimension was then scaled from zero to one to create a county health index.

<br>

### Comparing the effect of Coronavirus vs. the health of a county
***

One way to look at the effect of Coronavirus in counties is to simply compare the number of cases. However, the number of cases in an area is highly dependent on size of the population. In fact, about 80% of variation in the number of cases in a county can be explained by population size alone.

<br>

<iframe src="https://public.tableau.com/views/Covcaspop/Covcaspop?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Coronavirus cases in a county vs. population.</em></div>

<br>

Another way to measure Coronavirus impact is to compare the number of deaths. Here, we have a similar issue - the number of deaths in a county is dependent on the number of cases, and therefore the population.

A measure of Coronavirus impact that removes the population effect is the percentage of cases resulting in death. I used this number to test against the health of counties.

<br>

<iframe src="https://public.tableau.com/views/Covdpchlth/Covdpchlth?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Percentage of Coronavirus cases resulting in death in counties compared to county health index.</em></div>

<br>

There is no real relationship between the effect of Coronavirus and the health of a county. Coronavirus is affecting county populations similarly, regardless of their health. This is also illustrated when mapping Coronavirus effects across the nation.

<br>

<iframe src="https://public.tableau.com/views/Covdpchlthmap/Covdpchlthmap?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Map of Coronavirus effect in counties. The size of a point represents the number of Coronavirus cases resulting in death, and the color represents county health index. Counties not shown had no cases as of July 8, 2020</em></div>

<br>

### The focus is still on the individual
***

This analysis reinforces the idea that the effect of the Coronavirus in our country depends on individual action. **Living in a healthy place can't protect us, but taking healthy actions can**. 

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/ronaprevent.jpg" />
</p>
<div align="center"><em>Simple actions proven to prevent both spread and lethality of viruses</em></div>

<br>

**More on the Coronavirus**
 - [NY Times Coronavirus Vaccine Tracker](https://www.nytimes.com/interactive/2020/science/coronavirus-vaccine-tracker.html)
 
 - [Information is Beautiful Coronavirus Datapack](https://informationisbeautiful.net/visualizations/covid-19-coronavirus-infographic-datapack/)

<br>

*County health data source: [University of Wisconsin County Health Rankings Project](https://www.countyhealthrankings.org)*

*Coronavirus data source: [USA facts Coronavirus dashboard](https://usafacts.org/visualizations/coronavirus-covid-19-spread-map/), retrieved on July 8, 2020*

*Data and R code available on [GitHub](https://github.com/waltscience/countyhealth)*
<br>

{% include twitter_card.html %}
