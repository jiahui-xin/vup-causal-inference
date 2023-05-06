# vup-causal-inference

RUC course project: Advanced Statistical Analysis in Spring 2023.

## File folder description

`data.h5` and `vtb.csv` are from https://github.com/wandleshen/vup-data-analysis (`data.csv` is translated from `data.h5` and I added some features on `vtb.csv` to construct `vtb2.csv`.) 

Code is contained in *vup.Rmd* and the output file is `vup.html`. 

My presentation slides is `presentation.pdf` and final report is `analysis_report.pdf`. `acc_form.docx` is JASA-required author contributions checklist (ACC) form.

Thanks for your reading! If your time is limited, just read `analysis_report.pdf`!


## Data description

Select 50 different virtual hosts and get revenue and engagement data for their last 50 live streams. Their names, projects or unions they belong to, and user IDs are all manually entered into a csv file for subsequent data grabbing.

## Dependency
* Python package:

pandas version 1.4.4 (optional, just to translate `data.h5` to `data.csv`)
* R packages: 

reticulate version 1.28 (optional, just for python interface), GGalary version 2.1.2, pheatmap version 2.1.2, ggplot2 version 3.4.1, grf version 2.2.1, lubridate version 1.9.2, marginaleffects version 0.11.1, randomForest version 4.7-1.1, reshape2 version 1.4.4, MatchIt version 4.5.3, dyplr version 2.3.1, extrafont version 0.11

## Code description

I do data analysis within Rmarkdown file `vup.Rmd`. 

First read data with python virtual environment in ananconda. (You maybe need to modify this part by your environment.) Then use R to do other things: EDA, random forest, regression adjustment, causal forest and matching method with both regression adjustment and causal forest. 

I will show both regression adjustment and causal forest with(out) matching method. The results of different methods are quite similar.

## Main results

Overall, more viewer exposure can bring more benefit. While if conditioning on viewer exposure, affilliation of vup still makes about 20% difference but whether starting live on weekends or not makes no difference.

## Acknowledgement

So many thanks! Thank https://github.com/wandleshen/ for his data. Thank https://weibo.com/u/7743187451 for her love. Thank Prof. Ma for his kindness.
