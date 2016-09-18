---
layout: portfolio_entry
title: Where Does the NYPD Live?
description: Interactive plots for NYPD Home Zip Locations. Click on your home precinct and see where the cops in your neighborhood live.
twitterimage: http://blog.labsbell.com/foil/NYPDHomeZip/resources/img/screenshot.png
tags: FOIL
visible: 0
---


You would think based on [this](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/ResidencyRequirements.pdf) that officers must "live in one of the city’s five boroughs or Nassau, Suffolk, Rockland, Westchester, Putnam or Orange counties."

* 51% of NYPD Officers Live in NYC 
* 4% of NYPD Officers Live in Manhattan
* 14% of NYPD Officers Live in Brooklyn
* 8% of NYPD Officers Live in The Bronx 
* 10% of NYPD Officers Live in Staten Island
* 15% of NYPD Officers Live in Queens
* 24% of NYPD Officers Live in Long Island
* 12% of NYPD Officers Live in Upstate NY
* 4% of NYPD Officers Live in the Same Zip they Serve


### Map of Zip Codes with Number of Officers in Each

<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesNYPDLive.html" width="800" height="400" style="border:1px solid">

Embed with `<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesNYPDLive.html">`

<a href="https://twitter.com/share" class="twitter-share-button" data-show-count="false"></a><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>


### Map of Precincts (Click Precinct to see stats)

<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesMyNeighborhoodNYPDLive.html" width="800" height="400" style="border:1px solid">

Embed with `<embed src="http://blog.labsbell.com/foil/NYPDHomeZip/WhereDoesMyNeighborhoodNYPDLive.html">`

<a href="https://twitter.com/share" class="twitter-share-button" data-show-count="false"></a><script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

### The case of the misplaced officers

According to [this](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/ResidencyRequirements.pdf) officers can't live in the same zip code they work in. 

In a post on a police forum the following was posted but quickly removed, http://forums.officer.com/t152263/ .

![Alt text](../foil/NYPDHomeZip/resources/img/image00.png =1000x)
<br />
![Alt text](../foil/NYPDHomeZip/resources/img/image01.png =1000x)


I suspect that the officers who are listed as living in the same zip and potentially lots more have false addresses listed, probably the address of the precinct they work. If you go by any precinct you will see that the sidewalks, bikelanes, and parks around the precinct are covered with private officers cars and police vehicles. You will also notice that quite a few of these vehicles have non-ny plates but have notes on the dash with badge numbers etc.

![Alt text](../foil/NYPDHomeZip/resources/img/merged.png)


## How did you get this Data?

First I filed a foil request [Here](../NYPDOfficerHomeZip_Request.txt) 

This was Rejected see  [Here](../FoilRejection.JPG)

Side note, if you file a lot of FOIL requests to the NYPD you might think that in rejecting your claim they would tell you which request they were rejecting. They dont. You might also think that if you supplied your own file number than it would be listed in "Your File #" section. You would be wrong on both accounts. The NYPD doesnt tell you what its rejecting. It gives the same canned rejection to every request, no matter how small. It doesn't take emails. You can call but no one will ever pick up or call you back. 

Then I responded with an appeal  [Here](../NYPDOfficerHomeZip_RejectionAppeal.txt)   

This was rejected again. 

## How to sue the NYPD.

Get a lawyer (I leaned on family for this one)

Write out a petition. 

[Here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/BellvNYPDPetition.docx)  and [Here](https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/NypdOfficersHomeZip/BellAffirmationofEBinsupport.docx) 


Go to 60 Centre Street

![Alt text](../foil/NYPDHomeZip/resources/img/60CenterStreet.JPG =1000x)

Note the text on the building, The True Administration Of Justice Is The Firmest Pillar Of Good Government.

Go downstairs to room 141B in the basement. 

Note: "E-filing through the New York State Courts Electronic Filing System ("NYSCEF") is mandatory in all cases commenced on or after Feb. 19, 2013 (except for Article 70 (habeas corpus) proceedings, Article 78 proceedings, and election law, matrimonial, and Mental Hygiene Law matters."

For some reason you can skip the hassel and expense of going downtown for the everything BUT the important things like elections, challenging government agencies, matrimonial etc. 

Get the Index Number for the case 210$

Now you have to serve the papers, which you cant do yourself, $187.50

Then you have to go back to 60 Center Street and file the papers and the receipt of service. 

After a few rounds of calls between the lawyers in which the NYPD went from " this is ludicrous and will be dismissed" to " ok here is what you want."

And then they sent over the data.

Helpfully the NYPD lawyer who pointed out "I am not sure if your client is aware but the Department purposefully prohibits members of service being assigned to work within the confines of their residential precinct except for school crossing guards and civilians who began working for the NYPD before July 2009 – see entry nos. 6, 7, & 8 of the attached NYPD Patrol Guide. In addition, NYPD employees are required to live within New York City or one of the surrounding NY counties listed in the Patrol Guide. Plus, NY Appellate Courts have ruled in Ruberti, Girvin & Ferlazzo v. N.Y. State Div. of State Police, 641 N.Y.S.2d 411, (3rd Dpt, 1996) that the disclosure of troop, zone and station assignments of each sworn member of the State Police could endanger the life and safety of those officers." Which is humorous because the data shows otherwise. 


## Turning Data into Maps

[Here](https://github.com/Bellspringsteen/other.nyc/tree/master/NYCGOV/NYPD/NypdOfficersHomeZip) for turning the data into maps   

