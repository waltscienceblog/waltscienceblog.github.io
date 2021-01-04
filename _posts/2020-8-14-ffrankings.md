---
layout: post
image: /images/ffpreview.jpg
page.image: /images/ffpreview.jpg
summary: No, maybe a little for top-tier running backs, but even then.. its dicey
excerpt: No, maybe a little for top-tier running backs, but even then.. its dicey
time: 5 minute read
title: Are fantasy football rankings accurate?
tags: Tableau R regression sports web-scraping data-wrangling
dat: August 14, 2020
---
Fantasy football is huge. [About 50 million people play each year, and its now the number one marketing tool of the NFL](https://www.sportsbusinessdaily.com/Journal/Issues/2019/09/02/Media/Fantasy.aspx). Fantasy players are more engaged in the entire NFL and end up watching more football than typical fans.

The rise in popularity of fantasy football has generated an entire industry of fantasy analysis. There are an uncountable number of websites, forums, podcasts, and radio and TV shows devoted solely to fantasy football. And it seems that each unique site or show has its own weekly player rankings.

Rankings are everywhere, and I mean **everywhere**. Simply Google "fantasy football week 1 rankings" and you will see an endless list of websites offering rankings. Search the same phrase in Twitter and the result will be similar - an endless list of unknown individuals, each with their own unique player rankings.

When you first start playing fantasy, [all these rankings start to make you feel a bit like the Grinch](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiP4PbimJnrAhWTGc0KHRXKAsAQyCkwAHoECAwQBA&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DKUg5UTC3x3A&usg=AOvVaw2yL0QTPZAruVYGfbUyxsle). Only, instead of hating noise, *noise*, **noise**, you hate rankings.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/grinch.jpg" />
</p>
<div align="center"><em>When you are scrambling to find a wide receiver five minutes before kickoff in the Thursday night game.</em></div>

<br>

### What are fantasy football rankings?
***

Rankings are simply a list of players in a position ranked by their predicted performance in the coming week of play. Experts (and random people on twitter) rank each player based on their past performance and the upcoming matchup against the defense of an opposing team. Sophisticated experts also take into account variables like home or away games, weather, and historical rivalries.

*In theory*, all of this information is condensed down to one dimension - a ranked list of players to help fantasy team owners pick their lineup and manage their roster. In some cases, fantasy team owners even pay for access to proprietary rankings, thinking expensive rankings will give them the edge to win their league.

But *In practice*, are all of these rankings really worth anything?

<br>

### How do you measure the accuracy of rankings?
***

To measure ranking accuracy, I scraped weekly rankings for each player in each position from the 2019 season and compared them the fantasy football points scored in the same week. Since there are *so many* rankings to choose from, I chose the [Expert Consensus Rankings from Fantasy Pros](https://www.fantasypros.com/about/faq/football-inseason-accuracy-methodology/). These rankings are the averaged ranks of experts, who are chosen weekly based on their accuracy in predicting previous weeks. **In short, these are the most accurate rankings fantasy players can get**.

<br>

### How accurate are fantasy football rankings?
***

**As it turns out, fantasy football rankings are not very accurate at all**. In most cases, a player has the same probability of scoring as many fantasy points as another player ranked 10 to 30 places lower.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/ff.jpg" />
</p>
<div align="center"><em>Fantasy football rankings vs. fantasy points by player position for the 2019 season.</em></div>

<br>

Each graph has a line indicating the relationship between ranking and fantasy points. There is a real relationship there. However, the variability is so high that, in most cases, the relationships are not useful. For example, rankings can only explain about 2% of the variability in fantasy points in kickers.

Across all positions, rankings can only really explain 14% of the variation in weekly fantasy points. Meaning, **rankings have very, very little power in predicting how many fantasy points a player will score**.

The one exception to this was running backs. Running back rankings were able to predict fantasy points about two times better than the average position. But even then, rankings only explain 32% of the variation in fantasy points. 

Also interesting, a curved line fit the running back rankings best. That means, among top-tiered running backs (ranked 1 to 30), differences in ranks will lead to bigger differences in scoring. So, if you are choosing between a rank two and rank ten running back, the rank two is more likely to score more points. However, if you are choosing between a rank 52 and rank 60, the probability that the rank 52 will score more points is much lower.

Still, even in the case of running backs, rankings did not accurately predict fantasy points.

<br>

### Should you be using rankings to pick your lineup?
***

Even ranking experts acknowledge rankings should be used as a guide. [In a recent article on a prominent fantasy football site](https://www.rotoballer.com/michael-florios-2020-fantasy-football-rankings/752030), football commentator Mike Florio wrote 

>the mistake so many fantasy players make is treating rankings like an 'end-all-be-all' rather than using them as a guide. That is all they really are. The next step is learning how to properly use that guide...that's what I'm here for." 

But the articles doesn't really explain how to use his rankings as a guide. There are some fantasy buzzwords like "safe players" and "upside", but no real breakdown of how to properly use rankings.

In the end, maybe that is all rankings are? Fodder for the endless number of outlets offering fantasy analysis. Perhaps rankings are how these outlets signal to readers and listeners that they are experts? But now you know better.

**If you really need help with your lineup this year, try using projections instead of rankings**. [Projections have been shown to be considerably more accurate than rankings](https://fantasyfootballanalytics.net/2016/04/accuracy-of-rankings-vs-projections.html).

<br>

**More on fantasy football rankings**
 - [Fantasy Football: Understanding the Difference Between Rankings and Projections](https://bleacherreport.com/articles/1272428-fantasy-football-understanding-the-difference-between-rankings-and-projections)

 - [Custom Fantasy Football Rankings and Projections for Your League with this App](https://fantasyfootballanalytics.net/2014/06/custom-rankings-and-projections-for-your-league.html)

<br>

*Data sources*: 
 - *Fantasy football points for the 2019 season in a standard scoring Yahoo league from [Fantasy Pros](https://www.fantasypros.com/nfl/stats/qb.php?ownership=y&range=full)*. 
 - *Fantasy football Expert Consensus Rankings from Fantasy Pros for the 2019 season in a standard scoring league, scraped from [weekly rankings articles](https://www.fantasypros.com/2019/09/mike-taglieres-week-1-fantasy-football-rankings-2019/) and aggregated by the author*

*Data and R code available on [GitHub](https://github.com/waltscience/ffrankings)*
<br>

{% include twitter_card.html %}
