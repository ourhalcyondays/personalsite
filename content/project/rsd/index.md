---
date: "2021-06-04T00:00:00Z"
external_link: ""
image:
  caption: 
  focal_point: Smart
  preview: true
  preview_only: false
header:
  image: ""
  caption: ""
links:
- icon: file-image
  icon_pack: fas
  name: Poster
  url: https://drive.google.com/file/d/1SRaFvVckpJWQ_tPyrwycQvgXq2r5-k1H/view?usp=sharing
- icon: brain
  icon_pack: fas
  name: AOPUTC
  url: https://science.mcmaster.ca/pnb/news-events/aoputc.html
summary: My research on leadership behaviour in redside dace! This project was completed for PNB 2QQ3 and presented at the AOPUTC Conference.
tags:
- Research
- Animal Behaviour
- R
title: Simon Says; Leadership Behaviour in Redside Dace
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""
share: false
---
{{< toc >}}

## ABOUT:

**[Simon Says: Leadership Behaviour in Redside Dace](https://drive.google.com/file/d/1SRaFvVckpJWQ_tPyrwycQvgXq2r5-k1H/view?usp=sharing)** is a research project completed for the course PNB 2QQ2 (Independent Research Practicuum) under the supervision of Dr. Sigal Balshine, Dr. Andy Turko, & Avani Pathak. Using Behavioral Observation Research Interactive Software (BORIS), I scored the behaviour of groups of redside dace to see whether factors like size, boldness, temperature preference, and inhibition (a proxy for cognitive ability) predicted leadership in fish. This project was presented at **[AOPUTC](https://science.mcmaster.ca/pnb/news-events/aoputc.html)** (Annual Ontario Psychology Undergraduate Thesis Conference) and placed top 10% out of 200+ thesis presentations.

- **I Learned How To**: use BORIS software to collect data, create boxplots using base R functions, think about data, write an abstract, &  present scientific research.
- **Next I Want To**: learn to create other types of plots in R (besides boxplots), research fish through a more integrative lens (through physiological, molecular, or genetic lens, not only behavioural).
<br/><br/>

---

## 📚 I. Introduction & Background

There is **power in numbers**. And no one understands strength in numbers better than the happy residents of the animal kingdom. This is why so many animals live in groups; wolves, penguins, fish to name just a few.
    
But one limitation of living in a group is that there is a LOT of coordination involved. Animals need to collectively decide where to go, what to eat, and how to act. It is not surprising then, that some individuals in the group often emerge as leaders to help coordinate.
    
However, the factors that determine WHO the leader is in an animal group are not well understood. So for this experiment, we examined leadership behaviour in the redside dace, a species of group-living fish that are really sensitive to temperature. We wanted to know whether factors like temperature preference, body size, boldness, or cognitive ability predicted leadership in fish. And to see whether leaders were consistent over time. In other words, who calls the shots in a group? And what makes these individuals leadership material?

## 🧪 II. Methods

To test this, we placed groups of 3 fish inside a shuttlebox setup made of two tanks connected by a neck.

{{< figure src="Shuttlebox.png" caption="Shuttlebox apparatus." >}}

A temperature difference of 2 degrees existed between the two sides of the shuttlebox. Since the fish are sensitive to temperature, they would between the two sides to set their preferred temperature. We also put clear barriers on both sides of the shuttlebox neck, which the fish had to swim AROUND to get to the other side. Lastly, our trusty camera on top recorded fish activity throughout the 8h trials.


 Now we’re armed with our video data, but which fish behaviours were actually important to track? We measured 2 important types of behaviours: shuttling and inhibition.
 1. First, **shuttling** was when fish swam from one side of the shuttlebox to the other side, and we recorded the number of times the fish shuttled, the position of each fish during the shuttle, and the number of fish involved in each shuttle.
2. Another behaviour was **inhibition**. Inhibition was how much a fish got stuck behind the barrier. Inhibition was used as a proxy for cognitive ability because smart fish learn to avoid the barrier, decreasing their inhibition.

After collecting this behaviour data, I classified fish in each group as either **leaders** or **followers**. Leaders were the fish that led the most shuttles in the group. The other two fish in the group were classified as the followers.

## 📈 III. Results
So after scoring hours and hours of video data until my eyes glazed over, I finally get to the exciting part, the results!

First we compared the **temperature preference**, **size**, and **boldness** of leaders and followers. You can see here that leaders and followers don't differ in size or temperature preference. And lastly we compared the boldness of leaders versus followers. To give you some background about boldness, you can think of it like a measure of how brave the fish are, or a personality trait. In our case, it looks like fortune doesn’t favour the bold and there was no difference in boldness between leaders and followers. 

{{< figure src="RSDplots1.png" caption="t-test, t = -0.47, -0.47, 1.68; p = 0.64, 0.64, 0.11; n = 16 leaders and n = 32 followers" >}}


Next we compared inhibition of leaders and followers over time:

{{< figure src="RSDplots2.png" caption= "t-test; t = -0.67, -0.54, -2.39*; p = 0.51, 0.59, 0.025*, n = 16 leaders and n = 32 followers" >}}

Although inhibition was not different between leaders and followers during the beginning and middle of the trial, if you have a good eye, you’ll catch that by the end of the trial, **leaders had significantly lower inhibition than followers**, which is really interesting!
    
Lastly, we compared the temperature preference of the leaders to the temperature preference of the whole group. We were interested to see whether the leader's temperature preference influence the temperature preference of the whole group, but it turns out these things were not related.

{{< figure src="RSDplots3.png" caption="LM, R^2  = 0.12, p=0.20" >}}

## 💡 IV. Conclusions & Beyond...
 
Overall, our results tell us that leaders were consistent over time and the behaviour of leaders is only different from followers in subtle ways. But one interesting finding was that leaders had lower inhibition by the end of the trial, which tells us that leaders may have greater learning ability compared to followers! So based on these results, we think that cognitive ability may be an important part of leadership in fish. This kind of makes sense, the smart fish are leading the group, making all the right decisions. They help all the troopers survive.

Questions about what makes a good leader are important. Not only because the redside dace are endangered, and leadership can influence their survival. But also because leaders in any group have a great impact, and understanding leaders helps us understand the whole group. If we want to learn anything about social dynamics and its role in fitness, we need to look at leaders. And we need to understand what makes them great.

## 💝 V. Acknowledgements

This project could not have been completed without the generous mentorship of Dr. Sigal Balshine and Dr. Andy Turko who supervised this project for the PNB 2QQ3 course. Special thanks also goes to Avani Pathak; my project is an extension of her thesis work.
