---
layout: post
title: "Cook County Land Bank Part 2: A Real Estate Finder for Vacant Properties"
author: Skyler Whorton
pic: "cclb-header.png"
published: true
---
In a [previous post](http://dssg.uchicago.edu/2013/07/11/cook-county-land-bank.html), we asked how the [Cook County Land Bank Authority](http://www.cookcountylandbank.org/) ought to decide which vacant and abandoned properties to acquire. Let’s illustrate this question with a hypothetical comparison of two homes in Chicago.

<img src="/img/posts/cclb-home1.png">

39XX W Van Buren St. is a typical two flat multi-family property in Garfield Park, a neighborhood on Chicago’s West Side that has long struggled with economic decline, depopulation, and abandonment. The home was built in the early 20th century, and sits near both the neighborhood’s namesake park and a CTA Blue Line station. In its heyday, it probably housed at least two families on a densely-populated working-class block. 

Speculative interest was running high in Garfield Park during the real estate bubble, when investors believed the area to be next in line for gentrification. The property sold in 2005 for nearly $300,000. A little over a year later, near the beginning of the bust, the bank filed a foreclosure on the property. All indications suggest that the building is vacant. Six other homes on the block are also in foreclosure.

<img src="/img/posts/cclb-home2.png">

46XX S Evans is a two flat near the southern border of Grand Boulevard, a community area on the South Side comprising a portion of the Bronzeville neighborhood. Like Garfield Park, Grand Boulevard underwent decades of depopulation and abandonment. The home sits about half a mile from a CTA Green Line station on a block with several other foreclosed properties. It sold for half a million dollars in 2006, only to go into foreclosure in 2012, and it was boarded up and vacant by late last year.

Suppose the banks foreclosing on these two properties approached the Cook County Land Bank and offered to hand over the titles. Perhaps in a perfect world, the Land Bank could take possession of both, identify responsible owners, and put them back to use. However, resources are limited and priorities need to be set. What should the agency’s decision-making process look like in these two situations?

#### Neighborhood context

Take the Garfield Park property first. This is the community area with the highest foreclosure rate in the city of Chicago, as well as one of the highest rates of 311 vacancy complaints. The crime rate is consistently among the city’s highest. Moreover, the neighborhood’s median sales price is in the fifth percentile of all community areas, and roughly 60% of residential properties sell for less than $20,000. Banks are approving less than one mortgage per 2,000 residents, among the lowest rates in the city. So it’s fair to say that demand for owner-occupied residential property is exceptionally low. 

<img src="/img/posts/cclb-graph1.png">
_Single family home median transaction price in West Garfield Park_

At the height of the real estate boom at the end of 2006, the median single family home sale price in West Garfield Park was $180,000. The next two years saw an utter collapse in the housing market, to the point where most of the homes were selling for less than the price of a new car. In such circumstances, existing homeowners have a strong incentive to walk away from their underwater mortgages, and home equity to back reinvestment is virtually nonexistent. Moreover, potential buyers have almost no option other than cash, since banks are understandably reluctant to write mortgages in neighborhoods which have seen such dramatic declines in value. 

None of this implies that Garfield Park should be written off. It’s a neighborhood with many assets, including an attractive built environment, a park with a major tourist attraction, and good public transportation. Nevertheless, the short-term prospects for selling a renovated home in Garfield Park to an owner occupant are not good. Demolition is another option, but this home has not been the subject of any 311 vacancy complaints or the site of an unusual number of crimes. It’s also a masonry building that fits the area’s historical character -- why remove an asset from the community?

<img src="/img/posts/cclb-graph2.png">
_Single family home median transaction price in Grand Boulevard_

The situation in Grand Boulevard is rather different. While its foreclosure rate is also high relative to the rest of the city -- in the 81st percentile -- it’s significantly lower than in Garfield Park. Median home prices and the percentage of low-value transactions are in the middle of the pack among the city’s community areas, and per-capita spending on permitted construction is among the highest. Crime and vacancy are lower, and mortgages are being written at over six times the per capita rate of West Garfield Park. So people are investing in Bronzeville, and property values are at the level where private development can make economic sense under the right circumstances. 

Stepping back from the hypothetical for a moment, the record shows that the Garfield Park property remains vacant while the Grand Boulevard property sold earlier this year.

#### The Challenge

From a data scientist’s perspective, each property that changes hands (or sits unsold) tells us something about the state of its neighborhood. How can these data points be turned into a plan of action for the Cook County Land Bank?

<img src="/img/partners/landbank.jpg">

That plan may look completely different across neighborhoods. If the Land Bank acts in the most troubled markets, its decisions may center around disamenities such as unsafe buildings, crime hotspots, and so on. 39XX W Van Buren may not be an ideal candidate for acquisition in part because it does not seem to be degrading its neighbors’ quality-of-life. In stronger markets, the agency may focus on amenities such as jobs, open space, affordable housing near public transit, and the like -- priorities that will be set by the Land Bank’s political leadership in consultation with the community. 46XX S Evans may be an attractive target for housing development because of its location near a retail corridor and a CTA stop.

Moreover, the plan needs to be designed to address market failures. 46XX S Evans sold without the Land Bank’s intervention, which means no taxpayer money was put at risk -- that’s a victory, assuming the new owner is responsible. 39XX W Van Buren didn’t sell. But why? For each vacant property, there is some underlying reason why the private market has not put it to use. In Grand Boulevard, where good properties are likely to move, the market for a given vacant home may be gummed up by a large unpaid tax lien or a title complication -- problems the Land Bank can help solve. In Garfield Park, there may just not be sufficient buyer demand. It will be important for the agency to distinguish these cases, lest it find itself spending its entire budget maintaining properties that don’t sell for decades.

The Land Bank can try to pull neighborhoods out of the foreclosure morass, or it can try to keep other neighborhoods from falling into it. Neither path is easy, but the former would certainly require vastly more resources. Attacking the latter and more achievable challenge first might be the best way to start.

#### How Does Data Fit In?

The DSSG team -- Sophia Alice, Skyler Whorton, Evan Misshula, and mentor Tom Plagge -- worked with the Land Bank to inform these choices with data. 

<img src="/img/posts/cclb-team.png">

Among the factors we considered were:
* Basic neighborhood characteristics such as building types, population trends, and crowding.
* Economic characteristics such as income, property investment, and access to jobs.
* Real estate market trends such as units sold, prices, mortgages, and foreclosures.
* Policy variables such as zoning, community plans, and transportation infrastructure.
* Possible red flags such as EPA-designated brownfields.

With guidance from experts at DePaul University’s Institute for Housing Studies, we computed indicators for each community within the county, and then put them in context by ranking them relative to comparable areas. We also assembled some property-specific characteristics such as vacancy complaints, crimes, and recent sales and foreclosures. We used these data to model aspects of the housing market: by seeing how foreclosures spread, by finding the average price impact of amenities and disamenities, and so on.

<img src="/img/posts/cclb-tool4.png">
_A screenshot of the DSSG app built for Cook County Land Bank_

The CCLBA Board of Directors can use these data and models to ask questions about each candidate property: Is this a parcel that is likely to sell on its own? How much demand for is there within the property’s sub-market for rental housing, owner-occupied housing, and retail? Does the area lack some amenity that a government agency (like a school or park district) might be able to supply? And how might treating this one property affect its neighbors?

“As Chairman of the largest land bank in the Country, I was thrilled to partner with the Eric & Wendy Schmidt Data Science for Social Good Fellowship to help us kick start what will be the backbone of the Cook County Land Bank’s mission –- access to smart and timely data," said Bridget Gainer, Cook County, IL Commissioner and Chairman of the Cook County Land Bank. "The Cook County Land Bank fellows provided invaluable analytical tools that will help us return thousands of vacant and abandoned properties back into productive and sustainable community assets.” 

Data and models can inform these decisions, but only once the Land Bank engages the stakeholders in each community to come up with mutually acceptable criteria. Once they do, the ingredients will be in place to set a clear, justifiable plan of action for putting vacant properties back to work.

To learn more about our project, visit our [GitHub page](https://github.com/dssg/land-bank). 