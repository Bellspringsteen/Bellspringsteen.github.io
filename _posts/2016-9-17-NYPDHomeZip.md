---
layout: portfolio_entry
title: Your neighborhood NYPD officer isn't likely to be your neighbor
description: Interactive plots for NYPD Officer residence Zip Locations. Click on your home precinct and see where the cops in your neighborhood reside.
twitterimage: http://blog.labsbell.com/foil/NYPDHomeZip/resources/img/screenshot.png
tags: FOIL
visible: 1
---


The NYPD Patrol Guide states that officers must "live in one of the city’s five boroughs or Nassau, Suffolk, Rockland, Westchester, Putnam or Orange counties." 

Why do residency requirements exist?

	* http://www.gothamgazette.com/index.php/development/3218-residency-requirements
	* http://fivethirtyeight.com/datalab/most-police-dont-live-in-the-cities-they-serve/

I was curious where within the allowed counties most officers live, and curious if there are any exceptions to the rule. Using personnel data provided by the NYPD (see below for details on how the data was obtained), I found the following:

* 58% of NYPD Officers live in NYC 
	* 17% of NYPD officers live in Queens	
	* 16% of NYPD officers live in Brooklyn
	* 11% of NYPD officers live in The Bronx 
	* 10% of NYPD officers live in Staten Island
	* 4% of NYPD officers live in Manhattan
* 26% of NYPD officers live in Long Island (Nassau or Suffolk County)
* 13% of NYPD officers live in Approved Upstate NY Counties (Rockland,Westchester,Putnam, or Orange County)

Less than 1% live in, I guess, specially approved non-standard counties.


The Patrol Guide also states that officers can't live in the same zip code they work in. However, I found that 4% of NYPD officers live and serve in the same zip code.

### Map of Zip Codes with Number of Officers in Each

<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesNYPDLive.html" width="1200" height="600" style="border:1px solid">

Embed with `<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesNYPDLive.html">`

<a href="https://twitter.com/share" class="twitter-share-button" data-show-count="false"></a><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


### Map of Precincts (Click Precinct to see stats)

<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesMyNeighborhoodNYPDLive.html" width="1200" height="600" style="border:1px solid">

Embed with `<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesMyNeighborhoodNYPDLive.html">`

<a href="https://twitter.com/share" class="twitter-share-button" data-show-count="false"></a><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

### The case of the misplaced officers

According to the [NYPD Patrol Guide](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/ResidencyRequirements.pdf) officers can't live in the same zip code they work in.

In a post on a police [forum](http://forums.officer.com/t152263/) the following was posted:

![Alt text](../foil/NYPDHomeZip/resources/img/image00.png =1000x)
<br />
![Alt text](../foil/NYPDHomeZip/resources/img/image01.png =1000x)


I suspect that the officers who are listed as living and working in the same zip code have false addresses listed, probably the address of the precinct where they work. (And of course, other officers may also have false addresses listed.) 

If you go by any precinct you will see that the sidewalks, bike lanes, and parks around the precinct are covered with private officers' cars and police vehicles. You will also notice that quite a few of these vehicles have non-New York license plates and have notes on the dashboard with badge numbers or other NYPD identifiers.

![Alt text](../foil/NYPDHomeZip/resources/img/merged.png)


## How did you get this Data?

First I filed a FOIL request (see [here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/NYPDOfficerHomeZip_Request.txt)). It was rejected (see [here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/FoilRejection.JPG)). Then I responded with an appeal (see [here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/NYPDOfficerHomeZip_RejectionAppeal.txt)) This was rejected again.

Side note: I have filed many FOIL requests with the NYPD, and when I receive a response, it is very difficult to track which of my requests the response relates to. You might think that in rejecting your claim they would tell you which request they were rejecting. They don’t. You might also think that if you supplied your own file number than it would be listed in "Your File #" section. You would be wrong on both accounts. The NYPD doesn’t tell you what it’s rejecting. It gives the same canned rejection to every request, no matter how small. It doesn't take emails. You can call but no one will ever pick up or call you back.

## When a foil request doesn't work

A step-by-step guide:<br />
	1. Get a lawyer. (I leaned on family for this one.) <br />
	2. Write out a petition. See [here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/BellvNYPDPetition.docx)  and [here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/BellAffirmationofEBinsupport.docx)<br />
	3. Go to 60 Centre Street. Go downstairs to room 141B in the basement. Yes, you really have to go to the building. [NYS](https://www.nycourts.gov/courts/1jd/supctmanh/motions_on_notice.shtml) says that "E-filing through the New York State Courts Electronic Filing System ("NYSCEF") is mandatory in all cases commenced on or after Feb. 19, 2013 (except for Article 70 (habeas corpus) proceedings, Article 78 proceedings, and election law, matrimonial, and Mental Hygiene Law matters." So, for some reason you can skip the hassle and expense of going downtown for the everything BUT the important things like marriage, elections, and challenging government agencies.<br />
<br />


![Alt text](../foil/NYPDHomeZip/resources/img/60CenterStreet.JPG =1000x)
<br />
*60 Centre Street. Note the text on the building, The True Administration Of Justice Is The Firmest Pillar Of Good Government.*<br />
	4. Get the Index Number for the case, which costs $210. <br />
	5. Now you have to serve the papers, which you can’t do yourself. $187.50 <br />
	6. Then you have to go back to 60 Center Street and file the papers and the receipt of service. <br />

In my case, after a few rounds of calls between the lawyers the NYPD went from "This is ludicrous and will be dismissed" to "Ok here is what you want."

And then they sent over the data.

Helpfully, the NYPD lawyer pointed out: 
"I am not sure if your client is aware but the Department purposefully prohibits members of service being assigned to work within the confines of their residential precinct except for school crossing guards and civilians who began working for the NYPD before July 2009 – see entry nos. 6, 7, & 8 of the attached NYPD Patrol Guide. In addition, NYPD employees are required to live within New York City or one of the surrounding NY counties listed in the Patrol Guide. " 

Which is humorous because the data shows otherwise.

## Turning Data into Maps

[Here](https://github.com/Bellspringsteen/other.nyc/tree/master/NYCGOV/NYPD/NypdOfficersHomeZip) is my repository with the code I used to turn the data into maps. Feel free to point out errors and make your own maps.

FYI Someone in the 45 precinct lives in 12253, that doesn't seem to exist.

Also someone is driving 2 hours each way from East Stroudsburg, PA 18302 to the 14th Precinct. 

## Questions/Suggestions/History

"Every matter, and thing, that relates to the city ought to be transacted therein and the persons to whose care they are committed [should be] Residents," [wrote George Washington in 1796](https://books.google.com/books?id=o9kRAAAAYAAJ&lpg=PA179&ots=wSJrUDImHe&dq=Every%20matter%2C%20and%20thing%2C%20that%20relates%20to%20the%20city%20ought%20to%20be%20transacted%20therein%20and%20the%20persons%20to%20whose%20care%20they%20are%20committed&pg=PA179#v=onepage&q=Every%20matter,%20and%20thing,%20that%20relates%20to%20the%20city%20ought%20to%20be%20transacted%20therein%20and%20the%20persons%20to%20whose%20care%20they%20are%20committed&f=false).
	
Do local officers make better officers? 

If the NYPD created a non-personally identifiable identifier for each officer and then released aggregate data on firearm discharges, home zip, sex, race, and civil rights complaints we could potential answer these questions. Time for another FOIL request.

PRESS:

* http://www.villagevoice.com/news/interactive-map-shows-where-nypd-officers-live-9249670
* https://www.nytimes.com/2016/10/24/nyregion/new-york-today-how-to-build-a-subway-tunnel-boring-machines-second-avenue-subway.html


