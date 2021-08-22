---
layout: portfolio_entry
title: Arrested for bigamy, broken headlight and inadequate windshield wipers. Does the NYPD know this data is public?
tags:
visible: 1
---

TLDR: On https://nyponline.org you can change the url parameters and receive things like disceplenary entries, arrests made with dates for entire career and maybe more. I made a twitter handle <a href='https://twitter.com/NYPDdata'>https://twitter.com/NYPDdata</a> to tweet out the NYPD arrests made. 

<a href="https://blog.labsbell.com/blog/NYPDHomeZip"> Reminder, NYPD officers are not your neighbors, thats a problem. </a>

### Intro

I was reading the ProPublic article on the NYPD (https://projects.propublica.org/nypd-disciplinary-records/) and saw this link to https://nypdonline.org/link/1026 a nypd website. 

Its pretty cool, NYPD is providing a good amount of info on officers like rank, command history, training summary and other items. 

<div style="text-align:center"><img src ="../../img/nypdonline_images/querynypd.png" /> </div>

You can see that for each tab the query is a api endpoint
Request URL: https://oip.nypdonline.org/api/reports/13/datasource/list

I iterated through all the filter lists, here are some interesting items that don't show up in the UI. It's unclear if the NYPD knows that this data is also public. 

Since 2018 NYPD has been publishing arrest data quarterly but that data does not include information on the arresting officer https://data.cityofnewyork.us/Public-Safety/NYPD-Arrest-Data-Year-to-Date-/uip8-fykc so there seems to be some new data here. 


Examples for a officer <a href="https://github.com/Bellspringsteen/other.nyc/tree/master/NYCGOV/NYPD/nypdonline.org/918049_MURRAY%2C%20WILLIAM%20A">LINK TO EXAMPLE FOLDER </a>  

### Filters:

LIST_OF_FILTERS = [1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,1027,1028,1029,1030,1031,1032,1033,1034,1035,1036,1037,2041,2042]

1. Basic Profile Info, Ethnicity, Shield No, 
2. Some kind of summary of command value and unspecified value. 
3. List of arrests per year
4. Data for some kind of visualization involving arrests and misdemeanor information
5. Data for some kind of visualization, unclear
6. Another list of arrests per year
7. Some unknown value for command, PERMANENT is included in each json value
8. Says ArrestYear but a single value
9. **List of all arrests the officer has ever made, just date and type of arrest**
10. Some kind of history of a value for the officer, the values start with a PROB like 22 MONTHS PROB and then end with ANNUAL
11. Another visualization of ArrestYear
12. Unknown value of NO or YES with a date
13. Awards for EXCELLENT POLICE DUTY 
14. Similar to 13
15. Another @ArrestYear but with different values. These seem to be some search of different items on Arrest per year. Perhaps type of arrest or characteristics of arrest.
16. Similar to above
17. Similar to above, all with different values. Must be some kind of filter on Arrests
18. Static image
19. Just name of officer and image
20. Value PERMANENT with date
21. When they were promoted to current command
22. Some record of officer discipline perhaps? Items like INTERNAL INVESTIGATION, CHRONIC SICK-A, DEPT. AUTO ACCIDENT, 
23. Promotion history
24. Really long list of trainings: CUSTOMER SERVICE PROGRAM:  ROLL CALL MODULE 1, INTRODUCTION TO PRECINCT GREETER PROGRAM , INVESTIGATIVE ENCOUNTERS-VIDEO #4 DOCUMENTATION AND SUPERVISION-UNIT TRAINING JULY 2016, COBRA REFRESHER TRAINING (THREAT)
25. List of events or trainings attended:POLICING A DEMOCRACY JULY 03. JUNE 07   
26. List of arrest types but all with the same value, not sure what this is
27. "Search Instructions go here", "Interactions": [], "RelatedItems":
1027. More detailed courses:DETECTIVE BUREAU RETRIEVING BODY WORN CAMERA DATA, COUNTERTERRORISM U.A.S. (UNMANNED AIRCRAFT SYSTEMS) DRONE AWARENESS,IPHONE AND DAS MOBILE OPERATION, **LOCATING APPLE DEVICES USING YOUR DEPARTMENT SMARTPHONE**
1028. Another “@ArrestYear” with different values
1029. Unfilled Event details
1032. Related to FOIL requests? List of values “FOIL 4234” with dates
1033. FOIL & Discipline Documents is the key but no values
1034. Some graph that is common across all officers: Lists things like FEMALE (6,191), MALE   (26,539), NON-BI (1)
1035. Some graph based on ethnicity same across all officers: Lists things like Asian 3055, BLACK 4933, NATIVE AMERICAN 23
1036. empty
1037. Active Disciplinary Cases = 100, same across all officers
2042. VIOLATION, MISDEMEANOR, FELONY with values

### CSV of Arrests

I parsed through all officers and saved all raw requests for each filter. You can see the data <a href="https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/nypdonline.org/data-folders.zip">HERE </a>  . I also parsed all the arrest data into a single CSV which you can see <a href="https://github.com/Bellspringsteen/other.nyc/tree/master/NYCGOV/NYPD/nypdonline.org/arrests_csv_split">HERE </a> ( caution 5 Million rows, you will have to re-append the csv files together) 

For CSV, this is the headers. There is data from way back in 1982.

Epoch_time_of_arrest,string_date_of_arrest,day_of_week,holiday,arrest_type,officer_name_without_comma,officer_tax_id,officer_race,officer_appointment,<br>officer_tenure,officer_assignment,officer_command,officer_rank,officer_shield,officer_substantiated_complaints,officer_unsubstantiated_complaints

#### Example data

378709200, 1/1/1982 12:00:00 AM, Friday, New Year's Day, ROB-1ST:FORC THEFT/DEADLY WEAP, SOHAIB RAFI, 942750, ASIAN, 7/10/2006 12:00:00 AM, 14, 2/18/2021 12:00:00 AM, UNIFORMED OPERATIONS UNIT, DETECTIVE 2ND GRADE, 1044, 0, 0


378709200, 1/1/1982 12:00:00 AM, Friday, New Year's Day, ROB-1ST:FORC THEFT/DEADLY WEAP, SOHAIB RAFI, 942750, ASIAN, 7/10/2006 12:00:00 AM, 14, 2/18/2021 12:00:00 AM, UNIFORMED OPERATIONS UNIT, DETECTIVE 2ND GRADE, 1044, 0, 0

Complaints are from the CCRB data. 


### Arrest Types

Some interesting items were the list of arrests by type and frequency. See <a href="https://github.com/Bellspringsteen/other.nyc/blob/master/NYCGOV/NYPD/nypdonline.org/arrest_types_sorted.txt">HERE </a> . There are 2100 things people were arrested for!!

The top

395723  CRIM POSS MARIHUANA-5TH:PUBLIC <br>
381779  ASLT W/INT CAUSES PHYS INJURY <br>
287489  INTENT/FRAUD OBT TRANS W/O PAY <br>
279440  CRIM POSS CONTRL SUBST-7TH <br>
246144  PETIT LARCENY <br>
200643  VIOL OF LOCAL LAW VIOL <br>
149816  CRIM POSSESSION STOLN PROP-5TH <br>
145830  AGGRAVATED UNLIC OPER/MV-3RD <br>
131656  AGGRAVATED UNLIC OPER VEH-3RD <br>
109170  CPCS-3RD:NARC DRUG INT/SELL <br>

WOW. Marijuana. **Jumping turnstiles!!!**

Jumping the turnstile is the third most common.

Ones I found interesting <br>

13676  TRADEMARK COUNTERFEITING 3RD <br>
8458  US CODE UNCLASSIFIED <br>
7214  PROMOTING GAMBLING-2ND <br>
6379  UNAUTHORIZED SALE OF FARECARD <br>
6125  POSS/SELL UNSTAMPED CIGARETTES <br>
5504  PUBLIC LEWDNESS <br>
5222  MV LICENSE VIOL:NO LICENSE <br>
5097  UNLAWFUL ASSEMBLY <br>
2637  FORGERY-3RD <br>
2252  UNLICENSED BOTTLE CLUB <br>
2146  URINATE IN PUBLIC <br>
1644  AUTO STRIPPING-3RD <br>
1531  EQUIP VIO:WINDSHIELD TINT VIOL <br>
1487  CPCS-4TH:HALLUCINOGEN <br>
1435  UNAUTH PRACT PROFESSION <br>
999  RIOT-2ND <br>
864  FAILURE TO COMPLY WITH SIGN <br>
840  POS GAMB DEVICE:SLOT MACHINE <br>
689  INADEQUATE OR NO STOP LAMPS <br>
643  INCITING TO RIOT <br>
558  REFUSAL TO TAKE BREATH TEST <br>
558  EQUIP VIO:HEADLIGHTS <br>
495  JOSTLING HAND NEAR POCKET <br>
400  BICYCLE OPER ON SIDEWALK <br>
330  LOITERING <br>
240  SEAT BELT VIOLATION-DRIVER <br>
235  BICYCLE:FAIL TO KEEP RIGHT <br>
202  UNAUTH RECORDING PERFORMCE-2ND <br>
158  MFG DANGEROUS INSTRUMENT <br>
85  SELL TIX W/O PRINTED PRICE <br>
80  BRIBERY PUBLIC SERVANT-2ND <br>
78  DISRUPT REL SER/FUNRL/MEMORIAL <br>
64  BRIBING A WITNESS <br>
48  ILL SIGNAL:LESS THAN 100 FEET <br>
35  EAVESDROPPING <br>
29  UNAUTH BOTTLING OF ALC BEV <br>
29  CEMETERY DESECRATION-1ST DEG <br>
24  TRANSPORT UNAUTH RECORDING-2ND <br>
14  FORTUNE TELLING <br>
10  LOG BOOK VIOLATIONS <br>
10  INADEQUATE WINDSHIELD WIPERS <br>
8  OPER PRIV MV W/O US MAIL SIGN <br>
8  CONSPIRACY TO FORM MONOPOLY <br>
7  TAKING BRIBE FOR PUBLIC OFFICE <br>
7  ON PREMS RECORDKEEPING VIOL <br>
6  LITTER RAILROAD RIGHT-OF-WAY <br>
6  ABORTION 2ND <br>
5  ILL OP SNOMOB <br>
4  OWNING/HARBORING UNLICEN DOG <br>
3  RADIO/TV/MOVIES PROCEEDINGS <br>
2  TRUSTEE VOTE <br>
2  FAIL TO CHANGE ADDRESS ON LIC <br>
2  EQUIP VIO:SPLASH GUARDS <br>
2  EQUIP VIO:NO DOOR HANDLES <br>
2  ABORTION-1ST <br>
1  UNLAW SALE BICYCLES <br>
1  SNOWMOBILE - IMPRUDENT SPEED <br>
1  KEEPING UNVACCINATED DOG <br>
1  FAIL TO MAINTAIN PROPER FILES <br>
1  BIGAMY <br>
1  ANARCHY-PUB/DIST DOCUMENT <br>


These are listed as arrests. **But does this really mean someone was arrested for not having door handles?** Or not wearing a seatbelt? Why are these arrests and not tickets? There are millions of tickets given each year in NYC, so these cant be tickets. 

I tried cross referencing with the posted arrest data, for instance on  3/16/2021 in this data there is a arrest for Windshield Tint Violation. In the official NYPD quarterly releases, there is a  3/16/2021 arrest for TRAFFIC,UNCLASSIFIED INFRACTIO. 'TRAFFIC,UNCLASSIFIED INFRACTIO' never appears in the nypdonline dataset. So is someone doing some data 'cleaning'? Why remove the data about tinting?

### Twitter Account

Posts everyday <a href='https://twitter.com/NYPDdata'>https://twitter.com/NYPDdata </a> the arrests from 2 weeks ago. I could move it to arrests from yesterday, but I think sometimes arrests are added later.

I could add more info like about how it compares historically etc. 

### Some Interesting Graphs

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_over_all_time.png" /> </div>
<div style="text-align:center">Arrests over time from Currently Employed NYPD Officers</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/10years_arrests_over_all_time.png" /> </div>
<div style="text-align:center">Just last 10 years of arrests for current employed</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/4years_arrests_over_all_time.png" /> </div>
<div style="text-align:center">Last 4 years for currently employed</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/1years_arrests_over_all_time.png" /> </div>
<div style="text-align:center">Last 1 year of arrests over time</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday.png" /> </div>
<div style="text-align:center">Arrests by day of week. I was surprised by this. Without any real knowledge I would assume that arrests were much higher on weekends. </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_holiday.png" /> </div>
<div style="text-align:center">Arrests by holiday</div>
<br>

### Graphs about arrest type

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_MARIHUANA.png" /> </div>
<div style="text-align:center">Marijuana arrests going down over time</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_DRUG.png" /> </div>
<div style="text-align:center">Drug arrests</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_Controlled_Substance.png" /> </div>
<div style="text-align:center">Controlled Substance</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_PETIT.png" /> </div>
<div style="text-align:center">The number of arrests for Petit Larceny shot up in mid 2013. I’m really curious why!</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_BICYCLE.png" /> </div>
<div style="text-align:center">Arrests for bicycle related things</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_POSSESSION_OF_BURGLAR_TOOLS.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_OBSTRUCTING_TRAFFIC.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_FIREARM.png" /> </div>
<br>


<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/weird_daily_spikes_graffitti.png" /> </div>
<div style="text-align:center">Weird daily spikes for graffitti arrests</div>
<br>

### What about arrests by weekday for type of arrest

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday_FIREARM.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday_MARIHUANA.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday_ASLT.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday_INTENT_FRAUD_OBT_TRANS_W_O_PAY.png" /> </div>
<div style="text-align:center">So basically, people going to work/school during the week are arrested for jumping turnstile.</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/arrests_by_weekday_AGGRAVATED_UNLIC_OPER.png" /> </div>
<br>

### What about individual officers arrests? 

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_number_arrests_per_day_over_1.png" /> </div>
<div style="text-align:center">How often do officers make more than 1 arrest per day. Who is arresting 200 people in a day? Data issue?</div>
<br>

Diving in, says that on 04/25/2018, tax id 929600 (https://oip.nypdonline.org/view/1/@TAXID=929600/) arrested 196 people. Seems like this officer is part of the special fraud squad and arrested them for GRAND LARCENY 3RD DEGREE. 

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officers_arrests_per_year_2019.png" /> </div>
<div style="text-align:center">Arrests per year in 2019</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officers_arrests_per_year_2019_log.png" /> </div>
<div style="text-align:center">Log graph of above</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_number_arrests_per_day_over_1_percentage.png" /> </div>
<div style="text-align:center">Occurrences of arrests per day 1 or greater</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019.png" /> </div>
<div style="text-align:center">How many days make an arrest in 2019 per officer</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_POLICE_OFFICER.png" /> </div>
<div style="text-align:center">Percentage of officers who make arrests on X days for value Police Officer</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_DETECTIVE.png" /> </div>
<div style="text-align:center">Percentage of officers who make arrests on X days for value Detective</div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_WHITE.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_BLACK.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_ASIAN.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_HISPANIC.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_BLACK.png" /> </div>
<br>

### Tenure and arrest frequency

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_tenure_5.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_tenure_10.png" /> </div>
<br>

<br>
<div style="text-align:center"><img src ="../../img/nypdonline_images/officer_how_many_days_make_an_arrest_2019_tenure_20.png" /> </div>
<br>




### Next Ideas

* FOIL for specifics about some arrets, like was someone really arrested for bigamy? Whats that story
* What is the variance of arrest per officer? Like do they only arrest for 1 type
* The CCRB compliant data is interesting, can we say something about the officers that have complaints on certain arrests by date.
* Can we cross reference this with the quarterly published arrests that are about the person arrested but not the arrested officer? To get a more complete dataset?
* Whats going on with some of these filters like filter 22 or 1027. There is some interesting data there. 
* Is there grouping of arrest types by precinct and time? i.e. the spread of a arrest type over time from one location through city as police learn they can arrest for that, quota, or are instructed to?

### Code

None polished. All hacked together with bugs. <a href="https://github.com/Bellspringsteen/other.nyc/tree/master/NYCGOV/NYPD/nypdonline.org"> Github</a>