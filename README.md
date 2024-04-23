# Education Inequality, Location, and Income

## Authors:
Sean Nakagomi, instructed by Dr. Galen Egan

## Requirements:
This project was created using Python via Google Colab.

## Introduction:
This project addresses inequality of educational opportunity in U.S. high schools. Here we will focus on average student performance on the ACT or SAT exams that students take as part of the college application process.

We expect a range of school performance on these exams, but is school performance predicted by socioeconomic factors?

## Data:
This project utilizes two data sets EdGap_data.xlsx and ccd_sch_029_1617_w_1a_11212017.csv. The primary data set is the EdGap data set from EdGap.org. This data set from 2016 includes information about average ACT or SAT scores for schools and several socioeconomic characteristics of the school district. The secondary data set is basic information about each school from the National Center for Education Statistics.

EdGap data

All socioeconomic data (household income, unemployment, adult educational attainment, and family structure) are from the Census Bureau’s American Community Survey.

EdGap.org report that ACT and SAT score data is from each state’s department of education or some other public data release. The nature of the other public data release is not known.

The quality of the census data and the department of education data can be assumed to be reasonably high.

EdGap.org do not indicate that they processed the data in any way. The data were assembled by the EdGap.org team, so there is always the possibility for human error. Given the public nature of the data, we would be able to consult the original data sources to check the quality of the data if we had any questions.

School information data

The school information data is from the National Center for Education Statistics. This data set consists of basic identifying information about schools and can be assumed to be of reasonably high quality. As for the EdGap.org data, the school information data is public, so we would be able to consult the original data sources to check the quality of the data if we had any questions.

The data set EdGap_data.xlsx can be accessed from the Github repository for DATA 3320 in the educationLinks to an external site. folder. 

The data set ccd_sch_029_1617_w_1a_11212017.csv is too large for Github and can be accessed from the google drive link:

https://drive.usercontent.google.com/u/0/uc?id=1HvW2w-o2XZzCm4KTvnb1Bb3BvoAa14BP&export=download.

## Data prep: Sean Nakagomi Education Inequality Data Preparation
I converted the "NCESSCH" column in the "school_info" df to an integer to match up the type with "ed_gap".

I got rid of unusable columns and renamed the columns kept for both the "ed_gap" and "school_info" df's to lower_case, snake_case, and less complicated names.

I got rid of some outlier ACT scores and made some pair-plots to visualize the data.

I joined the "ed_gap" and "school_info" df's via the ID.

I got rid another useless column: "year" and dumped data not related to high school for "school_level."

I looked for and got rid of percent-values outside of [0,1] as well as duplicates.

I identified missing values before splitting up the Training and Testing datasets.

I reclassified the school ID as a string so I could normalize numeric-valued columns and then randomly split the data 80-20.

Lastly, I imputed values to the NaNs in the Training dataset via IterativeImputer.

Clean data: X_train.csv   &   X_test.csv

## Licence:
MIT License

Copyright (c) 2024 Sean Nakagomi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
