---
layout: post
title: "Case Foundation: A Hairball to Help Non-Profits Untangle Strategy"
author: John Brock
pic: "case-header.png"
published: true
---
Starting a new nonprofit is a difficult process. Besides choosing a mission, developing a strategy and hiring employees, a new organization must figure out how they fit into the larger nonprofit landscape and find support. 

“How can I attract supporters?”

“With whom can I partner?”

“What are people saying about me?”

These are just some of the questions nonprofits must answer to produce positive change in the world. And to find answers to their questions, nonprofits are increasingly turning to the Internet. 

Unfortunately, information about nonprofits is scattered across the web, in social media, news articles, charity search engines and databases hidden behind paywalls. Many nonprofits, already facing severe resource constraints, lack the ability to effectively make sense of all this scattered information.

To address this problem, our team -- Kyla Cheung, Giorgio Cavaggion, Ahmad Qamar, myself, and mentor Aron Culotta -- has partnered with the Case Foundation to build the [Giving Graph](http://casefoundation.org/blog/how-new-type-social-graph-could-change-philanthropy).

<img src="/img/posts/case-team.png">

The Giving Graph, first described by the Case Foundation at this year’s SXSW, collects nonprofit-related information from across the web and brings it together in one centralized location. However, having lots of data about nonprofits in one place isn’t the point: What’s really exciting is that having all of this information in one place for the first time allows us to explore the connections between all of that information.

Using the methods provided by natural language processing and social network analysis, we can automatically find links between nonprofits, companies, charitable causes and individuals that would be difficult or time-consuming for a human to infer. Ultimately, the goal is to help nonprofits better understand themselves, better understand their sector, and better answer the questions they care about.

<img src="/img/partners/case.jpg">

#### Finding Similar Nonprofits

For example, imagine you are executive director at [Dogs Deserve Better](http://www.dogsdeservebetter.org/), a nonprofit dedicated to the well-being of dogs. To help the dogs of the world, you need money. So you ask yourself “Which companies should I approach for support?” Our approach is to answer this by addressing a slightly different question: “Which companies support nonprofits similar to me?”

<img src="/img/posts/case-connections1.png">

Why this question? Because if you knew 3M supported the nonprofit Canine Partners, and that Canine Partners was similar to your nonprofit, you could go to 3M and say, “You seem to care about the treatment of dogs. You should give us money, too.” Similarly, if you knew Native Foods Cafe supported PETA, and your nonprofit was similar to PETA, you might expect Native Foods Cafe to support your nonprofit as well.

There are two steps to answering the question, “Which companies support nonprofits similar to me?” The first part is to find similar nonprofits. The second part is to find companies that support those similar nonprofits.

To find similar nonprofits, we’re using three resources: mission statements, nonprofits’ Twitter followers, and nonprofits’ tweets.

<img src="/img/posts/case-statements.png">

For mission statements, our basic approach is to count how many words they have in common. For example, if two nonprofits’ mission statements both use the words “education” and “dogs”, they may be similar. More precisely, we create a vector for each mission statement, where each dimension of the vector represents a word. The value of each dimension is the number of times that word appears in the mission statement. For example, here are two word vectors constructed from the above mission statement excerpts.

<img src="/img/posts/case-vectors.png">

Of course, words will tend to appear more often in longer mission statements than in shorter mission statements. Additionally, some words, like “the” and “and”, tend to appear more often than other words. To control for these issues, we normalize the vectors using a technique called [TF-IDF](http://en.wikipedia.org/wiki/Tf%E2%80%93idf) (term frequency-inverse document frequency). Finally, we compute the cosine similarity between the two normalized vectors, i.e., the cosine of the angle between the two vectors. This produces a number between 0 and 1, which is what we use as our nonprofit similarity score.

<img src="/img/posts/case-twitter.png">

For Twitter followers, we look at how many followers are shared by two nonprofits’ Twitter accounts. If two nonprofits share a lot of the same followers, they may be similar.

For tweets, we use an approach like the one we use for mission statements: looking for nonprofits whose tweets share words in common. Here’s a “hairball” visualization of nonprofit similarity based on tweets (created in Gephi, an open source network visualization application). Each dot represents a nonprofit’s Twitter account, with lines connecting similar nonprofits. A community detection algorithm groups the dots so that nonprofits with highly similar tweets are placed together (for details on the community detection algorithm used by Gephi, ["Fast unfolding of communities in large networks."](http://arxiv.org/abs/0803.0476)).

<img src="/img/posts/case-zoom.png">

This visualization shows nonprofits in the animal sector, but let’s zoom out and look at the visualization for all two thousand nonprofits currently in our database:

<img src="/img/posts/case-hairball.png">

To build this full visualization, we compared the tweets for each pair of nonprofits. For the two thousand nonprofits in our database, this meant comparing the tweets for two million different pairs of nonprofits. Different groupings of nonprofits naturally arise out of these comparisons, and one can zoom in on the visualization to manually label the different groupings. For example, let’s zoom in on the human rights grouping:

<img src="/img/posts/case-zoom2.png">

Here you can see nonprofits that fall into the high-level category of human rights, but subgroupings are also evident: in the upper-left are nonprofits related to domestic violence. To the right of those are LGBTQ rights organizations. On the right side of the image you can also see a grouping of nonprofits supporting causes in the developing world.

#### Adding Support to the Hairball

Now that we can determine that two nonprofits are similar, how do we determine that a company supports a nonprofit? One source of information is the news. Our system automatically looks for news articles that mention a nonprofit and company together in a supportive context, and records a link between the nonprofit and company. A second source of information is nonprofit websites. Just as with news articles, if a nonprofit’s official website mentions a company in a supportive context, our system records a link between that nonprofit and the company.

Currently, to determine that the context is a supportive one (as opposed to, say, a nonprofit and company being mentioned together because the nonprofit is criticizing the company) we simply look for key phrases that indicate support, such as “supported by”, “donated to” or “made possible by." If warranted, we may try more sophisticated sentiment analysis methods in the future.

<img src="/img/posts/case-news.png">

Now we can finally answer the question, “Which companies support nonprofits similar to me?”: By comparing mission statements, Twitter followers, and tweets, we found similar nonprofits. And by analyzing news articles and nonprofits’ webpages, we found companies that support those similar nonprofits. If you’re the executive director of Dogs Deserve Better, you can now see that 3M and Native Foods Cafe are potential supporters.

Of course, there are other questions that nonprofits care about. Other areas to explore include nonprofit collaboration (with whom should I write a grant?), branding (how is the language I use similar or different from the language used by other nonprofits?), and board member connections (to whom am I connected at other nonprofits or companies?). All of these questions are answerable from data that are already out there on the web. It’s just a matter of collecting them and finding the links between those pieces of data.

To learn more about our project, visit our [GitHub page](https://github.com/dssg/givinggraph). 