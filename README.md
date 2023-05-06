# vup-causal-inference

RUC course project: Advanced Statistical Analysis in Spring 2023.

## File folder description

Data is from https://github.com/wandleshen/vup-data-analysis. So many thanks to this friend! Code is contained in vup.Rmd and the output file is vup.html.

## Data description

Select 50 different virtual hosts and get revenue and engagement data for their last 50 live streams. The size of such a data set is sufficient for us to perform some simple analysis, but it is not too large, which makes the analysis process too cumbersome. Most of these 50 virtual anchors come from the VirtualReal project (VR is true), but some of them come from other unions or individuals. Their names, projects or unions they belong to, and user IDs are all manually entered into a csv file for subsequent data grabbing.

## Code description

I do data analysis with Rmarkdown. First read data with python virtual environment in ananconda. (You maybe need to modify this part by your environment.) Then use R to do other things: EDA, random forest, regression adjustment, causal forest and matching method with both regression adjustment and causal forest. 
I will show both regression adjustment and causal forest with(out) matching method. The results are quite similar.

## Main results

• With a real-world dataset, I used both regression adjustment and causal forest with(out) matching to exploit causal effect.

• Key assumptions such as unconfoundedness and overlap are hard to verify but the results are similar.

• Given variables *{danmakusCount,timeDuration, watchCount, interactionCount,superchatCount, membershipCount,followers}*, treatment **Independent** has significant causal effect but treatment **Weekend** does not. 

In other words, more viewer exposure can bring more benefit. While if conditioning on viwer exposure, affilliation of vup still makes about 20% difference but whether starting live on weekends or not makes no difference.

## Acknowledgement

So many thanks! Thank https://github.com/wandleshen/ for his data. Thank https://weibo.com/u/7743187451 for her love. Thank Prof. Ma for his kindness.
