# PISA Data Exploration
## by Ogunlana A. Adejoke


## Dataset

The Program for International Student Assessment (PISA) is a survey of students' skills and knowledge as they approach the end of compulsory education. It is not a conventional school test that focuses on examining how well students have learnt the school curriculum; rather, it is an international assessment that tests how well students are prepared for life beyond school.

> There are 5233 students in 2 economies, all Non-OECD member countries that took part in the PISA assessment of reading, mathematics and science. In addition to that, the dataset also consist of 636 variables/features describing each student’s background, personality and academic achievement. Some of the variables were repeated and some were condensed so effort was made to select the important features/variables necessary for the analysis. The dataset was gathered from Udacity hosted site available [here](https://docs.google.com/document/d/e/2PACX-1vQmkX4iOT6Rcrin42vslquX2_wQCjIa_hbwD0xmxrERPSOJYDtpNc_3wwK_p9_KpOsfA6QVyEHdxxq7/pub). In addition, the PISA data dictionary was obtained from [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud507/pisadict2012.csv&sa=D&ust=1554482573645000).

Feature Engineering was done to produce:
> - Academic Performance: the average of all student's assessment in mathematics literacy, science literacy and reading literacy.
> - Average Learning Time (mins/week): the average of all learning time spent by students

Some other selected variables analyzed include:
> - Country (Nominal/Categorical variable)
> - Gender (Nominal/Categorical variable)
> - Age (Continuous/Numeric variable)
> - Grade (Discrete/Numeric variable)
> - Class Repetition (Ordinal/Categorical variable)
> - Immigration Status (Ordinal/Categorical variable)
> - Academic Performance - _Engineered variable_ (Continuous/Numeric variable)
> - Average Learning Time (mins/week) - _Engineered variable_ (Continuous/Numeric variable)
> - Perseverance Level(Give up easily) (Ordinal/Categorical variable)
> - Highest Educational Level of Parents (Ordinal/Categorical variable)
> - Parent's Highest Educational Years (Continuous/Numeric variable)
> - Teacher Support (Continuous/Numeric variable)
> - Class management (Ordinal/Categorical variable)
> - Student-Teacher Relation (Continuous/Numeric variable)
> - Attribution to Failure (Ordinal/Categorical variable) and others

For the data wrangling steps, the dataset was assessed to identify data quality and tidiness issues. Some of which are:
1. Condensing the plausible values in mathematics, reading and sciences by finding the average respectively and renaming the resulting values in a column called “Academic performance”.
2. Condensing the Learning time(minutes per week) columns for Science, text language and mathematics by finding the average of these in a new column called Average learning time
3. Renaming the necessary columns appropriately for better representation/information purpose.
4. Dropping all redundant columns with more null values as they are regarded as low-level information columns.
5. Fixing all formatting error in the Class repetition and Highest Educational Level of Parents columns and fixing the data type where appropriate.

Thereafter, effort was made to clean-up these issues and the resulting dataset was saved for further data exploration. 



## Summary of Findings

   In the PISA dataset exploration, I discovered that most students that took part in the assessment came from Albania than from the United Arab Emirates, however, students from the United Arab Emirates performed better academically than students from Albania. These students are mostly 15years old and they are more of female gender than male. The assumption of the female students outperforming male students in a range of indicators of academic performance was also validated.  
   
   The relationship between the two engineered variables; average learning time and academic performance reveal that there is a positive correlation between these two variables, although very weak. This implies that as students spend more time in learning there is the higher probability of the students performing better than they did before in their academic studies. 
   Moreover, more native students partook in the assessment than the first-, and second-generation immigrant students. But my analysis reveals that the immigrant students perform better academically than the native students, hence immigration status has an impact on the academic performance of students in the PISA dataset analyzed. 
   Of note is the finding that the both native and immigrant students are most likely NOT to repeat a grade than they are to repeat a grade. For the immigrant students, those who did not repeat a grade performed better academically than those immigrant students that repeated a grade irrespective of whether they are first-, or second-generation immigrants. It can also be noticed that the immigrant students that repeated a grade performed better academically than the native students; irrespective of whether they repeated a grade or not. 
   It is also worth mentioning that students of parents with higher levels of education or spent higher number of years in education, performed better academically than those with lower level of education; as the former may have an enhanced regard for learning probably from learned parents, more positive ability beliefs, a stronger work orientation, and they may use more effective learning strategies than students of parents with lower levels of education. 
   The role of school in preparing students for life was validated as students who performed best academically are prepared for life and better able to make the transition into life beyond school, adulthood and to achieve occupational and economic success. 
   In addition, students that performed the best academically stated that they would likely attribute their failure to teachers not explaining well in class and teachers not getting them interested in the subjects taught. This can be summed up as negative teacher's attitudinal problem.
    Meanwhile, it should be emphasized that students who are not likely to give up easily in their academic studies performed better academically than those that tend to give up easily. 
    Again, students who do not necessarily give up easily, spend more time learning, and thus better academic performance than those who tend to give up easily. More so, whether students REPEATED a grade or NOT, students that are NOT MUCH likely to give up easily performed the best academically while those that are VERY MUCH LIKELY to give up easily are low-performing students. Across all students, students who REPEATED a grade AND are NOT MUCH LIKELY to give up easily scored higher than other students in their academic studies, irrespective of whether the other students repeated a grade or not. 
    Finally, in this PISA dataset, it is unlikely that student-teacher relationship and classroom management promote student's academic achievement.

Besides the main variable of interest, I also looked into the relationships between average learning time and other variables. 
> -I found that immigrant students spent more time learning than the native students. 
> -Also, as expected, students who REPEATED a grade spent MORE TIME learning (to cover up for lost ground) than those who DID NOT REPEAT a grade. 
> -It should also be worth noting that students of parents with higher educational years/level spent longer time learning than students of parents with lower educational years/level. 
> To sum up, I also discovered that irrespective of a student's immigration status, grade repetition status, parent's educational level, or the tendency to give up easily, students who spent more time learning perform better academically than those that spent less time learning.


## Key Insights for Presentation

As regards the presentation, I focus on the major factors/variables affecting the academic performance of students which are:
> - Class Repetition (Categorical/Qualitative variable)
> - Immigration status (Categorical/Qualitative variable)
> - Academic Performance - _Engineered variable_ (Numeric/Quantitative variable)
> - Average Learning Time (mins/week) - _Engineered variable_(Numeric/Quantitative variable)
> - Perseverance Level(Give up easily) (Categorical/Qualitative variable)
> - Highest Educational Level of Parents (Categorical/Qualitative variable)

Then, I began with the introduction of the engineered variables (academic performance and average learning time) using a histogram plot. This was subsequently followed by exploring the relationship between one categorical variable and numerical variable in a barplot and violinplot respectively. Such relationships include: 
> - The relationship between  Perseverance level to give up easily and Student's Academic performance, and
> - The relationship between Class Repetition and Student's Average Learning Time. 

Thereafter, I looked at multi-variable relationships to deduce the factors affecting the academic performance of students. Those relationships include:
> - Effect of Student's Immigration Status and Class Repetition on Student's Academic Performance.
> - Effect of Class Repetition and Perseverance level to Give up easily on Student's Academic Performance.
> - Effect of Class Repetition and Parent's Highest Level of Education on Student's Academic Performance.
> - Effect of Class Repetition and Average Learning Time on Student's Academic Performance.
> - Effect of Immigration Status and Average Learning Time on Student's Academic Performance.

I've made sure to use different color palettes for each quality variable to make sure it is clear. In conclusion, a summary of all findings were documented in the conclusion section of the Pisa_dataset_Part_I_exploration.ipynb.