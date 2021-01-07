# Airbnb Pricing Model

## Introduction
Has the COVID-19 pandemic caused a significant difference in the visitation rates for national parks in the United States? Some people have suggested that the pandemic has caused many people to flock to our outdoor spaces and public lands as the only source of refuge during lockdowns; others have pointed out that international visitors have been unable to come to the parks due to travel restrictions and many of the parks have remained closed or re-opened with limited access. It is possible that these effects have canceled each other out or been nonexistent in the first place, in either case leading to steady visitation rates.

The leaders of the National Park Service need to understand how the public is using these spaces so they can ensure that they are staffing the parks at approriate levels. Especially since the parks are a public commodity and the park rangers are meant to help the guests, it would be very bad for the parks to either be overstaffed or understaffed.

## The Data
The National Parks Service collects data about the number of visitors who come to each park throughout the year. They have provided this data for 2020 broken down by month while providing a comparison to the data from the same month in 2019, along with Year-To-Date data in each case. This research will focus on three particular months from 2020 and how they compare to each other: February, April, and August. These three months represent three distinct periods of time during the year: before COVID-19 shutdowns (February), early/peak shutdowns (April) and summertime phased re-opening (August). By comparing the data from these months to the 2019 data, the results will be able to control for seasonal effects and isolate the effects of the pandemic on National Park visitation.

One interesting observation in the data is that a large number of parks have certain months where the number of 2019 visitors is exactly the same as the number of 2020 visitors. Since these parks have tens of thousands of visitors per month, it is very unlinkely that they would have an exact match. One possible explanation is that the 2020 data was unavailable, so the park copied over the 2019 data as an approximation. Even without these data points, the sample size is plenty large enough, so this research simply eliminated those cases from the data sets.

## Methods
For this analysis, the data is already split up into three separate groups, and the variable of interest is already calculated. Since the sample size for each group is large enough (n = 330) the only concern is normality. Since the data is heavily skewed (many more small parks, relatively few mega-parks) we cannot use a parametric test and instead must rely on the Kruskal-Willis test to compare the three groups.

## Results
Looking at the results of the Kruskal-Wallis test, we can conclude that visitation rates in the National Parks had a statistically significant difference between February, April, and August. In February, the parks had a slightly higher number of visitors compared to 2019. In April, the numbers dropped off dramatically as everyone stayed indoors at the onset of the pandemic in the United States. By August, things were opening back up, but visitation rates were still very far below the 2019 levels.

## Recommendation and Discussion
Based on these results, we can conclude that the National Parks have seen similar behavior when compared to other types of destinations in the United States. COVID-19 has made a significant impact on the amount of people visiting the parks this year, and while the most drastic differences were back in spring, there was still a very real lingering effect as summer progressed and the COVID impact did not disappear.

This is very good information for the people in charge of the National Parks. They can take these results and staff the parks to match these visitation rates, knowing that the number of guests is less than normal, but there are still enough guests to warrant the majority of the staff sticking around.

To continue this research and provide even better results, my next steps would be to analyze the complete 2020 data instead of focusing on these 3 particular months. I would also like to break down the analysis by park size, since a very large park like Yellowstone might be seeing a different effect compared to a park that usually only sees a few hundred guests during a normal month.

Other lurking variables that could be introducing bias are the overall weather for the year (maybe 2020 has had a lot of bad weather that would have kept people inside anyways) or even the specific states that the parks are in (the general public in Wyoming might be behaving differently compared to the general public in California).
