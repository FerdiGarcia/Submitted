# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Testing, Statistical Summaries and Inference

### Problem Statement
To identify any likely factors influencing in various SAT and  ACT participation rates in various states of the United States, based on the provided materials.


### Executive Summary

As the new format for the SAT was released in March 2016, the College Board have undertaken this study to determine:
1. If there are any factors influencing in various SAT and ACT participation rates in various states of the United States.
2. To analyze and identify any trends and patterns that can provide further insight to the rates and scores.

This document will guide the audience across to the phases of the study:
#### 1. Data Import and Gathering:
    a.	Average SAT Scores by State
        i.  The 2017 version was taken from https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/.
        ii. ii.	The 2018 version was taken from (https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/).
    b.  b.	Average ACT Scores by State
        i.	The 2017 version was taken from http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf.
        ii.	The 2018 version was taken from (https://magoosh.com/hs/act/2016/average-act-score-by-state/)
    c.	Below are the data import statistics:
        i.  File Name	# of Rows	# of Columns
                 File Name                        # of Rows   # of Columns   
            -  2017 Average SAT Scores by State 	   51	           5
            -  2018 Average SAT Scores by State 	   51	           5
            -  2017 Average ACT Scores by State 	   52	           7
            -  2018 Average ACT Scores by State 	   52	           7
        ii. Data to all the source data has been successfully loaded to the Jupiter Notebook without errors.
    d.  SAT Score Ranges
        i.  Participation% - % of total students who took the exam in the state
        ii.	Math : expected range between minimum of 200 to maximum of 800.
        iii.Evidence-Based Reading and Writing (EBRW) : expected range between minimum of 200 to maximum of 800.  
        iv.	Total Score : expected range between minimum of 400 to maximum of 1600.
        v.	Participation% - % of total students who took the exam in the state
    e.  ACT Score Ranges
        i.	Participation% - % of total students who took the exam in the state
        ii.	English : expected range between minimum of 1 to maximum of 36.
        iii.Reading : expected range between minimum of 1 to maximum of 36.
        iv.	Math : expected range between minimum of 1 to maximum of 36.
        v.	Science : expected range between minimum of 1 to maximum of 36.
        vi.	Composite : calculated as the average of all subjects: expected range between minimum of 1 to maximum of 36.  

#### 2. Exploratory Data Analysis
    a.  Data completeness and consistency
        i.	The following issues were found in the source files. This was corrected in the source file and re-loaded again.
            1.	2017 SAT
                a.	A “%” character in the Participation column.
            2.	2017 ACT
                a.	A score showed a value “20.2x” under Composite column.
                b.	A “%” character in the Participation column.
    b.	Data Observation points - The following points were observed from the loaded data:
        i.	SAT Summary Analysis (2017vs 2018) – comparison of the result of .describe shows the following:
            1.	Based on
        ii.	SAT – Detail Analysis by States (2017vs 2018)
              -  Iowa	                     50%
              1.	The top 5 performers showing with their Total performance improvements from previous year:
                    State         Total %(2017 to 2018)   
              -  Illinois	               1000%
              -  Colorado	                809%
              -  West Virginia	          100%
              -  Arkansas	               66.67%
              -  Ohio	                     50%

              2.		3 states showed poor performance:
                    State         Total %(2017 to 2018)   
              -  Nevada	                -11.54%
              -  District of Columbia	   -8.00%
              -  Arizona	               -3.33%


#### 3. Data Visualization
The following visualization was generated for this project in the Project 1 Jupyter notebook:
    a.	Display Data - portions of the data-frame was displayed as proof of a successful loading of data:
        i.  Seaborn's Heatmap with Pandas .corr showing correlations between the numeric features.
        ii. Histograms :
              1.  Participation rates for SAT & ACT - highlights the following:
                  -   SAT Histogram: High participation among the low scoring participants, but low participation among the high scoring participants
                  -   ACT Histogram: Low participation among the low scoring participants, but high participation among the high scoring participants
                  -   the above is true for both 2017 & 2018
              2.  Math scores for SAT & ACT - highlights the following:
                  -   SAT Math score trend were similar for both 2017 & 2018; most are distributed between 525 and 550
                  -   ACT Math score trend slightly changed from 2017 to 2018 where the ones who scored between 23 - 24 increased.
              3.  Reading/Verbal scores for SAT & ACT
                  -   SAT improved slightly from 2017 to 2018 where most participants scores improved from 530 to 540 to 550. there was also an increase in participants having a high score of 640.
                  -   ACT improved slightly from 2017 to 2018 where there was an increase in  participants scoring 23.
        iii. Scatterplot :
              1.  SAT vs. ACT math scores for 2017
                  -   the graph shows no correlations between SAT vs. ACT math scores
              2.  SAT vs. ACT reading scores for 2017
                  -   the graph shows no correlations between SAT vs. ACT reading scores
              3.  SAT vs. ACT total/composite scores for 2017
                  -   the graph shows no correlations between SAT vs. ACT reading scores
              4.  Total scores for SAT 2017 vs. 2018
                  -   the graph shows POSITIVE correlations between SAT Total scores
              5.  Composite scores for ACT 2017 vs. 2018
                  -   the graph shows POSITIVE correlations between ACT Composite scores
        iv.  Boxplots :
              1.  The Plot Value for SAT EBRW Reading and Writing 2017/2018
                  -   both years have similar upper and lower quartile (530 - 620). However, 2018 shows  shorter lower whisker, indicating  fewer outliers in  lower scores (from 485 - 500).
                  -   Median slightly decreased for 2018 (from 560 to 550)
              2.  The Plot Value for SAT Math 2017/2018
                  -   both years have similar upper and lower quartile (530 - 615). However, 2018 shows  shorter lower whisker, indicating  fewer outliers in  lower scores (from 485 - 495).
              3.  The Plot Value for SAT Math 2017/2018
                  -   both years have similar upper and lower quartile (525 - 600). However, 2018 shows  shorter lower whisker, indicating  fewer outliers in  lower scores (from 475 - 480).
              4.  The Plot Value for SAT Total 2017/2018
                  -   both years have similar upper and lower quartile (1050 - 1220). However, 2018 shows  shorter lower whisker, indicating  fewer outliers in  lower scores (from 950 - 985).
              5.  The Plot Value for SAT participation 2017/2018
                  -   2018 has a higher upper quartile (69% - 80%).
              6.  The Plot Value for ACT participation 2017/2018
                  -   both years have similar upper and lower quartile (30% - 100%).
              7.  The Plot Value for ACT English 2017/2018
                  -   both years have similar upper and lower quartile (19 - 23).
              8.  The Plot Value for ACT Reading 2017/2018
                  -   both years have similar upper and lower quartile (20.5 - 24).
              9.  The Plot Value for ACT Science 2017/2018
                  -   both years have similar upper and lower quartile (20.0 - 23.25).
              10. The Plot Value for ACT Composite 2017/2018
                  -   both years have similar upper and lower quartile (20.0 - 23.5).
        v.  Additional Plots:
              1.  I  added a scatter plot showing a negative correlation between Participation and Composition scores for ACT.
                  -  The same NEGATIVE is seen for both 2017 and 2018.
                  -  Since there is limited data to explain this, further study is needed to determine the cause of the correlation.
