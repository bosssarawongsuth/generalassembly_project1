# GA Project 1: SAT Student Performance & Benchmarks
## Jetnipat Sarawongsuth 
### Scenario and Problem Statement

I work for an independent research organisation in West Virginia where SAT has recently become compulsory. [[Source]](https://www.wsaz.com/content/news/All-WVa-high-school-juniors-to-begin-taking-SAT-exam-beginning-Spring-2018-444248263.html#:~:text=The%20West%20Virginia%20Department%20of,old%20standardized%20test%2C%20Smarter%20Balanced.) I have been contacted by a school in that state to provide them with some advice and guidelines to the teaching staff to help
- Identify students who are thriving and require greater challenges.
- Identify students who require additional academic support.

Currently the school is only requiring Grade 12 students to do SAT exam with other Grades doing the school's own internal exams. The school is also exploring other options for these Grade 8-11 students in this regard as their internal grading system is not standardised. 

Ultimately the school would like to ensure that the students across Grades 8-12 are on the right tracks to achieving the scores they need in order to study in their intended higher education institues and subjects. Additionally, the school would also like to know how the other states in the country are performing in the SAT and what the current trends are so they can better prepare the students.

### Datasets

#### SAT_RESULTS DATASET [[Source]](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|state|object|sat_results|The name of the State| 
|participation_2017|float|sat_results|The 2017 participation percentage| 
|erw_2017|int|sat_results|The average 2017 SAT score for Evidence-Based Reading and Writing section| 
|math_2017|int|sat_results|The average 2017 SAT score for Math section| 
|total_2017|int|sat_results|The average 2017 SAT score for both sections| 
|participation_2018|float|sat_results|The 2018 participation percentage| 
|erw_2018|int|sat_results|The average 2018 SAT score for Evidence-Based Reading and Writing section| 
|math_2018|int|sat_results|The average 2018 SAT score for Math section| 
|total_2018|int|sat_results|The average 2018 SAT score for both sections| 
|participation_2019|float|sat_results|The 2019 participation percentage| 
|erw_2019|int|sat_results|The average 2019 SAT score for Evidence-Based Reading and Writing section| 
|math_2019|int|sat_results|The average 2019 SAT score for Math section| 
|total_2019|int|sat_results|The average 2019 SAT score for both sections| 

#### SAT_COLLEGE_MAJOR DATASET [[Source]](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|major|object|sat_college_major|The intended College Major for SAT takers|
|test_takers|int|sat_college_major|The number of test takers|
|percent|float|sat_college_major|The percentage of SAT takers choosing the major|
|total|int|sat_college_major|The average SAT score for both sections combined|
|erw|int|sat_college_major|The average SAT score for Evidence-Based Reading and Writing section|
|math|int|sat_college_major|The average SAT score for Math section|


#### SAT_BY_COLLEGE DATASET [[Source]](https://www.compassprep.com/college-profiles/)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|school|object|sat_by_college|The name of the college/university/school|
|applicants|int|sat_by_college|The number of applicants for the school|
|accept_rate|float|sat_by_college|The proportion of applicants accepted into the school|
|sat_25_percentile|float|sat_by_college|The 25th percentile of SAT Scores for accepted applicants|
|sat_75_percentile|float|sat_by_college|The 75th percentile of SAT Scores for accepted applicants|


#### SAT_GPA_GRADE_2019 DATASET [[Source]](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|gpa|object|sat_gpa_grade_2019|The grade received at junior/high school|
|academic_grade|int|sat_gpa_grade_2019|The Grade (Year Group) of the student|
|test_takers|int|sat_gpa_grade_2019|The number of test takers within the GPA category|
|test_taker_pct|float|sat_gpa_grade_2019|The percentage of students within the GPA category|
|mean_total|int|sat_gpa_grade_2019|The average SAT Scores for both section|
|mean_erw|int|sat_gpa_grade_2019|The average SAT score for Evidence-Based Reading and Writing section|
|mean_math|int|sat_gpa_grade_2019|The average SAT score for Math section|
|met_both_benchmarks|float|sat_gpa_grade_2019|The proportion of students who met the benchmark scores for both sections|
|met_erw_benchmarks|float|sat_gpa_grade_2019|The proportion of students who met the specified benchmark scores for ERW section|
|met_math_benchmarks |float|sat_gpa_grade_2019|The proportion of students who met the specified benchmark scores for Math section|


#### SAT_BENCHMARK DATASET [[Source]](https://collegereadiness.collegeboard.org/about/scores/benchmarks)

|Feature|Type|Dataset|Description|
|---|---|---|---|
|red_erw|int|sat_benchmark|The red band benchmark score for Evidence-Based Reading and Writing section|
|red_math|int|sat_benchmark|The red band benchmark score for Math section|
|total_red|int|sat_benchmark|The combined red band benchmark score for both sections|
|yellow_erw|int|sat_benchmark|The yellow band benchmark score for Evidence-Based Reading and Writing section|
|yellow_math|int|sat_benchmark|The yellow band benchmark score for Math section|
|total_yellow|int|sat_benchmark|The combined yellow band benchmark score for both sections|
|green_erw|int|sat_benchmark|The green band benchmark score for Evidence-Based Reading and Writing section|
|green_math|int|sat_benchmark|The green band benchmark score for Math section|
|green_total|int|sat_benchmark|The combined green band benchmark score for both sections|
|academic_grade|int|sat_benchmark|The Grade of the students for the benchmark level|





### Summary of Analysis

Based on the research, West Virginia is one of the worst performing state in the country when it comes to SAT exams. This applies to both the Evidence-based Reading and Writing and Mathematics section. In 2019, West Virginia had an average of 943 points in Composite SAT Score. This is well below the recommended level at 1010 as advised by SAT's College Board. The SAT ERW score in West Virginia was 483 which is just over the benchmark at 480. The SAT Math score in 2019 was a shocking 460. This is 70 points below the benchmark for college readiness. Schools should place more emphasis on Mathematics.These below average results in WV could be due to the recently introduced requirement for all high schools in West Virginia to include SAT as a part of the School Day Exam. The sudden change in the rules may have had an impact on the students as well as teachers' preparedness for the exam.

### Conclusion

As such this study has given some rough guidelines on what educators should expect from students at different Grades. The study aims to encourage schools to adopt the standardised PSAT exams for students in Grade 8 to 11. This will undoubtedly help them better prepare for SAT exmas. In the meantime, schools should be able to use the provided GPA grading scheme/PSAT Score Equivalent to help monitor students individual performance. The benchmarks provided by SAT's College Board can help with ensuring that students are on course to being college ready.

In terms of college majors, across all of the subjects, the mean SAT composite score is a reasonable 1059 which is comparable to the benchmark. The mean for ERW is 535.5 compared to green band's benchmark of 480. The mean SAT Math score is 523 which is just under the benchmark at 530. The most popular majors are in the science and engineering field with majors such as 'Health Professions and related Clinical Sciences', 'Business Management Marketing' and 'Engineering' topping the list. Students who are interested in these field should be advised that the average SAT scores for these candidates are 1088, 546 and 542 for composite, ERW and Math respectively. It shouldn't be surprising that there is a larger mean for the Math section as the field are heavily reliant on Mathematics.

Finally, when it comes to choosing the colleges, there is a large range in the acceptance rate for colleges ranging from 4.3% up to 99.9%. More competitive colleges are certainly very selective about choosing the right candidates. Some of the more competitive colleges include Stanford University (4.3%), Harvard College (4.7%) and Princeton University (5.5%). These top colleges have very high SAT scores for enrolled students. For example, at Harvard College, the top performers (75th Percentile) scores around 1580, only 20 points below the maximum score. This is a big jump from the average of other college's top performers which is around 1358. It should be noted that eventhough these are the most prestigious colleges, they are in no way the colleges with the most applicants. That title goes to University of California - Los Angeles with over 100,000 applicants at 12% acceptance rate.




