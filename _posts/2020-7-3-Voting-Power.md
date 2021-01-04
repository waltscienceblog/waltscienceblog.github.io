---
layout: post
image: /images/Electoral_Map_States.png
page.image: /images/Electoral_Map_States.png
summary: Yes, because Americans don't actually vote for a president.
excerpt: Yes, because Americans don't actually vote for a president.
time: 3 minute read
title: Do some people have more power than others to elect a president?
tags: politics Tableau R regression
dat: July 3, 2020
---
Instead, they vote to determine how the actual people who vote for president should vote. If that sounds needlessly complicated, [it is.](https://www.history.com/news/the-history-of-the-electoral-college-debate)

The people that actually elect a president are called electors. All the electors together form the Electoral College. And each state is given a number of electors based on its population size.

![Electoral College Map]({{ site.baseurl }}/images/Electoral_Map_States.png "Electoral College Map")
<div align="center"><em>Electoral college votes by state</em></div>

<br>

### How does the Electoral College affect your power to elect a president?
***

To find out, I calculated the presidential voting power of each state. By dividing the number of presidential ballots cast by the number of electors in each state, I determined the number of ballots per elector. To calculate power, I then divided each states ballots per elector value by the average state ballots per elector.
 
The resulting number is the individual voting power for each state compared to the average person's voting power across all states.

<iframe src="https://public.tableau.com/views/PersonalVotingPowerMap/Map?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Individual voting power by state. Click or hover on a state to see its voting power compared to the average voter.</em></div>

<br>

The map shows people in certain states have much more power to elect a president. **One vote in Wyoming is about 260% more powerful than the average voter. But one vote in Florida only has 68% the power of an average vote.**

<br>

### Does having more voting power lead to more voting?
***

To answer this, I calculated the potential voting power of each state if all eligible voters voted. There is no relationship between potential voting power and voter turnout.

<iframe src="https://public.tableau.com/views/Percentvs_Potential/Sheet2?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Potential individual voting power by state. The power a voter in a state has if every elegible voter voted.</em></div>

<br>

Hawaii and West Virginia are the states with the lowest voter turnout in the nation. But they both have more potential voting power than the average voter. What is going on here?

[An NPR story interviewing West Virginians in 2018](https://www.npr.org/2018/09/10/646422511/what-some-west-virginia-residents-have-to-say-on-why-they-dont-vote) suggests voters there simply think their vote doesn't matter.

<iframe src="https://www.npr.org/player/embed/646422511/646422512" width="100%" height="290" frameborder="0" scrolling="no" title="NPR embedded audio player"></iframe>
>Because we don't matter. We're so small. It really don't matter. I mean, literally look. You look up and down the streets. There's nobody. - Brittany Jenkins, West Virginian

But your vote does matter Brittany, *it does*. It matters more than mine and more than most Americans.

<br>

### How has the Electoral College affected elections?
***

One way to answer this question is to count the times the Electoral College has diverged from the popular vote. Five presidents have won the election but lost the popular vote:

 - John Adams (1824)
 - Rutherford Hayes (1876)
 - Benjamin Harrison (1888)
 - George W. Bush (2000)
 - Donald Trump (2016)

Among 45 presidents, that means about **1 out of every 10 presidents was elected by losing the popular vote but winning the most electors**.

<br>

### Is the Electoral College anti-democratic?
***

I have shown that each person's vote is not equal in presidential elections. Whether or not this misappropriation of power is anti-democratic depends on your idea of democracy.

It might also depend on what year you were asked.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">The electoral college is a disaster for a democracy.</p>&mdash; Donald J. Trump (@realDonaldTrump) <a href="https://twitter.com/realDonaldTrump/status/266038556504494082?ref_src=twsrc%5Etfw">November 7, 2012</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<br>

**More on the Electoral College**
 - [Five common misconceptions about the Electoral College](https://www.theatlantic.com/ideas/archive/2019/11/five-common-misconceptions-about-electoral-college/602596/)

 - [Supreme Court weighs whether Electoral College members must stick to state's Popular Vote](https://www.wsj.com/articles/supreme-court-to-weigh-whether-electoral-college-members-must-stick-to-states-popular-vote-11589362201)

<br>

*Election data source: [United States Election Project](http://www.electproject.org)*

*Data available on [GitHub](https://github.com/waltscience/votepower)*
<br>

{% include twitter_card.html %}
