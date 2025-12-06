---
layout: post
title: Comparative Politics - Duverger's Law
permalink: /comparativepolitics/
---

- [Case Studies](#case-studies)
  - [FPTP: United Kingdom](#fptp-united-kingdom)
  - [Modified PR: Japan](#modified-pr-japan)
  - [PR: Belgium](#pr-belgium)


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

There are <a href = 'https://www.britannica.com/question/How-many-political-parties-are-there-in-the-U-K'> thirteen </a> parties represented in Parliament as of 2025. However, the UK has an ENP of 3.24. The main parties represented in Parliament are the Labour Party (center-left, 404 MPs), The Conservative "Tory" Party (center-right, 119 MPs), and the Liberal Democrats (center-left, 72 MPs). 

The structure of FPTP favors parties with strong geographical support, as parties need a majority in each local constituency to get MPs. As a result, we see two major parties UK-wide and quite a few local/nationalist parties that have geographical strongholds. Examples of the latter include Sinn Féin (Irish republican and democratic socialist), Plaid Cymru (Welsh nationalist), and the Scottish National Party (Socttish nationalist).[^2] 

Below is a slideshow[^3] displaying the share of seats in Parliament in different years. Click the upper two arrows to freely toggle back and forth; click the middle button to have it play for you.

<iframe scrolling = 'no' sandbox="allow-same-origin allow-forms allow-scripts allow-downloads allow-popups allow-popups-to-escape-sandbox allow-top-navigation-by-user-activation" src = 'https://flo.uri.sh/story/163875/embed?auto=1' width="100%" height="668px" frameborder="0" style="border:1" allowfullscreen></iframe>

## Modified PR: Japan

Japan's legislature is the National Diet, which consists of the upper House of Councillors and the lower House of Representatives. The House of Representatives uses a modified PR system to elect its members: 60% are elected via a FPTP system, and 40% are elected using a PR system in eleven regional blocs.[^4] 

Japan has an ENP of 3.72. Eleven parties are represented in the House of Representatives, but there are two main parties. As of October 6, 2025, the Liberal Democratic Party holds 196 seats, followed by the Constitutional Democratic Party of Japan (148 seats). Together, they constitute 73.98% of the House.[^5]

![Japanese House of Representatives Composition](/stuff%20included/images/comppoliticsjapan.png)

## PR: Belgium

Belgium was the first country in the world to adopt a PR system for national parliamentary elections in 1900. Belgium is divided into eleven electoral districts, and representation in the Chamber of Representatives (the lower house of the legislature) is proportional to each district's population. 

Belgium is split into four "linguistic regions" per its Constitution: the Dutch-speaking region in the north (Flanders), the French-speaking region in the south (Wallonia), the bilingual area of Brussels-Capital, and the German-speaking region in the east.[^6] Each language region has their own set of parties which speak that language: as a result, there's no national "Green" party, for example, but there's a Dutch-speaking Green party and a French-speaking Green party. As a result of both the language divide and the PR electoral system, parties abound.

| Political Ideology | Dutch-Speaking | Francophone |
|:--|:--| :--|
|Center-Left | Socialist Party Different (sp.a) | Socialist Party (PS)|
|Liberal| Open Flemish Liberals and Democrats | Mouvement Réformateur|
|Green| |Groen | Écolo|
|Christian Democratic | Christian Democratic and Flemish | Humanist Democratic Center|
| | New Flemish Alliance | Democratic Federalist Independent | 
|| Flemish Interest | Workers' Party

Belgium has an ENP of 10.97. Sixteen parties ended up winning seats in the Chamber of Representatives in the 2024 election. Leading the pack was the New Flemish Alliance (right-wing, 24 MPs), the Vlaams Belang (far-right, 20 MPs), and the Mouvement Réformateur (liberal, 20 MPs).The government must be supported by an absolute majority, or at least 76 MPs. After the 2024 election, it took eight months for a five-party coalition to gain an absolute majority with 81 seats.[^7]

---

[^1]: Armingeon, Klaus, Sarah Engler, Lucas Leemann and David Weisstanner. 2025. *Comparative Political Data Set 1960-2023.* Zurich/Lueneburg/Lucerne: University of Zurich, Leuphana University Lueneburg, and University of Lucerne.

[^2]: "United Kingdom: Political parties at a glance." *PolitPro*, accessed Dec. 5, 2025. <a href = 'https://politpro.eu/en/united-kingdom/parties#parties-in-comparison'>'https://politpro.eu/en/united-kingdom/parties#parties-in-comparison</a>

[^3]: This lovely slideshow was taken from the <a href= 'https://electoral-reform.org.uk/voting-systems/types-of-voting-system/first-past-the-post/'> Electoral Reform Society</a>. It was made with <a href = 'https://flourish.studio/product/data-storytelling/?utm_source=showcase&utm_campaign=story/163875'>Flourish</a>. 

[^4]: Matthew Mathias. "How do elections work in Japan," *Electoral Reform Society*, Sep. 19, 2019. https://electoral-reform.org.uk/how-do-elections-work-in-japan/

[^5]: "Strength of the In-House Groups in the House of Representatives." *The House of Representatives, Japan*. https://www.shugiin.go.jp/internet/itdb_english.nsf/html/statics/english/strength.htm

[^6]: "Four language areas." Parlament der Deutschprachigen Gemeinschaft Belgiens. https://pdg.be/en/desktopdefault.aspx/tabid-3986/7167_read-41451/

[^7]: "IPU data on Belgium, House of Representatives." *IPU Parline*. Accessed Dec. 5, 2025, https://data.ipu.org/parliament/BE/BE-LC01/election/BE-LC01-E20240609/