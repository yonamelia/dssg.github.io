---
layout: post
title: "Mining Data, Making a Difference"
author: Rob Mitchum
pic: "dssg-postits.jpg"
---

In June, it was just rows and rows of data: property assessments, school records, smart meter readings, contract bids, and census results. By the end of August, this raw material was transformed into tools for detecting international corruption and political earmarks, predicting buildings that pose lead hazards and students at risk of dropping out, and suggesting strategies to fight maternal mortality, unemployment, and homelessness.

For the second year of the Eric & Wendy Schmidt Data Science for Social Good Summer Fellowship, 48 fellows from around the world worked on 14 projects that helped non-profits and government agencies do more with their data to improve the world. Beyond the accomplishments of the 12-week program, the fellowship hopes to seed a new, international community of data-savvy minds driven to make an impact that goes deeper than click rates.

“The primary goal of this fellowship was to train these students to not only solve real problems but problems with social impact,” said Rayid Ghani, director of the fellowship and researcher at the Computation Institute and the Harris School of Public Policy. “Our hope is that these fellows will not only go out and continue this work, but they’ll also start forming more local communities which will evolve into a larger set of people who care about these issues, who care about using their data science skills to make a social impact.”

This year, fellows from the United States, Mexico, Colombia, Australia, and Nigeria worked with project partners including the World Bank Group, Chicago Public Schools, the Office of the President of Mexico, Enroll America, and the City of Memphis to build new data-driven tools and generate novel, actionable insights for the organizations.

On August 19th, the fruits of the fellowship’s frantic summer were presented at the 1871 startup hub in Chicago’s Merchandise Mart. In a succession of 3-minute talks, the students presented predictive models, interactive dashboards, and policy recommendations to enable partners to use their data to better achieve their mission.

“I was amazed by what they were able to do with our data,” said Bill Thorland, national program evaluator at [Nurse-Family Partnership](http://www.nursefamilypartnership.org/), a project partner in 2013 and 2014. “It’s given us an opportunity to bring fresh eyes in, to look at our problems, to give us some new ideas. It’s been extremely valuable, I can’t put a price on what this is worth to us. I think we’ve turned the corner in the way which we’ll be using data in the future.”

####Summer Camp, with More Statistics

<img src="/img/posts/dssg-circle.jpg">

When the fellows gathered at fellowship’s downtown Loop space in early June, they represented a range of disciplines from computer science, statistics, and machine learning to economics, public policy, psychology, and architecture/design. The early days were spent finding common technical ground -- Python, Scikit-learn, R, iPython notebook, GitHub, SQL, Redshift, and MapReduce. To name a few.

But learning new technical skills was only part of the fellows’ education. Speakers from non-profits such as the YMCA, After-School Matters, Chicago Community Trust, and LISC informed them about problems they face, the data their organizations collect, and the challenges they face in realizing its fullest potential.

Data scientists working at Github and the City of Chicago talked about how they use data to improve services and conduct innovative research. Sociologists from Yale and Ohio State University talked about the use of new computational data analysis techniques to answer social science questions. Panels on workplace diversity and entrepreneurship gave fellows valuable insight into professional careers within and beyond the tech industry.

The diverse knowledge helped the 12 teams of the fellowship -- each made up of four fellows and one experienced mentor -- explore their data and scope their project to achieve a useful result on a brisk schedule. Before jumping into the data, there was a lot of time spent on understanding the problems. One team [traveled to Memphis](http://dssg.uchicago.edu/2014/07/10/battling-blight.html) to work with their Mayors Innovation Delivery Team on strategies to rehabilitate distressed properties. Another [visited the World Bank Group headquarters](http://dssg.uchicago.edu/2014/07/11/world-bank-corruption.html) in Washington D.C., participating in a “Data Dive” on finding signs of corruption in data about the organization’s contracts around the world.

By diving deep into complex problems of education, public health, conservation, and social services, fellows learned what they could provide that would best suit the needs of their partners.

“You could have the best analytical model in the world, but if your partner can’t understand what it’s doing or why they should want to use it, it doesn’t really do that much good,” said Andrew Reece, a graduate student studying psychology at Harvard University. “Ultimately, it’s the partner that we’re trying to help, so they need to really feel and understand what it is we’re doing, in a way that makes sense to them.”

####An Antidote Before The Poison

<img src="/img/posts/dssg-cdph.jpg">

Since bans on leaded paint and gasoline went into effect, the lead levels of Chicago children have dropped precipitously. But in some areas of the city, children still present elevated blood lead levels when tested by pediatricians, reflecting exposure with serious effects upon brain development and other health outcomes.

Finding and mitigating lead hazards in city homes is a leading priority of the [Chicago Department of Public Health](http://www.cityofchicago.org/city/en/depts/cdph.html) (CDPH), yet currently they can only investigate residences *after* an elevated blood lead test from a child who lives there. One DSSG team -- Reece, Alex Loewi, Joe Brew, Subhabrata Majumdar, and mentor Eric Rozier -- worked with CDPH to change that process from reactive to proactive, directing home inspections *before* lead poisoning occurs.

Using data from blood tests, housing records, census demographics, and other sources, the team constructed a model that classified every building in Chicago -- over 1 million structures -- based on their risk of containing hazardous sources of lead. Combined with birth record data on where pregnant mothers and young children live, the model provides a list of high priority houses for CDPH inspectors to check and, if necessary, initiate lead mitigation efforts.

“The data we’re getting from DSSG is helping us rethink the way we do our operations,” said Bechara Choucair, Commissioner of the Chicago Department of Public Health. “When you have limited resources, you have to be smarter in how you use those resources, and that’s exactly what we’re doing.”

<iframe width="640" height="360" src="//www.youtube.com/embed/DbplLXRQquI" frameborder="0" allowfullscreen></iframe>
*Video of the CDPH team presenting at the DSSG Data Fair, held at 1871 on August 19th*

But as the team developed the property risk model for their partners, they realized that it only addressed part of the lead poisoning problem. Children can also be exposed to lead in the environment outside the home, or from objects brought into the residence. So the fellows developed a second model that predicts a child’s blood lead levels through the critical early years of their life, so that physicians can test high-risk children earlier and take other preventive measures to prevent poisoning.

“There’s a lot of different ways that lead can get at a child, and the house is only one of them,” Reece said. “When a child is born, we can now tell how much danger that child is going to be in a couple years from now. That kind of predictive trajectory for both children and homes is something that CDPH has never seen before.”

####Data Science Hits Home

<img src="/img/posts/dssg-mcps.jpg">

Another DSSG team used predictive analytics to support a different sort of early intervention -- providing assistance to students at risk of not graduating high school on time. With student records from [Montgomery County Public Schools](http://www.montgomeryschoolsmd.org/), fellows Everaldo Aguiar, Nasir Bhanpuri, Himabindu Lakkaraju, David Miller and mentor Ben Yuhas built an [“early warning” system](http://dssg.uchicago.edu/2014/08/01/early-warnings-schools.html) using grades, attendance, suspensions, and other features to identify at-risk students. Their work was delivered in the form of an information-rich dashboard that allows administrators to monitor students and get them back on track to graduation with personalized guidance.

A project with Austin-based non-profit [Pecan Street](http://www.pecanstreet.org/) and the [Village of Oak Park](http://www.oak-park.us/) sought to unleash the energy-saving potential of an increasingly common source of big data: [“smart” utility meters](http://dssg.uchicago.edu/2014/07/18/smarter-smart-meters.html). The dense data collected by these devices -- most commonly used today for billing purposes -- contains a wealth of information about a household’s energy use, which can be extracted with the right statistical methods. The team of Philip Ngo, Miguel Perez, Stephen Suffian, Sabina Tomkins and mentor Varun Chandola [built a website](http://smartenergyactions.org) where consumers can upload their energy bill data and receive automated feedback on when they use the most energy, how they compare to their neighbors, and how much of their energy use is due to heating and cooling systems.

“What excited me was being able to give more information to consumers,” said Tomkins, a recent graduate of New York University. “We’re putting power directly into their hands, so that their utility bill will be less opaque. Each household will be able to see, this is how much energy you’re using, and this is how you can make it better. We’re going to give people the power to make better choices.”

Regardless of the project, fellows ended the summer feeling inspired to find careers and pursue projects where they could continue to do work with meaningful social impact.

“I’m from Nigeria, and a lot of the things I was interested in pursuing involved using data science skills to tackle environmental or policy problems that they have there,” said fellow Julius Adebayo, a masters student in Engineering Systems at MIT who worked on a project [examining maternal mortality in Mexico](http://dssg.uchicago.edu/2014/08/04/maternal-mortality-mexico.html). “This summer has shown me that a lot of the things I was thinking were potentially possible are possible and implementable in Nigeria, so that was really helpful for me.”

That reaction, organizers said, fulfilled the fellowship’s primary goal of creating a new community of data scientists with ambitions of improving the world -- work that will continue when Data Science for Social Good returns in 2015, and through the new Center for Data Science and Public Policy at the University of Chicago.

“For me, the most exciting thing to observe is how fellows came to the gradual realization over the last 12 weeks that they actually can make an impact on the world,” said Matt Gee, DSSG co-organizer. “One of the fellows told me ‘This fellowship has changed the way I view the world. It’s changed the way I think about myself and how I can make an impact. And because of it, I’m rethinking what I”m doing next -- I want to continue doing this kind of work.’ To me, that’s the whole point of the fellowship. It’s incredibly rewarding and incredibly exciting to see.”

-----

Join [the DSSG mailing list](http://dssg.us7.list-manage.com/subscribe?u=e926f7378762c658c445fe119&id=6053f5e6e3) to hear about 2015 applications as soon as they open.

[Contact us](mailto: datascifellows@gmail.com) if you want to work with us as a Post-doc, Student, or Project Partner before Summer 2015.

