---
layout: post
image: /images/pasta.jpg
page.image: /images/pasta.jpg
summary: Yes, we spend more on groceries, online shopping, and maybe pasta machines.
excerpt: Yes, we spend more on groceries, online shopping, and maybe pasta machines.
time: 3 minute read
title: As our economy hits an unprecedented low, are we changing the way we spend?
tags: Tableau R Shiny regression economics politics
dat: August 8, 2020
---
The [U.S. Gross Domestic Product (GDP)](https://en.wikipedia.org/wiki/Gross_domestic_product) dropped by 33% in the second quarter of 2020. The drop was the most drastic ever. **Seriously**. [Ever](https://www.npr.org/sections/coronavirus-live-updates/2020/07/30/896714437/3-months-of-hell-u-s-economys-worst-quarter-ever).

How much we spend on goods and services is a huge factor in calculating GDP. And while it might be obvious that Americans are spending less money on restaurants and bars, I wondered whether we were spending that money somewhere else?

I got a little curious about spending a few nights ago while I was unboxing my brand-new pasta machine that I bought online. Yep, I splurged on a gadget that has taken my culinary game to a new level. And by looking at the data, you probably have too.

<br>

<p align="center">
  <img src="{{ site.baseurl }}/images/pasta.jpg" />
</p>
<div align="center"><em>Pasta machine cutting some fettuccini. Or maybe its tagliatelle? Lasagnette?</em></div>

<br>

### How do you measure spending in the U.S. economy?
***

I grabbed data from the U.S. Census Bureau's Monthly Retail Trade database. This database includes monthly retail sales, broken down by retail sector.

I measured differences in actual vs. projected spending in each retail sector from March through June, 2020. To estimate projected spending, I built linear models of spending from February through December 2019. Then I calculated the cumulative difference in projected vs. annual spending from March through June in each retail sector. 

<br>

### Where are we spending our money?
***

My hunch that I might not be the only person using an online shop to up my culinary game was right. **Grocery store sales have increased by about 15% since the beginning of March - an increase of more than 34.5 billion dollars.**

Over the same time period, **Non-store and online retail sales spiked by about 14%, or 38.5 billion dollars**. My beautiful, Amazon delivered pasta machine is starting to make sense.

Our new focus on cooking might also explain the rise in chefs streaming from home, like the amazing baking videos from [Christina Tosi on Instagram](https://www.instagram.com/christinatosi/?hl=en). 

<br>

<iframe src="https://public.tableau.com/views/pctchangesales/Sheet1?:showVizHome=no&:embed=true" width="100%" height="500"></iframe>
<div align="center"><em>Percent difference in projected vs actual spending in retail sectors since February 2020. Hover, click, or tap on bars to see differences in dollars spent. Note to mobile users - turn your device sideways for a better view.</em></div>

<br>

In addition to groceries and online shopping, we are also spending more on building materials and garden supplies, and a bit more in general merchandise stores (like Target and Walmart).

But where have we spent less? **Clothing and accessories. This sector decreased by more than 55%, dropping about 49 billion dollars in sales since the beginning of March.** The second largest decline in spending is in food service and drinking places. Together, this sector lost more than 38% of its sales - over 100 billion dollars.

The remaining retail sectors all lost sales since the beginning of March. 

<br>

### How massive are these changes in spending?
***

I have thought about how to convey the magnitude of spending changes. A 55%, 49 billion dollar decline in clothing sales - how big is that? I am not sure the numbers alone can convince us of what is happening right now in the economy.

Simply looking at the data might actually be the best way to undertand how massive these spending changes are. So I have made an interactive graph to explore retail sales data since 1992. 

**Click through some of the sectors and play with the year slider on the graph below to get a feel for the unprecedented change in the economy**.

<br>

<iframe src="https://waltscience.shinyapps.io/shinymrt/" width="100%" height="730px"></iframe>

### What does the future hold for the GDP?
***

Unfortunately, retail data isn't very useful for forecasting future GDP in a pandemic. But we don't need forecasting to know the outlook isn't great.

Some economists have argued [enhanced unemployment benefits and social safety net programs kept the GDP from falling even further in the second quarter](https://www.cnbc.com/2020/07/10/unemployment-boosts-will-help-recovery-more-than-new-stimulus-checks.html). Many of those benefits expired on July 31st. 

Others argue [new funding should focus on the states and municipalities](https://www.forbes.com/sites/lizfarmer/2020/07/30/bailout-stimulus-federal-relief-recovery/#6fbc9e895678) facing enormous revenue shortfalls. Yet, there seems to be little desire to grant federal stimulus money to states.

In any case, [an unprecedented, unheard-of, unimaginable portion of our economy is being kept afloat right now by a firehose of U.S. aid aimed at corporations and citizens](https://www.barrons.com/articles/for-the-first-time-ever-uncle-sams-aid-to-u-s-tops-quarterly-gdp-51596244795). As the government begins to close the tap, *the economy will start to sink*.

**Until then, I'll keep trying to perfect homemade pasta - at least *it* floats when its done cooking**.

<br>

**More opinion on the GDP**
 - [Did a third of the economy really vanish in just three months?](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=newssearch&cd=&ved=0ahUKEwj6zp2R0oDrAhXSKM0KHeJ4BuQ4ChDF9AEINDAB&url=https%3A%2F%2Fwww.washingtonpost.com%2Fbusiness%2F2020%2F07%2F30%2Fdid-third-economy-really-vanish-just-three-months%2F&usg=AOvVaw2Ox_VV98LJQnNtomgiq_0Q)

 - [Ignore GDP Plunging 33%. Pay Attention To The 9.5% Decline](https://www.forbes.com/sites/chuckjones/2020/07/31/ignore-gdp-plunging-33-pay-attention-to-the-95-decline/#635c4c9f2640)

<br>

*Retail sales data source: U.S. Census Bureau Monthly Retail Trade database, 1992-2020.*

*Data and R code available on [GitHub](https://github.com/waltscience/retailspending)*
<br>

{% include twitter_card.html %}
