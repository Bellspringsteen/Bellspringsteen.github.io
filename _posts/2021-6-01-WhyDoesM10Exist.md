---
layout: portfolio_entry
title: Why does the M10 Bus Exist?
tags:
visible: 1
---

## Evaluating bus routes in NYC based on Google Maps directions

### Intro:

I noticed that Google Maps never recommends I take the bus. Is it because I live and work in areas that are close to subway lines? In a constrained and existing system, how should we think about allocating transit routes? In this post I look at using Google Maps directions as a tool for detecting overlapping service and for doing transit planning. 

### Brief History of NYC Transit:

Wikipedia has amazingly detailed articles (<a href="https://en.wikipedia.org/wiki/History_of_transportation_in_New_York_City">here</a> and <a href="https://en.wikipedia.org/wiki/History_of_the_New_York_City_Subway">here</a>) which detail the history of transit in NYC. Present day NYC shows its history in its design; Broadway follows a Lenape route and numbered and lettered subway trains are of <a href="https://en.wikipedia.org/wiki/New_York_City_Subway_rolling_stock">different incompatible widths</a> because of their separate histories. Throughout NYC transit history there is dual control between government and private companies. <a href="https://en.wikipedia.org/wiki/New_York_and_Harlem_Railroad">The New York and Harlem Railroad </a> was the world's first street railway and was privately funded and designed but with governmental approval. In 1894 the Board of Rapid Transit Railroad Commissioners laid out routes and franchised to private companies. For busses, the <a href="https://en.wikipedia.org/wiki/Fifth_Avenue_Coach_Company"> Fifth Avenue Coach Company </a> and its <a href="https://en.wikipedia.org/wiki/Fifth_Avenue_Transportation_Company"> predecessor </a> appear to be the first bus-like transportation in the city starting in 1885 and running along 5th avenue. The bus companies appear to have proposed routes in applications for franchises to the city which were <a href="https://web.archive.org/web/20210323214738/http://www.coachbuilt.com/bui/f/fifth_avenue/fifth_avenue.htm"> changed or granted based on other transit routes</a>, backroom dealing, and corruption. The history up until the middle of the 20th century is marked by competition from different types of transit and different companies with tradeoffs in routes, fares, and travel times. But by the 1960’s the city was on its way towards complete public control through the <a href="https://en.wikipedia.org/wiki/Metropolitan_Transportation_Authority"> MTA</a>.

Currently the MTA is in the midst of a <a href="https://web.archive.org/web/20210430222201/https://new.mta.info/system_modernization/bus_network/about"> periodic bus redesign </a> however strangely the MTA bus redesign does not mention subway trains. Currently the Bronx bus network has been redesigned with the other boroughs plans ongoing. In the <a href="https://www.youtube.com/watch?v=9AqNRgMxbPE&ab_channel=mtainfo">MTA video</a> a very manual process is described that doesn't seem to take into account the obvious, the subway, or the tradeoffs in dollars spent which all seems very strange considering the agency's financial situation. 

The MTA’s mission statement says “The Metropolitan Transportation Authority (MTA) preserves and enhances the quality of life and economic health of the region it serves through the cost-efficient provision of safe, on-time, reliable, and clean transportation services.” I would simplify it to say “ The goal of the MTA is to improve the quality of life and economic health of the region by expanding access to low cost and fast transit evenly throughout the region” and the first step is to reconsider the bus redesign to emphasize multimodal transit time across the whole region and lower cost. 
 
### Google Maps as a Tool:

I am a lifelong New Yorker and remember the days of tokens and paper maps. But for me and I would guess many New Yorkers, Google Maps and other automated trip planners are how we pick transit routes. 

I created a program to randomly generate 10 thousand pairs of points in NYC: hypothetical start and end points for a trip. The pairs vary in how far apart they are. Some pairs are across the city from each other, others both in the same borough, and others within the same 3 mile radius. 


<br>
<div style="text-align:center"><img src ="../../img/m10_1.png" /> </div>
<div style="text-align:center">Fig 1- 10k pairs of points </div>
<br>

With these 10 thousands points, I queried the <a href="https://developers.google.com/maps/documentation/directions/overview"> Google Directions API </a> which is the trip planner used by Google Maps for directions. I simulated traveling between the two points on a weekday morning.  

For the below map, I went through all the trips and looked for cases where the bus was more than 5 minutes quicker than any other public transit option. In these cases, I mapped the bus route. The more trips the darker the route. Under this thought experiment, if all riders were able bodied and optimized for transit time only, you could remove all bus lines besides those shown and you would not increase the transit time of any commuters.

<br>
<div style="text-align:center"><img src ="../../img/m10_2.png" /> </div>
<div style="text-align:center">Fig 2- All Bus Routes</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/m10_3.png" /> </div>
<div style="text-align:center">Fig 3- Bus Routes needed when optimizing for transit times</div>
<br>

<b> The majority of bus lines in Manhattan are gone. </b> This represents hundreds of millions of dollars that a cash strapped transit agency is spending on potentially unneeded bus lines. As you would expect, the crosstown bus lines in Manhattan would remain. As would the majority of the bus lines on 1st, 3rd, Madison and 5th where there is less train access. 


<br>
<div style="text-align:center"><img src ="../../img/m10_4.png" /> </div>
<div style="text-align:center">Fig 4- Lower Manhattan</div>
<br>

## M10 and specific examples:

Let's look at the M10 Bus as an example. You can see via the <a href="https://new.mta.info/map/5391"> NYC bus map </a> that the M10 Bus goes from Columbus Circle up CPW/FDB to 155th. Along the majority of its length it is directly above the A,B,C,D trains. Above 121st it's a block away from the same train lines. And if we look at the map generated from Google Maps directions, the M10 is never recommended. Looking at <a href="https://new.mta.info/agency/new-york-city-transit/subway-bus-ridership-2019"> 2019 NYC MTA ridership </a> we see an average weekday ridership for the M10 of only 5k weekly riders with ridership decreasing 15% from 2018 to 2019. 

<br>
<div style="text-align:center"><img src ="../../img/m10_5.png" /> </div>
<div style="text-align:center">Fig 5 - current M10 route vs route gone on transit time map</div>
<br>

The story is similar for many other bus lines that run for their majority along major subway lines for instance the BX1/2 which besides small portions in kingsbridge and mott haven travels along the same line as the B/D on the grand concourse in the bronx. Or the B25 in Brooklyn which runs along the A/C except for a small portion in dumbo. 

<br>
<div style="text-align:center"><img src ="../../img/m10_6.png" /> </div>
<div style="text-align:center">Fig 6 - B25 redundant along A/C line</div>
<br>

We can see the importance and the need for more busses when we look at areas with few subway options. For instance in the Bronx, the highest ridership is the Bx12 which travels east to west providing indispensable transportation. Or the Brooklyn B82 which is similarly important.

<br>
<div style="text-align:center"><img src ="../../img/m10_7.png" /> </div>
<div style="text-align:center">Fig 7- Bx12 providing east-west transit</div>
<br>

There is a clear need for more busses in outer boroughs where the current transit density is poor and most likely causally the housing is also less dense. 

<br>
<div style="text-align:center"><img src ="../../img/m10_8.png" /> </div>
<div style="text-align:center">Bronx</div>
<br>


<br>
<div style="text-align:center"><img src ="../../img/m10_9.png" /> </div>
<div style="text-align:center">Brooklyn</div>
<br>


<br>
<div style="text-align:center"><img src ="../../img/m10_10.png" /> </div>
<div style="text-align:center">Queens</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/m10_11.png" /> </div>
<div style="text-align:center">Central Park</div>
<br>


<br>
<div style="text-align:center"><img src ="../../img/m10_12.png" /> </div>
<div style="text-align:center">Upper Manhattan</div>
<br>

## How would you redesign a bus system?

As stated in the introduction I would suggest the goals for the transit system should be to expand low cost transit throughout the region and lower transit times. 

Contrary to the MTA redesign website, “It all begins with wiping the slate clean and starting from scratch,” ignoring billions in existing infrastructure, commuter preference and history is a terrible way to start. <a href="https://softwareengineering.stackexchange.com/questions/6255/have-you-ever-been-involved-in-a-big-rewrite"> It reminds me of the famous software question of the big rewrite, do you rewriting everything or refactor. </a> Rarely if ever is the blank slate the starting point, instead you want to make thousands of small refactoring changes instead of decade long redesigns. 

The task of redesigning is as much a political question as it is a systems engineering question. Begging to consider tradeoffs and you are quickly considering racial, socioeconomic, age, environmental and more questions. Is this central planning? Is the redesign racist? Ageist? Disablism?

We have an imperfect transit system which amplifies the inequities of our society and history. To change it, create an open system with clear tradeoffs and iterate over a thousand small steps instead of giant leaps. 

In the literature I can already see some algorithmic approaches to bus map designs such as <a href="https://trid.trb.org/view/542792">here</a> and <a href="https://www.sciencedirect.com/science/article/abs/pii/S0191261514000812">here</a>. I would work to create an open algorithm which takes in a few inputs and uses a <a href="https://en.wikipedia.org/wiki/Mathematical_optimization">objective function </a> / <a href="https://en.wikipedia.org/wiki/Loss_function"> loss function</a>  to quantify each map against the prime goals of access to low cost transit and transit time. Researchers and interested individuals could iterate on the functions, inputs, and generated maps.

## Code

You can play with a version of the map
* Without a access key - https://blog.labsbell.com/bus/draw_map/index.html
* Or get a key here and then go to https://blog.labsbell.com/bus/draw_map/index.html?access_key=TYPEKEYHERE

<iframe src="https://blog.labsbell.com/bus/draw_map/index.html" width="100%" height="600"></iframe>

See code here <a href="https://github.com/Bellspringsteen/other.nyc/tree/master/bus-redraw"> https://github.com/Bellspringsteen/other.nyc/tree/master/bus-redraw </a>

# Extra Questions:

* I don't think you understand the purpose of the bus. Its for XYZ.

	I don't think I do. 

    Reading some random articles like <a href="https://www.businessinsider.com/why-nyc-buses-are-better-than-using-subway-system-2018-1">here</a> and <a href="https://www.nytimes.com/2020/07/06/nyregion/mta-buses-nyc-coronavirus.html">here</a> it seems that the bus is seen as a slower but more pleasant commute.  <b> But why would the MTA have two competing services covering the same route???!!!? <b>

    The MTA mission statement says “The Metropolitan Transportation Authority (MTA) preserves and enhances the quality of life and economic health of the region it serves through the cost-efficient provision of safe, on-time, reliable, and clean transportation services.”

    With limited resources, wouldn’t the quality of life and economic health be maximized by allocating busses to areas without trains? Creating routes across busses and subways that minimize the transportation time for the entire city? Shouldn’t there be more bus service in brooklyn, queens and the bronx areas that are underserved?

* Dont tools like remix.com already do this? 

    Not sure but their website doesnt suggest they do. The websites seem to show a manual flow where planners draw maps and estimate usage based on demographics. I see no page that for instance says “ v2 reduces average transit time for your commuters by 12seconds but increases average distance walked by 12 feet” which is what i would expect to see.

* You’re proposing taking away services, and in particular, services in wealthy areas of the city like Central Park West, where the M10 runs! Won’t that be hard, politically? 

	Yes. Change is hard. 

* If you have lots of small changes they all have to be approved by city government and community boards vs a single large plan.

    Yes but the hope would be that the city would get used to thousands of small changes and each change would be less of a fight. Especially if it were more clear what tradeoffs were being made and the reason for decisions. 

* Should time be the only thing considered? 

    In <a href="http://web.mta.info/mta/planning/data/MTA%20NYC%20Travel%20Survey%20Final%20Report.pdf">MTA Survey Report </a> we can see that the #1 reason (more than double the second reason) for not taking transit is transit time. Transit time is how people choose transportation. There are of course other considerations, but in terms of planning a transit system I believe transit time far outweighs any other optimization. 


* If you select “optimize for fewer transfers” or “optimize for less walking” then what happens?

    I hope to do this in part 2, but I expect it increases the number of bus routes recommended. The question is how should a transit system allocate resources? Should it allocate resources to decrease the transit time of some commuters or provide an equivalent time route but with less walking for others? I would argue we should optimize for the transit time of the greatest number of people. 


* What happens if you run with “wheelchair accessible” 
    The google maps api https://developers.google.com/maps/documentation/directions/get-directions does not give accessibility as a query option.


* Shouldn’t you generate points based on demographics or density instead of random?

    Yes, and I might work on that. However, that opens up the question of if the system your building is just reinforcing the current state of the distribution of people. I would posit that lack of public transportation is a barrier to increasing density in many areas of NYC. 


* Can’t you use cellphone data or FOIA the MTA for a list of requests to its trip planning software in order to get real world trips?

    Yes, good idea. 


* You only searched weekday during the day, what about 3 am or the weekend?

    I wanted to focus on when ridership is highest and also when the MTA spends the most money. 


* Google Maps is using the MTA scheduled train data but the schedule is always wrong.

    Yes, but it's still a good description of the frequency of trains and buses even if it's not great at arrival times. The frequency of trains or buses is what matters for this project not really the exact arrival times. 


* People prefer the bus over the subway because the subway is dangerous, dirty or loud. 

    I don’t see convincing data that the subway is more dangerous than the bus. It's also not a very high reason in MTA user studies for why people don't take transit. Lastly, in a resource constrained system should dollars be allocated for more pleasant rides for some people or minimum transit times?
 
* The bus is a lifeline for people who are ambulatory disabled.

    The MTA has conducted user surveys such as <a href="http://web.mta.info/mta/planning/data-nyc-travel.html#">here</a> which is summarized <a href="http://blog.tstc.org/2014/04/11/nyc-bus-riders-tend-to-be-older-and-poorer-than-subway-riders/">here</a>. In the 2018 MTA survey of 30k transit users, less than 5% of respondents reported having an ambulatory disability. Unfortunately in the survey I could not determine the ambulatory disability status of bus riders versus subway riders and could not look at which specific bus routes are important to those with ambulatory disabilities. 

    Although it is not clear from the MTA survey data, it does anecdotally appear that the bus is important for the ambulatory disabled. If the MTA was better able to clarify what percentage of the bus riders were disabled, then a better accounting could take place. For instance if it could be determined what percentage of the 5k weekly riders on the M10 were disabled, it would be possible to evaluate the cost of that bus route against other options, like Access-A-Ride or improving subway station accessibility. My guess would be that investments in increasing the accessibility of subway stations would greatly decrease the transit times of people with ambulatory disabilities and further remove the need for some bus lines. 


* It's our history! A bus has always run on the M10 route.

    True, the history of M10 https://en.wikipedia.org/wiki/M10_and_M20_buses is interesting and shows a version of the bus route existing years before the subway. It also makes sense that private companies kept the bus route as a competitive alternative to the subway. When the subway and bus were consolidated under the MTA, the competition should have disappeared and bus routes should have optimized for transit time.


* Why didn't you embed the Google Map so we can play with the data? Why didn’t you query more than 10k routes?

	Because Google charges for that.


* Transferring from bus to subway to bus wastes time or is a pain/cognitive load.

    The directions take into account walking and waiting.


* Google algorithm is wrong, its faster to do X. 

	I don't think so. Try both methods with a stopwatch. 

* If I transfer, I might lose my seat. On the bus I always get a seat. 

    In a resource constrained system, should dollars be spent on comfort for some or minimizing transit times?

* If you remove busses more people will drive.

    Most of these areas with subway lines are high congestion areas and hence the cost of driving and parking would be very high. With congestion pricing coming to NYC the price will rise higher. Looking at NYC car ownership and usage, the highest amount of driving is in areas with poor transit options, by re-allocating bus service to these areas overall driving should decrease.

* Where is Staten Island in the data?

    I didn't include Staten Island as the relative scarcity of subways makes it less interesting for this investigation.

