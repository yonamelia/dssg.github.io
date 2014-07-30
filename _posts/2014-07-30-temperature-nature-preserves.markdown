---
layout: post
title: "Heatmaps for Habitats: Enriching Conservation Sensor Data"
author: Rob Mitchum
pic: "team-header.jpg"
---
<img src="/img/posts/conserv-team.png">

Environmental causes typically work to preserve portions of the planet in their pre-human state. But conservation groups are increasingly finding ways of using modern technology to support their mission, allowing them to gather more information about the areas they protect and better argue to decision-makers and local residents why they are worth protecting.

The [Tropical Ecology, Assessment and Monitoring (TEAM) Network](http://teamnetwork.org) is one such effort. Founded by Conservation International (CI), and now a partnership of [Conservation International](http://www.conservation.org), the [Smithsonian Institution](http://www.si.edu/), and the [Wildlife Conservation Society](www.wcs.org), TEAM deploys sensor networks at 17 sites around the globe, including sites in Costa Rica, Ecuador, Madagascar, and Indonesia. These sensors gather wildlife photos, climate data, carbon measurements, and other information that is publicly shared to support ecological and conservation research.

For the first month of the DSSG fellowship, fellows Nadya Calderon, Scott Cambo, Christopher Lazarus, and Raphael Stern and mentor Varun Chandola worked with TEAM on a project to extract more value from this broad sensor network. Working with data from motion-detecting camera traps spread out across protected sites, the team developed new methods to build a high-resolution, dynamic map of temperature -- and more -- for each area, enriching TEAM’s data with valuable new layers of information.

####Erupting with Data

[Volcan Barva](http://www.teamnetwork.org/network/sites/volc%C3%A1n-barva) is an inactive volcano in north central Costa Rica, sitting within a rich, diverse tropical rain forest region. Since 2003, TEAM has studied the ecology of this region, placing 60 camera traps along the volcano’s “steep elevational transect,” a gradient rising from 26 meters to 2,900 meters over just 20 kilometers.

<img src="/img/posts/ci-barva.png">

TEAM’s camera traps are small, camouflaged devices automatically triggered by motion and used to study the natural movement of wildlife deep in nature. In Volcan Barva, the cameras regularly snap photos of jaguars, mountain lions, anteaters, and endangered birds, recording the time and date of the photo. In 2011, [a TEAM study](http://rstb.royalsocietypublishing.org/content/366/1578/2703) reported using camera traps in seven countries captured over 50,000 images containing over 100 species -- and even one suspected poacher. 

<img src="/img/posts/ci-species.png">

But the camera trap captures more than just pictures and time -- it also records the temperature when the photo is taken. Ecologists at TEAM are interested in how temperature and other climate factors affect how species migrate within their habitats, but with only one weather station recording climate data per site, it’s not possible to get higher-resolution data about the temperature in different subregions.

<img src="/img/posts/ci-photos.png">

“They’re interested to see how these small temperature variations might affect species movements, since a lot of these animals have a very narrow range of comfort,” said Raphael Stern, one of the fellows on the project. “The camera trap information can tell you where animals are located, so to study that, you would need to know what the temperature is throughout the site.”

Instead of extrapolating temperature from just one station over the entire site, the camera trap temperature readings offered the possibility of richer detail about the area's climate. But while the thermometer on a weather station constantly measures temperature from a fixed point, the 60 camera traps only record a temperature when they are triggered by motion. That created technical challenges for the team in building a comprehensive map from disorganized data.

“The problem is there are 60 fixed points, that go off at random, different moments,” said Christopher Lazarus. “If you had a uniform sample over time, it would be easy to just simply interpolate over space. But it’s basically sparse over time and space. The problem is non-uniformity.”

####Creating Order From Randomness

To turn this random collection of data into a uniform map, the team built a model using a method called radial basis interpolation that determines a value based on the distance from a known point. Say you picked a particular location in the Volcan Barva site, then looked around for camera trap temperature readings in the vicinity. In the equation, camera traps closer to your target would be weighed more heavily, and traps farther away would be weighed as less important, combining to provide an estimate of temperature in your location. 

A similar process is used for calculating “distances” in time -- for a camera trap nearby your target location, a reading taken 10 minutes before your chosen time would be weighed more heavily than a reading taken six hours later. By organizing the site into a grid of thousands of points, and calculating these space and time estimates for each of these locations, the model can produce the dynamic, high-resolution visualizations of temperature changes across the site that the TEAM researchers sought.

<iframe width="640" height="360" src="//www.youtube.com/embed/f_M6KgpfeiI" frameborder="0" allowfullscreen></iframe>
[*Temperature changes across the Volcan Barva site (left), matched with the migration of [peccaries](http://en.wikipedia.org/wiki/Peccary), or skunk pigs (right)*]

The resolution of the map was high enough that the fellows were able to deduce natural features of the sites that weren’t obvious in the original dataset.

“We learned about the geography of the site through the results,” Stern said. “We kept seeing consistently that this one portion of the south was always predicted to be much colder than the north. So we thought there must be a mountain there or we’re completely wrong. And when we looked at the map, sure enough, right where it’s colder, that’s exactly where the volcano is. So we learned something about the geography from the data and then confirmed it with the map.”

####Two Heatmaps For The Price of One

Once the model for producing temperature grids was built, the fellows added another dimension: a heatmap for tracking species density based on camera data. The method is the same -- calculating an estimate for a given location and time based on readings from nearby sensors -- but uses the number and type of animal spotted by those sensors instead of the temperature. Side by side, the two visualizations can help ecologists examine patterns of movement correlated with changes in temperature, identifying interesting relationships for follow-up research.

<img src="/img/posts/ci-migration.png">

“They have collected this data for their own very specific questions, and they have their own perspective on data, their own ideas for what to do with it,” said Nadya Calderon “We wanted to demonstrate what happens when you step back and say how else can you use this data?"

The model created by the DSSG team can be applied to all 17 sites monitored by TEAM, and could be used by any other conservation group that collects similarly-structured data with camera traps that record temperature and time. Furthermore, it could be applied to study basically any quantified measure over space and time -- Lazarus ran it on crime data from Mexico City to observe how patterns fluctuated over different neighborhoods and times of day. 

“We’re adding value to their camera traps,” said Scott Cambo. “This was an opportunity to not only make that high-resolution temperature grid, but since each one of those data points is also an observation of an animal, to be able to understand how temperature -- and climate change -- affects animal behavior.”
