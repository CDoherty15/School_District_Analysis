# School_District_Analysis
Module 4 - PyCitySchools with Pandas
# Module 4 

## Overview
- So far have been working on creating data frames in pandas by using school board’s data on the different high schools in the area for Maria to present back to the school bord. The school board has notified Maria the file shows evidence of academic dishonesty. More specifically the reading and math scores for the Thomas High School ninth graders. The school board has requested to just omit the scores from Thomas High School. The next steps will then to find the Thomas High School 9th graders, omit them from the data, and then re-run the code to obtain the new scores and percentages. 

## Results
- Since we omitted a whole grade from a school, some of the results have changed. 
### District summary
##### Old District Summary 
![image](https://user-images.githubusercontent.com/79118630/111917655-a16d1300-8a57-11eb-87f7-00df6abac07d.png)
##### New District Summary
![image](https://user-images.githubusercontent.com/79118630/111917659-a5993080-8a57-11eb-80c5-9ebffc0644cd.png)

- School count and total budget are not effected since we are only removing the Thomas High School 9th grade data, and not the whole school. One thing that sticks out is that the new average math score and all the percentages decreased. What is interesting is that the average reading score did not change but the passing reading percentage went down by 0.3, which was the biggest change out of the 5 score values. This is interesting, that the average reading score change was so minimal that when rounded there was no change, but this changed how many people passed reading. Another note is that the percentage of passing math also decreased, by 0.2. But the percentage of overall passing went down by only 0.1. 
### School Summary
Here we see the school summary before and after removing the Thomas High School 9th graders. 
##### Old School Summary 
![image](https://user-images.githubusercontent.com/79118630/111917755-088ac780-8a58-11eb-938d-e7134c59843c.png)
##### New School Summary 
![image](https://user-images.githubusercontent.com/79118630/111917757-0de81200-8a58-11eb-921f-d1076ffda314.png)

- There isn’t much to compare since we only changed one school’s values. There is a lot of information and stuff to unpack with these two data frames, which will be discThe new values for Thomas High School will be discussed next.
### Thomas High School’s performance
##### Old Thomas High School Summary 
![image](https://user-images.githubusercontent.com/79118630/111917766-1fc9b500-8a58-11eb-8d2a-c95b6dc5d1ea.png)
##### New Thomas High School Summary
![image](https://user-images.githubusercontent.com/79118630/111917764-193b3d80-8a58-11eb-8225-eff19880337e.png)

- We originally had 1635 students, we removed the 461 9th graders and get 1174 students. The biggest change is the per student budget, which is expected since the total school budget is not changed. 
- This time there is a variety of changes with the scores and percentages. Average math score stays the same, while the average reading score increases by 0.1. When compared to the percentages of passing math and reading, the percentage of passing math decreased by 0.1 and the reading percentage decreased by 0.3 even when the score went up. Then the overall passing percentage went down by 0.3. 
### New Scores: scores by grade, scores by school spending, scores by school size, scores by school type
#### Scores by grade 
##### Old Math and Reading Scores
![image](https://user-images.githubusercontent.com/79118630/111917774-27895980-8a58-11eb-90ba-5bee503a852c.png) ![image](https://user-images.githubusercontent.com/79118630/111917784-2e17d100-8a58-11eb-9a34-f9b4b1ce7032.png)
##### New Math and Reading Scores
![image](https://user-images.githubusercontent.com/79118630/111917794-3839cf80-8a58-11eb-9b7f-213c55c163ed.png) ![image](https://user-images.githubusercontent.com/79118630/111917798-3c65ed00-8a58-11eb-930b-2523592d31b0.png)

- Since we only removed 1 grade from 1 school, there aren’t going to be any real changes between the previous and new charts. What this does however, confirms that we have removed the Thomas High School 9th graders from the analysis, as noted by the “nan” in the 9th grade column next to Thomas High School. 
- One thing to that Maria should point out when presenting data is that all of the schools tend to have about the same average score for all grade levels

#### Scores by school spending
##### Old Scores by school spending
![image](https://user-images.githubusercontent.com/79118630/111917807-48ea4580-8a58-11eb-864f-39a524fcace8.png)
##### New Scores by school spending
![image](https://user-images.githubusercontent.com/79118630/111917817-51428080-8a58-11eb-8283-2668b7427892.png)

- We have seen some slight changes in values in the data frames after removing the students, but the per student budget had the biggest change from $638 to $888.53. Originally, we had pretty evenly distributed school count in the spending ranges, where the per student budget had a range of $578 – 655. When we omitted the 9th graders, the school’s total student count changed, but the school’s budget did not change. So this is why we see such a spike in there per student spending and we get a new range of per student budget of $578 – 888.53. 
- Through the spending ranges, the school were distributed by 4, 4, 4, 3. If we use the same spending ranges, the distribution would then be 4, 4, 3, 3, which is only 14 schools. So we include another spending bin to include Thomas High School.
#### Scores by school size
- Thomas High School has 1,635 total students, with 461 9th graders, when we remove the 9th graders, their new total is 1,174 students. Since they still have over 1,000 students, they are still considered to be in the medium school size. So the only the medium school values will be affected.
##### Old Scores by school size
![image](https://user-images.githubusercontent.com/79118630/111917856-7fc05b80-8a58-11eb-8e52-22756c582d60.png)
##### New Scores by school size
![image](https://user-images.githubusercontent.com/79118630/111917872-8cdd4a80-8a58-11eb-8b56-943482cb2573.png)

- We can see that the only really effected vale was the passing math percentage, decreased by 0.4. A lot of the values are very close to the original, this does not mean the code didn’t work properly, we know it does because we get a new passing reading percentage value. With this new outcome, we can make a strong estimate that a lot of the scores from the Thomas High School 9th graders were around the average of other students in medium sized schools. Which is the reason why there is not significant changes in the values. 

#### Scores by school type
- Changing the number of students has zero effects on what type of school Thomas High School. Since it is a charter school, removing these scores will only effect the charter school scores.
##### Old Scores by school type
![image](https://user-images.githubusercontent.com/79118630/111917922-d75ec700-8a58-11eb-9358-91248ad55ec5.png)
##### New Scores by school type
![image](https://user-images.githubusercontent.com/79118630/111917926-daf24e00-8a58-11eb-8973-3bfaf8823a68.png)

- Similar to comparing the school sizes, this time, there wasn’t any significant or major changes when removing the Thomas High School data. We can make a strong estimation, that the 9th grade students at Thomas High School got similar scores to other charter school students. 

## Summary
- There were a couple major changes in the updated school district analysis when removing the
Thomas High School 9th graders.
### Scores by school spending 
- Looking at the scores and percentages by school spending per student might not be the best method for evaluating schools during this presentation of the schools in the area. School size effects when school boards discussing budgeting for the school year, when we remove the student we clearly see that the per student budget dramatically increases. This change actually pushes Thomas High School as an outlier in terms of per student budget. When Maria presents the data about scores by school spending, she needs to decide whether or not to keep or drop the Thomas High School data. We can see in that the values for the “$675<” is just the Thomas High School data because it is the same values as the values in the per school summary data frame. If Maria somehow was able to obtain a different total school budget that would be adjusted for a new student count, then it would be perfectly fine to include this data. But since that is unlikely and unprobeable, Maria should make sure to note that this form of evaluation may not be completely accurate, particularly for the $630 – 644 range. 

