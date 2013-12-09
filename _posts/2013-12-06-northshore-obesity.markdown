---
layout: post
title: "NorthShore: mining medical data to tackle the obesity crisis"
author: Allen Lin
pic: "northshore-obesity-header.jpg"
"pic-credit": puuikibeach
published: true
---
Obesity is a rapidly growing epidemic in the US. More than a third of American adults are obese, and another third are overweight. If this trend holds, [42% of American adults will be obese by 2030](http://www.ncbi.nlm.nih.gov/pubmed/22608371), making obesity one of the leading public health challenges of our times.

Excessive weight is bad for people’s health, wallet, and psyche. Obese adults are at increased risk for a lengthy list of diseases, from heart disease to diabetes to cancer. Obesity also puts pressure on already tight healthcare budgets - on average, obese adults have medical bills that are [42% greater than those of normal weight adults](http://content.healthaffairs.org/content/28/5/w822.long). 

Obesity is hard to tackle once it sinks in, so medical experts regard early prevention as the most promising way to stem the obesity epidemic. That’s because physical exercise and good nutrition can keep children from becoming obese in the first place.

####Growth Charts: The Data of Growing Up

To identify children who are overweight or obese, pediatricians use **growth charts** made by the U.S. Centers for Disease Control and Prevention (CDC).

<img src="/img/posts/cdc_chart_male_clean.png">
<div class="small"><a href="http://www.cdc.gov/growthcharts/clinical_charts.htm">Source: CDC</a></div>

This weight-versus-age growth chart depicts how the body weights of American boys vary by age and change over the years.

At the age of two, most boys weigh between 25 and 35 lbs. They gain weight steadily until puberty, when they go through a growth spurt. As boys age, their weights spread out - notice how much wider the range of weights is at age 20 than at age 2.

Over the years, pediatricians record a child’s height and weight at routine office checkups. To detect if the child is overweight or obese, they plot these measurements on such growth charts.
They compare these measurements to the rest of the population using the growth chart’s **percentile lines**. For example, if an 8-year-old boy weighs 70 lbs (shown as a red dot in the above chart), he falls along the “90%” line, meaning he is heavier than 90 percent of 8-year-old boys.

To better understand how doctors actually use growth charts to diagnose childhood obesity, we interviewed several clinicians. It turns out that pediatricians primarily use growth charts to detect unusual growth patterns in children. 

As long as a child follows the same percentile line over time and is not at either low or high extremes, the pediatrician will consider the child to be growing healthily. But a growth trajectory that fluctuates, crossing multiple percentile lines in a short time, can signal unhealthy changes in the child’s diet, physical activity, or metabolism.

Pediatricians also monitor each child’s body mass index (BMI), a way to measure body fat. BMI is calculated by taking the patient’s weight (in kilograms) over the patient’s height (in meters) squared. It’s a ratio - the larger the number, the more weight you have relative to your height, suggesting more fat (or muscle) on your frame. If you’re curious, [you can calculate your BMI here](http://www.nhlbi.nih.gov/guidelines/obesity/BMI/bmicalc.htm).

When physicians find kids with consistently high BMIs (above the 85th percentile), they might tell the parents their child needs to eat healthier or exercise more. However, these lifestyle changes are challenging to pull off, because the entire family needs to follow suit -- after all, the kid most likely eats what the family cooks. Too often, this advice goes unheeded.

<img src="/img/posts/northshore_team.png">

#### The Limits of Growth… Charts

Although growth charts are great way of comparing a child’s height, weight, and BMI to other children, they have two key drawbacks:

- First, growth charts are inherently retrospective. They show you how the child is growing, but tell you nothing about how she’ll grow in the future. 

- Second, kids have different growth patterns, going through growth spurts and puberty at different times. For example, late bloomers might have higher BMIs compared to their peers right before they go into puberty. These same children might subsequently have *lower* BMIs than their peers after puberty, having grown taller in a short amount of time. Simply comparing a child’s measurements to the population average would not account for this.

We wondered if these same measurements could be used to detect obesity in a more forward-looking and child-specific way. So we created an analytics tool for pediatricians to better detect kids who are likely to become obese as they age. In addition to **searching for worrisome fluctuations**, our tool draws on data from thousands of similar children to **predict a child’s growth path** a few years into the future. 

A physician can use this information to start interventions -- such as changing the child’s nutrition and exercise routines -- earlier in the kid’s life. And parents can visualize their child’s future height and weight if they maintain their current habits, amplifying the pediatrician’s warnings and perhaps making them more likely to adopt healthy habits.

#### Mining growth curves from electronic medical records

[NorthShore University HealthSystem](http://www.northshore.org/) is a network of four hospitals in the north suburbs of Chicago. The NorthShore hospitals were among the first to “go paperless” and implement a hospital-wide electronic medical record (EMR) system. 

<img src="/img/posts/northshore_logo.png">

By turning paper-bound medical histories into digital data, EMRs allow researchers to more easily conduct medical studies on routinely collected patient data. Properly mined, these digital records promise to dramatically improve our understanding of human health.

To predict obesity for a single child, we needed data on the growth trajectory of thousands. NorthShore provided us with the height and weight measurements of over 23,000 children, records captured over the past 6 years by the NorthShore EMR system. Of course, the data we received was anonymized so that there was no way to identify individual children. 

A sample of the data we received is shown below (patient IDs have been altered). We have each patient’s gender and race, along with their height, weight, and BMI measurements at different ages.

<img src="/img/posts/data_snippet_deid.png">

Data in hand, we started building growth curves of NorthShore’s young patients. We wanted to see how they stacked up to the CDC’s growth charts, which are supposed to represent growth trajectories of all American children. We first wanted to know what percentage of NorthShore’s patients were overweight and obese.

#### Measuring obesity in NorthShore patients

<img src="/img/posts/bmi_males_quartiles.png">

Here, we can see the BMIs of all male patients in our dataset as they grow into adulthood. (Remember, BMI expresses the balance of a person’s weight and height with a single number, and does a good job measuring their body fat.) The colored lines represent the percentiles in the NorthShore population. 

As you can see, children tend to put on weight relative to their height as they age. The range of patient BMIs also widens across the years.

According to the CDC, adults are overweight if their BMI is greater than 25, and obese if it’s greater than 30. In children, these thresholds are defined relative to the population -- a child is considered overweight if they are in the 85th percentile or greater, and obese if in the 95th percentile or greater. 

The plot below compare NorthShore’s BMI distribution (in solid lines) to that of the CDC sample (in dotted lines), using data collected from children in the early 90’s.

<img src="/img/posts/bmi_males_quartiles_wcdc.png">

Compared to CDC’s sample of the nation’s children, NorthShore patients tend to have greater BMIs. NorthShore’s 85th percentile line tracks the nation’s 95th percentile line, and NorthShore’s 75th percentile line tracks the nation’s 85th percentile line.  This means that 15% of the male NorthShore population is obese, and an additional 10% is overweight. 
Why the difference? It could be NorthShore kids tend to have greater body fat than children across the nation. Or it could simply be that children tend to have greater BMI now than a decade ago. 

#### Once obese always obese?

Having found our baseline, we wanted to know if children who were obese at a young age remained obese throughout childhood. If the same subpopulation of children stay obese over time, then predicting who will end up obese would be easy. However, if the subpopulation of children who are obese changes over time, then identifying children who are obese now would not capture all individuals who become obese later.

<img src="/img/posts/bmi_subset_male_individuals.png">

To investigate this issue, we started by viewing the growth curves of three individual patients who were overweight by age 5, each weighing above the 85th percentile at that point. We followed how these kids grew in subsequent years. We picked this particular age, because these years are critical, as a toddler’s dietary and exercise habits might change once they enter kindergarten and spend more time in school.

As you can see from the above graph, their BMIs diverged as they aged: patient 1 stayed overweight, remaining close to same percentile over the years, patient 2 achieved a healthy weight, dropping to the around the 50th percentile, and patient 3 worsened, becoming obese by moving up to the 95th percentile.

We now have a sense of three particular weight paths overweight children can experience in the early years. But we need to capture the trajectories of *all* overweight-by-5 kids simultaneously. To do so, we can isolate this particular subpopulation and examine how the children “funnel” out over time. 

<img src="/img/posts/bmi_subset_male_zoomed.png">

Here, we picked out all boys who had BMI greater than the 85% percentile (a BMI of 17.3) at age 5, and analyzed how they progressed in the next 3 years compared to the other children. 
The graph shows the 5th, 25th, 50th, 75th, and 95th percentile for the “kids who were obese at age 5” subset as they grow up. 64% of the children remain overweight or obese, but the other 36% do not - notice how the bottom 5th of the subset falls from the 85th population percentile line to almost the 50th population percentile line.

####Predicting obesity with adiposity rebound

The fact that a child who is overweight at an early age might not be a few years later made it more challenging to predict which kids were likely to have weight problems in the future. If early weight wasn’t a perfect predictor of later weight, perhaps we could also identify patterns in a child’s growth trajectory that signal obesity down the road?

A literature search turned up a few papers ([1](http://pediatrics.aappublications.org/content/101/3/e5.full), [2](http://www.ncbi.nlm.nih.gov/pubmed/19057527)) that referenced a physical phenomenon called **adiposity rebound**, when a child’s BMI trajectory dips and then rebounds around ages 5 to 6. These small studies suggested that early adiposity rebound was associated with adult obesity. 

We wanted to know if this phenomenon was detectable in the general population and in routinely collected electronic medical records. If so, these rebounds might be useful as obesity predictors and help guide medical decisions in the field.

So we calculated the age at which individuals undergo adiposity rebound in our dataset, which is the age at which the slope of a patient’s BMI curve turns from negative to positive.

<img src="/img/posts/individual_ar.png">

For example, we estimate that this particular patient’s adiposity rebound occurred at 5.7 years. 

We repeated this calculation for all 4,248 patients for whom we had height and weight measurements at age 5. Using our current method, we were able to find adiposity rebound events for 1,035 of them. 

<img src="/img/posts/ar_hist.png">

It turns out that these events occurred at many different ages. Here is a histogram of patients’ ages at adiposity rebound. The children in our dataset undergo adiposity rebound most frequently between the ages of 5 and 6, which matches what we found in the literature. But we were surprised to find a larger than expected share of patients with rebounds at a very young age, from 2 to 4 years old. 

Having found a way to measure if patients experienced adiposity rebound -- and, if so, at what age -- we were ready to see if this BMI curve signature was in fact predictive of obesity later in life. So we correlated the patients’ ages at adiposity rebound with their BMI percentiles at the end of their personal growth curves.  

<img src="/img/posts/bmi_perc_end_v_age_ar.png">

The scatterplot suggests a relationship: the younger a child is when they undergo adiposity rebound, the higher their BMI tends to be later in childhood. In fact, most of the children who ended up overweight (the dots above the blue line) rebounded before age 6, while most of the ones who rebounded after this age had very low BMIs later on.

To capture this relationship more rigorously, we ran a linear regression model, which sets a line of best fit through the data. Then we measured the model’s “goodness of fit” -- how well the line actually fits the cloud of datapoints we observe -- with an R squared test. We found an R square of .32, meaning that 32% of the variation in the BMI percentile at the end of a child’s growth curve can be explained by his or her age at rebound.

Remember, though, that  a child’s age at adiposity rebound isn’t our only predictor. Our earlier look at initial BMI percentiles hinted that they might also be predictive of later obesity. And indeed they are: a regression of final BMI percentile *only* on initial BMI percentile gives a R squared of .37, meaning initial BMI percentile explains 37% of the variation in later BMI percentile. And if we look at both variables simultaneously -- a regression of final BMI percentile on both adiposity rebound and initial BMI percentile -- the R squared bumps up to .65. 

####Implementing predictive tools in practice

In this post, we explored how adiposity rebound could be used as a predictor for childhood obesity. To our knowledge, this is the first time that adiposity rebound has been studied on routinely collected EMR data collected on a large scale. Because we built our obesity detection tool using only EMR data, it could be built into future EMR systems and used by doctors to make everyday medical decisions. 

Of course, our models are only a first stab at obesity prediction and would need to be improved before being used in the field. For example, we’d want to improve our simple method for teasing out adiposity rebound, and see if it could be detected in a larger share of children. Also, because we only have 6 years of data, adiposity rebound for some of the children in our study may have occurred outside of this period. Another caveat: our current method of finding adiposity rebound is retrospective, as we fitted curves to past growth measurements. We would eventually want to develop a forward looking method that could detect when a patient has just rebounded. 

Once we make the tool more robust, doctors could use it to better predict which children are likely to become overweight or obese, and work with them to develop healthy eating and exercise habits. Parents may also be more willing to change their own habits at home if they knew their children were at risk. Because the best way to stem the obesity epidemic is early intervention, deploying this kind of obesity prediction tool could help tackle one of the greatest public health challenges of our times.

####References

Finkelstein, E.A., Trogdon, J.G., Cohen, J.W., and Dietz., W., 2009. Annual medical spending attributable to obesity: Payer- and service-specific estimates. Health Affairs, 28(5): w822-31.

Finkelstein, E.A., Khavjou, O.A., Thompson, H., Trogdon, J.G., Pan, L., Sherry, B., and Dietz, W., 2012. Obesity and severe obesity forecasts through 2030. American Journal of Preventive Medicine, 42(6): 563-570.

Whitaker R.C., Pepe M.S., Wright J.A., Seidel K.D., and Dietz W.H., 1998. Early adiposity rebound and the risk of adult obesity. Pediatrics, 101(3): e5.

Williams, S.M. and Goulding, A, 2009. Patterns of growth associated with the timing of adiposity rebound. Obesity, 17(2): 335-41.

