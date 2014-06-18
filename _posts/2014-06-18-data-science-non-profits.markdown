---
layout: post
title: 'Why Doing Data Science with Non-Profits is Different from Industry'
author: Carl Shan
pic: "nonprofits-ASM.JPG"
"pic-caption": Jill Young of After School Matters talks to DSSG during the first week.
"pic-credit": datascifellows
published: true
---

*Republished from DSSG fellow [Carl Shan's blog](http://carlshan.com/), where is he recapping the summer week-by-week.*

One of the non-profit partners my team is working with came in to the office this past week. They shared with us the overarching problem they’re facing as an organization, and how they hoped our team can shed some light onto potential answers.

After listening to and reflecting upon the needs of our partner, I’ve come to see that the solutions to their problems are likely to not be all that technically sophisticated. What the non-profit needs is not some complex model feeding on thousands of variables and millions of data points. After speaking with a few of the other Fellows, this observation seems to be widely applicable to many of the other projects.

Since then, I’ve been crystallizing a series of observations about how data science as practiced in the non-profit space can be remarkably different from industry data science.

####Needs

In the technology industry, startups and companies can leverage data science to huge payoffs. Airbnb’s data science team mines the rich set of host-visitor data to build [conditional-probability models](http://nerds.airbnb.com/location-relevance/) estimating the likelihood that a user will book in a particular neighborhood. Education startup Knewton uses [Kalman filters to estimate student ability](http://www.knewton.com/tech/blog/2013/11/kalman-filter/).

However, generally speaking non-profits interested in data science are not typically looking for technical wizardry. Rather, the needs of the these organizations seem very straightforward and can be solved with common techniques.

My project partner is asking for an evaluation of the social support programs they put together, so that they can make informed decisions about where to allocate federal funding. Much of that means doing simple statistical analyses, such as looking at percentages, doing cohort analysis, and calculating survival rates.

There doesn’t seem to be any whiz-bang math to introduce here. There’s no need to break out the most cutting edge machine learning algorithms.

To be fair this isn’t something that’s true only of the non-profit space. Many for-profit companies also don’t need sophisticated data science teams. I’ve heard that even now, Dropbox’s data team consists of only three people. Nevertheless, I would wager that having a PhD in machine learning would help you solve more problems at, say, Google than it would at the National Breast Cancer Foundation.

####Where’s The Data?

Beyond the question of needs, a key component of effectively conducting data science is having a wealth of quality data. Even if the goals of non-profits necessitated complex techniques, machine learning algorithms really succeed in finding patterns when they’re being fed large volumes (think giga or petabytes) of high-quality data.

Unfortunately for many non-profits (and for-profit companies as well), this is a dealbreaker.

Non-profits are often launched to advance a praiseworthy social cause. They raise money from individual donors, foundation grants or other charitable giving to fund their organization. However, as non-profit are oftentimes not directly selling a product or service, they need to appeal to the emotional pathos or moralistic beliefs of donors. As a result, powerful personal stories and anecdotes are more potent forces in a non-profits arsenal than metrics or data.

And to be fair, this is very understandable. After all, it’s hard to measure exactly how much effective mentoring is happening as a result of your organization. Or whether women are being effectively empowered. Or if people are living more self-actualized lives. These missions just don’t easily lend themselves to measurement.

Nevertheless, all this poses a problem to applying data science.

Our partner has only been focusing on reliably collecting data for the past two years. Before then, there was some data entry, but it was performed as more of an afterthought. The data collection process also only happens on rare occasions; for instance, when a patient enters or leaves a social service program. There is little information about how an individual patient is doing during the program itself.

As a result, the data we have is fairly sparse, dirty and can only provide a limited perspective in evaluating the effectiveness of social programs.

(Fortunately, there are a few movements to attach greater importance to metrics in the non-profit space. These include ones such as [outcomes-driven philanthropy](http://www.gatesfoundation.org/Who-We-Are/Resources-and-Media/Annual-Letters-List/Annual-Letter-2013) and [effective altruism](https://www.ted.com/talks/peter_singer_the_why_and_how_of_effective_altruism).)

####Black Boxes

In [a seminal 1993 paper](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.103.7226), machine learning researcher Robert Holte analyzed the performance of a variety of different machine learning techniques on common datasets. He surprisingly revealed that simple methods he studied, based off of analyzing only one variable in the data, “are almost as accurate as more complex rules” looking at many more variables! This led him to conclude that any “additional complexity must be justified” in machine learning models.

Nowhere has this statement been made more clear to me than working with non-profits.

It’s likely that most non-profit organizations have never heard of any of the algorithms that are all the rage in the data science field today. As a result, individuals in these non-profits may be reluctant to touch and easily intimidated by black box methods, potentially resulting in situations such as my partner never using anything I build for them.

Holte’s warnings about complexity without justification rings even more true here. Even the most impressive tool is only valuable if others trust it enough to use it. This understanding motivates me to create something that meets non-profits at their level, rather than indulging in sophistication for sophistication’s sake.

####Conclusion

As a DSSG Fellow this summer, I hope to create and ship something that can be successfully used in advancing the causes of the visionary non-profits I’m working with.

As I progress throughout my summer, it will important for me to keep in mind that there will be many difficulties particular to the non-profit space that my team and I will need to carefully navigate. We must learn how to effectively deal with sparse and impoverished datasets, as well as negotiate the tension of building something that’s complex enough to solve a challenging problem, while being simple enough to be trusted by decision-makers.
