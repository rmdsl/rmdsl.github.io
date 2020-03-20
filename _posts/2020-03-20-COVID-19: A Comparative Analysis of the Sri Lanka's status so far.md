---
title: "COVID-19: A Comparative Analysis of the Sri Lanka's status so far"
comments: true
---

---

Corona Virus has shaken the world. People are gathering in [Facebook groups to be responsible citizens and fight against the virus](https://www.facebook.com/groups/1104689606534855/)!

The Government Medical Officers' Association has recently [tweeted](https://twitter.com/GMOAMU/status/1240598713652764672) with an implication that we are in a worst state than Italy. They have added an image that shows a comparison of the COVID-19 Confirmed Counts on the first 14 days between in Sri Lanka and Italy. It's unclear how GMOA has obtained and prepared that data so that they can be comparable. Since they do not provide details into how they've prepared the data, we'll have a look at the [data from a Johns Hopkins University's GitHub repository](https://github.com/CSSEGISandData/COVID-19/blob/master/csse_covid_19_data/csse_covid_19_time_series/time_series_19-covid-Confirmed.csv) ourselves.

![Tweet By GMOA](https://drive.google.com/uc?export=view&id=1Lkb5Dbma3ElYy3WfrG3L0Q5HbFDy9jAm)


**Note:** *This is by no means a challenge to the claim made by the GMOA. They have well qualified epidemiologists and they know way better than a person just analyzing the data. The goal here is to add a different dimension to the analysis.*

## Overall Growth

![overall confirmed count](https://drive.google.com/uc?export=view&id=1-8R5BvHnTwn4uYDcQ1vSBqBCKkO6-oj3)

**Fig. 1:** Data for the countries: `"Sri Lanka", "India", "Pakistan", "Italy", "China", "S. Korea", and "Singapore"` Left: Overall Confirmed Count Over Time, Right: Log(Overall Confirmed Count) Over Time

China is at the top, Italy is growing faster. If you pay attention to the Italy's curve (logarithm), you can notice that Italy has had a value below 10 betweeen 2/1/20 to 2/21/20 and after these 20 day period it is growing rapidly.

This observation suggests that there should be a focus on the Confirmed Cases Count variation in first n days since the day when a country has passed a certain number of patients (say 3, for example).

Reasons are:
1. If you look at the data, some countries seem to have spent a long time in a certain number of patients before it started to kick off (for example: Sri Lanka had a count of one due to the Chinese patient and Italy in Fig. 1.). 
2. Since different countries got the spread in different timelines, it would be a bit hard to draw them across an absolute time axis and compare them because of different scales.

Let's have a look at some of the countries that have a remarkable growth and their relative progress of the total Confirmed Cases in the first `n` days since passing the threshold.

## First 45 days in Italy, Iran, Spain, Germany, US, and France since passing a total Confirmed Count of 3

Some Asian nations that handle the situation well (China, South Korea, and Singapore) are purposely ommitted. Fig 2. shows that Iran (Orange) has passed the threshold of 3 patients and is growing rapidly. Spain (Green) has surpassed the count of Iran in about 20 days. Many days after, Italy has surpassed all and is continuing to lead. Epidemiologists can explain this behavior well. These patterns of growth depend on many communal factors that the numbers do not tell.


![first_45_days_'Italy', 'Iran', 'Spain', 'Germany', 'US', 'France'_italy-3_other-3.gif](https://drive.google.com/uc?export=view&id=1-9tvA8q9lzROOqoYJXQ2cRFzpNzSsX6K)

**Fig. 2:** Data for the countries: `'Italy', 'Iran', 'Spain', 'Germany', 'US', and 'France'` Left: Overall Confirmed Count since passing the count of 3, Right: Log(Overall Confirmed Count) Over Time since passing the count of 3.

## First 14 days in Sri Lanka and some other countries, since passing the total count of 3

Considering the amount of data we have on Sri Lanka, let's have a look at the first 12 days since passing 3 cases. Sri Lanka (blue --) is added to the above countries list to compare Sri Lanka's growth with them.
If you look at the plot, it shows that Sri Lanka is showing a behavior that is almost identical to that of Iran and Spain to during the first five days since passing three patients. Iran and Spain continue to grow in the remaining days and let's hope Sri Lanka's trend would not follow that.

![first_14_days_'Sri Lanka', 'Italy', 'Iran', 'Spain', 'Germany', 'US', 'France'_italy-3_other-3](https://drive.google.com/uc?export=view&id=1-O40lrdC5xLDiW7_SMhDLWS1CU9efeDE)

**Fig. 3:** Data for the countries: `'Sri Lanka', 'Italy', 'Iran', 'Spain', 'Germany', 'US', and 'France'` Left: Overall Confirmed Count since passing the count of 3, Right: Log(Overall Confirmed Count) Over Time since passing the count of 3.

As shown in Fig 3, Italy hasn't taken off yet. The story changes drastically if you've looked at the pattern after Italy hitting 4 confirmed cases.

![first_14_days_'Sri Lanka', 'Italy', 'Iran', 'Spain', 'Germany', 'US', 'France'_italy-4_other-4](https://drive.google.com/uc?export=view&id=1-Oaecl2QaBojZW47rGOIUDD2bwdhIbVf)

**Fig. 4:** Data for the countries: `'Sri Lanka', 'Italy', 'Iran', 'Spain', 'Germany', 'US', and 'France'` Left: Overall Confirmed Count since passing the count of 4, Right: Log(Overall Confirmed Count) Over Time since passing the count of 4.

Fig. 4 shows a completely different picture to that of Fig. 3 and this suggests that the growth pattern should be observed with respect to a previous minimum threshold. This also provides a scary image on how the growth pattern would be for some countries when they've hit a certain threshold for the Confirmed Count.
Again, this is not a good speculation, let's leave that to the epidemiologists to comment on.

## First 10 days in Sri Lanka and some other countries, since passing the total count of 10

Finally, let's have a look at the case when confirmd case count is greater than 10.

![first_10_days_'Sri Lanka', 'India', 'Pakistan', 'Italy', 'Spain', 'Singapore'_italy-10_other-10](https://drive.google.com/uc?export=view&id=1-OoSPjRe1kX02bvwc044TOw9isMNSVj1)


**Fig. 5:** Data for the countries: `'Sri Lanka', 'India', 'Pakistan', 'Italy', 'Spain', 'Singapore'` Left: Overall Confirmed Count since passing the count of 10, Right: Log(Overall Confirmed Count) Over Time since passing the count of 10.

When the count is larger than 10, Italy is having a way bigger growth than the rest! And Sri Lanka hasn't picked up that much. This might be providing relief for Sri Lankans that got panicked after seeing the image posted by GMOA. But, many factors might account to this growth and there is not enough knowledge to comment that a certain country would not exhibit a such growth like Italy when hitting a particular threshold! Given the exponential nature of the growth, it's certainly a good idea stay at home quarantined!

The code to generate the plot is available as a github gist [in this link](https://gist.github.com/rmdsl/8d17fefdad0a46e702d95320b561a3f8).

{% if page.comments %}
{% include disqus.html %}
{% endif %}

