---
layout: post
title: Comparative Politics - Duverger's Law
permalink: /comparativepolitics/
---
<b>Duverger's Law</b> holds that the simple-majority single ballot system (FPTP) favors the two party system. When voters go to the polls and vote strategically, a FPTP system incentivizes them not to select minority parties which will never be able to reach a plurality. This project seeks to check if Duverger's Law holds up when applied to empirical data.

I am using the <b>Comparative Political Data Set (CPDS)</b>,[^1] which contains annual data for thirty-six democratic countries. The dataset covers the range 1960-2023 (or, if the country transitioned to democracy after 1960, starts in the transition year). 

For this project, I looked only at data collected in 2023. The countries covered are below:

<img src = '/stuff%20included/images/cp.repregions.png' alt = 'Global map depicting countries in Northern, Western, Southern, and Eastern Europe; Eastern and Western Asia; Northern America; and Australia and New Zealand.'>

<div id="contentBox" style="margin:3px auto; width:100%">
    <div id="column1" style="float:left; margin:0px; width:50%;">
     <b>Australia and New Zealand</b>: Australia, New Zealand <br><br>
     <b> Northern America</b>: Canada, USA <br><br>
     <b>Western Asia</b>: Cyprus <br><br>
     <b>Eastern Asia</b>: Japan <br><br>
    </div>
    <div id="column2" style="float:left; margin:0px;width:50%;">
     <b>Western Europe</b>: Austria, Belgium, France, Germany, Luxembourg, Netherlands, Switzerland<br><br>
     <b>Eastern Europe</b>: Bulgaria, Czech Republic, Hungary, Poland, Romania, Slovakia<br><br>
     <b>Northern Europe</b>: Denmark, Estonia, Finland, Ireland, Iceland, Latvia, Lithuania, Norway, Sweden, UK<br><br>
     <b>Southern Europe</b>: Croatia, Greece, Italy, Malta, Portugal, Slovenia, Spain<br><br>
    </div>
</div>

Countries were grouped into "subregions" by coders at <a href = 'https://www.naturalearthdata.com/'>Natural Earth</a>. 

## Duverger's Law

Do countries using FPTP have a smaller number of effective parties than those that use proportional representation systems? I put that to the test by classifying each country according to their electoral systems and color coding them by the number of electoral effective parties (Electoral ENP). Electoral ENP is calculated by:

<ol> 
    <li> Calculating $$
r = 1 - \sum_{i=1}^{m} v_i^2
$$

where \(v_i\) is the share of votes for each party \(i\) and \(m\) is the number of parties. Subtracting the sum of squared shares from 1 gives us a measure of fractionalization.</li>

    <li> Calculating $$ ENP = \frac{1}{1-r}$$ </li>
</ol>


 <iframe src="/stuff%20included/html/effpar_elemap.html" width="100%" height="500px" frameborder="0" style="border:0" allowfullscreen></iframe>

One finds that European countries tend to have higher ENP measures, and that more European countries use proportional representation voting systems. The U.S., U.K., and Canada are the only countries classified as using FPTP systems, and have the lowest ENP measures. Countries noted to use "modified PR" systems (e.g. Australia,  France, Japan) have ENP measures between that of the PR-system countries and that of the FPTP-system countries. Overall, Duverger's Law holds.

## Duverger's Hypothesis

[^1]:Armingeon, Klaus, Sarah Engler, Lucas Leemann and David Weisstanner. 2025. <i>Comparative Political Data Set 1960-2023.</i> Zurich/Lueneburg/Lucerne: University of Zurich, Leuphana University Lueneburg, and University of Lucerne.
