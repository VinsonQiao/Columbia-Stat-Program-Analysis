# Columbia-Stat-Program-Analysis
There is a long-lasting rumor among Chinese international students: Columbia Statistics Graduate Program has realatively low admission standard compare to other graduate program in Columbia, such as Mathematical finance and Industrial Engineering and Operational Research. The main reason is that they have heard students in Statistics department are from second to third-tier undergraduate schools. Moreover, they claim that Stats students were not active during the job searching process and most people were not able to jobs.
Most of times, rumors are not based on facts and are untenable. Therefore, our group would like to break this rumor by provide visualized and solid evidence from our research and analysis. Thus, defending and restoring the reputation of our program.

## Description of The Data Source
### I. Data Source
In thie project, we have used 3 major set of data:
Data of students from 2018-2019 Statistics Program
Career outcomes of Stats students in the past two years
General perspectives towards the Statistics program
Our teammate Wensong Qiao is responsible for the data collection. The first data set is obtained from 2018 Statistics Program We-chat group through We-chat API. Since the We-chat group suggests everybody to change their username to the format “Name-Undergrad school-Undergrad major”, we are able to obtain those informations.
The second data set is obtained through the Statistics Program Career We-chat group through the same methodology. We were planning to use the data from LinkedIn. However, LinkedIn has restricted their API.
And the third data set was obtained from a career forum called “1 Point 3 Acres” through their API. We picked the post regarding our program with the most replies and extract all sentiment words.
### II. Data Information
Thr first data set contains 315 observations and 6 variables:
ID (int), Under_Grad_School (fctr)
Under_Grad_Major (fctr)
US_Ranking (int, indicates the ranking of labeled school)
X211 (lgl, “Ivy League” in China), X985 (lgl, another “Ivy League” in China)
Code
### III. Data Limitations
There are two main limitations of our data set. First of all, since we obtained the first two dataset from We-chat, not everbody on the We-chat group fully labeled their information although they are suggested to do so. As a result, we have a lot of missing values in the variable “Under_Grad_School” and “Under_Grad_Major” in the first dataset.
Code
## Number of people who labeled their undergraduate school name:  127
However, since our sample size is relatively large, we are able to mitigate this issue. As you can see, although more than half of people did not label their school name, we still obtain 127 valuable data.
Second issue is that first two dataset only contains informations of the Chinese student’s community. We did not get informations of Stats students from other countries, which could make our analysis a little bit biased. However, among 350 students in our current class, there are around 320 Chinese students, which is about 92% of the student population. We believe just by using the data of Chinese student. Our analysis is well-represented.
Description of Data Import/ Cleaning/ Transformation
Cleaning the first dataset is purely brutal. Since we scarpped the dataset from the We-chat group, the original format was a mess. It contains all kinds of symbols even emojis from people’s username. And the school name is not standardized. For example, somebody would write University of Connecticut as “UCONN”, but someone else would write as “Uconn”. Therefore, I ended up manually input the data into excel. One good thing is that I can directly modify the data to the form I wanted without transformation in R.
