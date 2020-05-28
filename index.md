## Wildfire Hackathon
Project by: Jack Seagrist, Yash Gaur, Hunter Johnson

### Project Summary
Our group chose to address problems related to evacuation routes. (have sources here about evacuation routes currently and evacuation plans, research papers). 

[a relative link](tracker_start.md)
[a relative link](map.html)
[a relative link](map3.html)

[Prototype](/template/index2.html)

To address these problems, our group developed a prototype tool that could be used by fire departments, sheriff departments, and citizens as a central repository of real time fire information to assist with evacuation. We have developed a prototype for a real time fire prediction model that uses the estimated fire path to provide an output of which parts of the jurisdiction should be under which evacuation order: Level 1 Alert, Level 2 Warning, Level 3 Order [1]. Our prototype was developed focusing on California, using historical California wildfire data as inputs to train the model. 
SEE UPDATED PDFS from Scott - now just two levels and a shelter in place order (in outreach folder)

thinks there needs to be a happy medium to get people out of the way and evacuated, but not too early of a full evacuation (leads to evacuation fatigue) or no evacuation at all. Balance (no evac --- happy medium --- full early evac) from Scott

From Nic Elmquist---------------------------------------
Great chatting with you all today.

Models really need analysts right now to tweak parameters and make the models accurate, because even if you put in what you think are the parameters that represent the region
SB example - if you use the shrub model for fuel, the fire never moves as fast as it does in real life. Need to select grass even though it is shrubs over there. Only would know that with experience in that area
Need the analyst to explain the outputs

Incident Teams
No requirements for fire departments to have these analysts
15 federal incident management teams, 5 state incident management teams
Each one has one of the fire behavior analyst.
 

Below are the things I talked about that you may find helpful…

Our evacuation map should be available at this link…https://drive.google.com/drive/folders/1iDKAJqwAealCSuWDikNbuLUO0fvdrV8j?usp=sharing . It’s “For Internal Use” only so please don’t share, but use for your general awareness.

The paper regarding Wildfires in California including infrastructure damage can be found here: “Long term trend in wildfire damages in California” - http://emlab.msi.ucsb.edu/sites/emlab.msi.ucsb.edu/files/wildfire-brief.pdf

The link to the FTP site containing the Fire Progression map is here” https://ftp.nifc.gov/public/incident_specific_data/calif_s/!CALFIRE/2017_Incidents/CA-VNC-103156_Thomas/GIS/Products/20180104/ . You should be able to find similar maps for other large incidents in the same locations in their respective folders.

Attached to the email is a screen shot showing the models we typically use to support incidents, an overview of WFDSS and the modeling support embedded within the site, and a guide to the use of Fire Behavior Fuel Models that are used in the models.

Chuck’s contact info is below…

Chuck McHugh

Fire Spatial Analyst

Forest Service

Rocky Mountain Research Station

Fire, Fuel, and Smoke Science Program

5775 US Highway 10 W

Missoula, MT 59808

charles.mchugh@usda.gov

www.firelab.org

 

#### Problem

  Wildfires pose a significant risk to human life and society, causing an estimated loss of $60-280 billion dollars in 2016 alone in the US with dozens of fatalities each year (11).  Climate and weather directly influence wildfire risks and global warming is expected to further exacerbate fire damage towards natural and urban ecosystems (10).  Just in the past 5 years, 2015-2020, several unprecedented fires have occured in varying parts and ecosystems of California showcasing the needs for new ideas and tools.    

#### Motivation

  One vital aspect of fire loss prevention is evacuation procedures, in particular how fire and police authorities decide and implement effective yet necessary evacuations in the face of imminient danger.  Aggressive fires, jammed roads, and paniced evacuees can complicate well thought out evacuation procedures potentially having fatal results.  
  Our project aims to create an easy to use, government facing, data based tool that assissts fire departments in real time evacuation scenarios.  Our tool utilizes live traffic and census demographic data to provide a blend of need to know data to decision makers in high stake situations.  High human and economic loss fires such as the Camp Fire in Paradise, CA serve as a motivation to help provide information for safe evacuation routes or areas to shelter to minimze wildifre loss.  

#### Challenges

  Creating a data based live platform has several challenges, most surrounding availability of useful data and its timely implementation.  However, clever integration of online softwares allows a variety of critical variables to be available simultaneously while constantly updating.  Data and technological approaches that fight natural disasters are still naiscent but are rapidly evolving, providing a promising future for our platform.    

#### Project Scope

(Describe the project here)
Fire prediction
Create circle radius outwards for evacuation
Traffic Layer
Demographic layer to highlight the elderly
Defensible space option - interactive map which allows fire department to locate defended space and send out a tweet
Add Ons:
Us-census layer - people contact info within zones for reverse 911 call
Idea → maybe have a component that allows people to enter the number of resources fighting a fire to influence our model and determine if evacuation is necessary, goes back to getting rid of evacuation fatigue
Have a time component to our layers, to show progression, and have metadata for how long the fire will take to get there

cell phone gps data to know who is still in the area??????? FUture work???

Based on notes with Scott should just focus on 1) Model perimeter prediction- with what the varying perimeters will look like over time 2) estimate evacuation overlay 3) traffic data 4) hospitals, nursing homes, and school locations 5) ability to add in community refuge areas if fire/sheriff dept need to add in

#### Model
Here are some links for some stuff I found for the model. Able to generate perimeters with Flammap 6 software. But someone made a set of python scripts for generating perimeter to webmap, could maybe use that. Also could maybe use outputs from flammap to train AI model. This pdf lists out a lot of the other perimeter prediction softwares as well (Farsite, Nexus, Wi-fire, ArcFuels) http://unigis.sbg.ac.at/files_en/Mastertheses/Full/104195.pdf

Flammap Process
1) download lcp data from Landfire 2) get fuel moisture conditions from https://www.wfas.net/index.php/national-fuel-moisture-database-moisture-drought-103 or https://firesafesanmateo.org/resources/live-fuel-moisture 3) find wind data from that day to use with wind ninja 4) foliar moisture? 5) try to find wtr and wnd files https://www.wunderground.com/history/weekly/us/ca/santa-rosa/KSTS/date/2018-10-25 https://www.meteoblue.com/en/weather/historyclimate/climatemodelled/santa-rosa_united-states-of-america_5393287

Map
Interactive map help https://stackoverflow.com/questions/36581775/mapbox-js-marker-creation-on-click
And think that maybe we can use leaflet.js if need more interactive?
https://paulcrickard.wordpress.com/2012/06/29/leaflet-js-interactivity-ii-allow-users-to-add-points/ --> looks good

#### Future Work
Alert or reference to where hospitals/nursing homes.  And also the number of houses/ population density. Also the time of day will cause different types of evacuation (ask Scott)
What to do for people without cars (we typically assume everyone is able, has a car, speaks english) - research (bodega bay santa rosa). Look into grassroots organizations for illegal immigrant and disabled populations help with evacuation (think about demographic layers)
Something with IPAWS https://www.fema.gov/integrated-public-alert-warning-system ?
Have some sort of public facing side with this as well (or just like a twitter alert)

Map - explore mapbox features with database for users to interact with the map on the fly https://www.mapbox.com/videos/how-to/deploy-a-collaborative-map-with-quick-launch/ https://www.mapbox.com/solutions/quick-launch

Machine Learning - Don't have the time scale data that we need to make model really work. We would need for a single fire the shapefile perimeters at smaller time steps, not just the final perimeter. Then we would have to add in the temporal data somehow. Potentially by making raster values for each datastack where the pixel value is based on the time from ignition

From Scott Westrope - Redundancy. Example is the Tubbs fire where they lost 72 cell towers in 4 hours. Thinking about actual use of the system, it would be good to have it be redundant and still work if towers go down, or if the users are out in the middle of nowhere with no/limited signal (have some type of feature where you can download model based on current/future conditions onto phone and operate that way)

Improved modelling capabilities - talk about what we would need to add in to improve the model. Model predictability should include historical data since fires tend to follow the same path

#### Data
GEE - Data Layers

GeoMAC - historical shape files
Link 1: Determining Fire Dates and Locating Ignition Points With Satellite Data
Link 2: Cal Fire Frap (just perimeters)
Link 3: USDA historical fire
Link 4: InciWeb
Link: Geomac <- think this is the one we used

Descartes Labs - Ignitions


NOT SURE if we used any of this
Town Boundaries:
Link: Cal data
Link: Cal Fire
Link: Who’s on First
Population Data:
https://www.ornl.gov/news/gis-landscan-goes-public
https://geoplatform.maps.arcgis.com/home/item.html?id=e431a6410145450aa56606568345765b
Fire Hazard severity zones:
https://osfm.fire.ca.gov/divisions/wildfire-planning-engineering/wildland-hazards-building-codes/fire-hazard-severity-zones-maps/
Fhszssn
Fire Threat:
https://frap.fire.ca.gov/mapping/gis-data/
US Census Data:
https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-data.html



### Tools

The main tools used to develop this platform were google earth engine, google colaboratory, and Mapbox/Arc WebMap.

### References

[1]. **Descartes Labs** (https://www.descarteslabs.com/)

[2]. Google earth engine

[2]. **Paradise Evacuation Zones** (https://www.townofparadise.com/index.php/17-news-events/248-evacuation-zones)

[2]. Failures of evacuation system Paradis - https://www.pbs.org/wgbh/frontline/article/camp-fire-anniversary-new-details-troubled-evacuation/  && Paradise Vulnerable Populations - https://www.nfpa.org/News-and-Research/Publications-and-media/NFPA-Journal/2019/January-February-2019/News-and-Analysis/Dispatches

[3]. Evacuation Behavior Literature (https://rgs-ibg.onlinelibrary.wiley.com/doi/pdf/10.1002/geo2.51)

[]. California Most Vulnerable Communities Map - (https://www.directrelief.org/2019/07/which-california-communities-are-most-vulnerable-to-wildfires/) -- might be able to incorporate that map with our map if we do arcgis webmaps

[3]. **US Forest Service Evacuation Levels** (https://www.fs.usda.gov/Internet/FSE_DOCUMENTS/stelprd3852749.pdf)

[4]. Cova, Thomas (2019): Geosimulating Hazard Warning Triggers: Geometry, Dynamics, and Timing. The University of Auckland. Conference contribution. https://doi.org/10.17608/k6.auckland.9863267.v1

[] NIST Disaster Failure Studies Fires - https://www.nist.gov/topics/disaster-failure-studies/studies-hazard-types/fires

[] NIST Study of emergency communications during a fire -https://www.nist.gov/el/fire-research-division-73300/wildland-urban-interface-fire-73305/nist-study-emergency

[] NIST community planning resilience guide

[5] ADD REFERENCES FOR GITHUB/CODE WE USED TO START OUR MODEL

[10] Keeley and Syphard, 2016, 'Climate Change and Future Fire Regimes: Examples From California", Geosciences 6(3), 37.

[11] Thomas et al, 2017, 'The Costs and Losses of Wildfires - A Literature Survey', National Institute of Standards and Technology.

### Thank you

We would like to thank the following people for their help in the creation of this project: Derek Fong, Rebecca Miller, Stace Maples, Caitlin Kontgis and the Descarte labs team, Scott Westrope, David Shew, Nic Elmquist ....
