---
layout: post
title: Comparative Politics - Duverger's Law
permalink: /comparativepolitics/
---
<strong>Duverger's Law</strong> holds that the simple-majority single ballot system (FPTP) favors the two party system. When voters go to the polls and vote strategically, a FPTP system incentivizes them not to select minority parties which will never be able to reach a plurality. This project seeks to check if Duverger's Law holds up when applied to empirical data.

I am using the <strong>Comparative Political Data Set (CPDS)</strong>,[^1] which contains annual data for thirty-six democratic countries. The dataset covers the range 1960-2023 (or, if the country transitioned to democracy after 1960, starts in the transition year). 

For this project, I looked only at data collected in 2023. The countries covered are below:

<img src = '/stuff%20included/images/cp.repregions.png' alt = 'Global map depicting countries in Northern, Western, Southern, and Eastern Europe; Eastern and Western Asia; Northern America; and Australia and New Zealand.'>


|Region|Countries|
|:---|:---|
|**Australia and New Zealand** | Australia, New Zealand|
|**Northern America**| Canada, USA|
|**Western Asia**| Cyprus|
|**Eastern Asia**:|Japan | 
|**Western Europe**| Austria, Belgium, France, Germany, Luxembourg, Netherlands, Switzerland|
|**Eastern Europe**| Bulgaria, Czech Republic, Hungary, Poland, Romania, Slovakia|
|**Northern Europe**| Denmark, Estonia, Finland, Ireland, Iceland, Latvia, Lithuania, Norway, Sweden, UK
|**Southern Europe**| Croatia, Greece, Italy, Malta, Portugal, Slovenia, Spain |

Countries were grouped into "subregions" by coders at <a href = 'https://www.naturalearthdata.com/'>Natural Earth</a>. 

## Duverger's Law

Do countries using FPTP have a smaller number of effective parties than those that use proportional representation systems? I put that to the test by classifying each country according to their electoral systems and color coding them by the number of electoral effective parties (Electoral ENP). Electoral ENP is calculated by:

<ol> 
    <li> Calculating $$
r = 1 - \sum_{i=1}^{m} v_i^2
$$

where $v_i$ is the share of votes for each party $i$ and $m$ is the number of parties. Subtracting the sum of squared shares from 1 gives us a measure of fractionalization.</li>
    <li>Calculating $$ ENP = \frac{1}{1-r}$$ </li>
</ol>


 <iframe src="/stuff%20included/html/effpar_elemap.html" width="100%" height="500px" frameborder="0" style="border:1" allowfullscreen></iframe>

One finds that European countries tend to have higher ENP measures, and that more European countries use proportional representation voting systems. The U.S., U.K., and Canada are the only countries classified as using FPTP systems, and have the lowest ENP measures. Countries noted to use "modified PR" systems (e.g. Australia, France, Japan) have ENP measures between that of the PR-system countries and that of the FPTP-system countries. Overall, Duverger's Law holds.


The CPDS also gives us data for the effective number of parties in the legislature. It's calculated in the same way as Electoral ENP, but it swaps $v_i$, a party's vote share in the election, for $s_i$, a party's share of votes in the legislature.


 <iframe src="/stuff%20included/html/effpar_legmap.html" width="100%" height="500px" frameborder="0" style="border:1" allowfullscreen></iframe>

Every country has a lower Electoral ENP than Legislative ENP. How strange! 

# Case Studies

Let's zoom in on three countries with different systems:
<ol>
    <li> FPTP: United Kingdom </li>
    <li> Modified PR: Japan </li>
    <li> PR: Belgium </li>
</ol>

## FPTP: United Kingdom

The United States and Canada based their election systems off of the UK's. The UK has 650 different constituencies which each use FPTP to elect a single MP to the House of Commons. FPTP is also used for local elections (councillors, parish and town council elections, police and crime commissioner elections...).

Below is a slideshow[^2] displaying the share of seats in Parliament in different years. Click the upper two arrows to freely toggle back and forth; click the middle button to have it play for you.
<iframe scrolling = 'no' sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation" src = 'https://flo.uri.sh/story/163875/embed?auto=1' width="100%" height="668px" frameborder="0" style="border:1" allowfullscreen></iframe>


[^1]: Armingeon, Klaus, Sarah Engler, Lucas Leemann and David Weisstanner. 2025. <i>Comparative Political Data Set 1960-2023.</i> Zurich/Lueneburg/Lucerne: University of Zurich, Leuphana University Lueneburg, and University of Lucerne.
[^2]: This lovely slideshow was taken from the <a href= 'https://electoral-reform.org.uk/voting-systems/types-of-voting-system/first-past-the-post/'> Electoral Reform Society</a>. It seems to have been made with Flourish. 
