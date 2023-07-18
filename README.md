# Evolution_of_the_super_falcons

Hi! So I recently just stepped outside my comfort zone and worked on data I normally would never choose. I chose the simplest approach to achieving a good result and I thought I should write about it.

## Problem Statement
In Nigeria, men’s football enjoys a significantly higher level of popularity than women’s football. This trend prompts a closer examination of the Nigerian women’s football team’s performance and prospects, as one might surmise that their male counterparts have outperformed them. Therefore, this analysis aims to explore the Nigerian women’s team’s history and their past World Cup performances. Additionally, the inquiry endeavors to identify any areas of potential improvement in the team’s performance.

2. Dataset

The dataset worked on is obtained from Kaggle through this <a href="https://www.kaggle.com/datasets/mattop/fifa-womens-world-cup-stats">link</a>. It’s a dataset about the women’s world cup around the world and so It spanned from the year 1991 to 2019 which was the last world cup. It features 36 countries and has 22 columns.

Now, I have very little knowledge of how football works so I obviously got help from my male friends. When I understood what each column meant and what I wanted to do with the dataset, my work became easier.

3. Cleaning and wrangling

The data cleaning was both tasking and easy. Easy because the data wasn’t dirty. Tasking because there were missing data and I could not just drop rows and columns here, I had to research and fill in the values.

Since I wanted to work with only Nigeria, I created a new dataset with only Nigerian countries. Some of the missing columns were the number of red cards/number of yellow cards per match. Since I wanted to understand the performance of the players each year, I was also interested in things that can affect the performance such as the coach at the time, if there seems to be team play, and the players at that time. My metrics were their number of goals, assists, and the number of red and yellow cards per match.

This led to lots of research looking for a site that has all of these records and luckily I found this <a href="https://fbref.com/en/squads/2bbd2880/1995/Nigeria-Women-Stats">one</a>. I would argue the data was scraped off this website in fact because it has all of the data (Almost). This sorted out missing values. Since we had columns on the number of goals and the number of assists, I thought of having a column for the players that scored those goals but that would lead to having multiple values in a cell and then I would have to normalize the data. Instead, I created new data with columns Scorers, Goals, Year, and a foreign key of the first data. The goals and assist columns are binary with 1 signifying that the person scores/assists and 0 means the person did not.

<img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*_Ke5-QWusIO87puuFFecqg.png" />

Finally, I introduced two other columns into the main table called managers and key. The key uniquely identifies each of the records and serves as a foreign key in the Players table.

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*ye44dhoKIXowqOEX4xc31Q.png" />

4. Report Building

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*DzFVD4CkTLNwd7WMP60wzA.jpeg" />

The visualization was done in Power BI. It consists of a Year slicer that is connected to some of the chats and a couple of column charts, a line chart, and a filled map chart.

The first chart is aimed at visualizing the total goals scored each year with the number of red cards and the number of yellow cards. It is obvious that the highest peak for all metrics is in the year 1999 than 2015. It’s also noticeable that the more the team participation, the more likely it is to have a red and yellow card.

The second map chart visualizes the top 5 countries by goals. It is connected to the slicer, so it changes with the year.

The left chart on the third row is an attempt to check if there is an increase or decrease in the number of Nigerian players and their average age as the year increases (Maybe that had an influence on their performance). There seems to be an increase in the average age of players (players are a bit older now) and the total number of players seems to fluctuate around the same range.

The right chart on the third row enlightens more about the manager and the total goals and assists made during their term. It is also connected to the slicer so in case you need to look closer at each manager, then there is the chance to. The analysis shows that Ismail Mabo of the year 1999 had the best term. Followed by Edwin Okon in 2015. Honestly, it is still not a certain fact that it is all because of the manager, hence the closer look at the players.

The final chart compares the total goals and assists of each player. It is also connected to the slicer so the total number of players that scored each year can be viewed.

5. Conclusions

The analysis indicates that the best performance of the super falcons was in 1999. They have the highest number of matches played and also scored their total highest goals. This year was managed by Ismaila Mabo. Nkiru Okosieme scored the highest with 3 goals in total followed by Mercy Akide who played a total of 2 goals and even made 2 assists. Other scorers include Nkechi Egbe, Prisca Emeafu, and Rita Nwadike.

The closest performance to this would be the 2015 performance. Three goals were scored and a total of three matches were played which is one less than the 1999 match. The 2019 match was quite identical to this too.
What can be deduced from this analysis is as below:

The possibility that a more competent manager is needed although this cannot be statistically proven.
The 1999 team seems to be just very strong. Even though the star girl was Nkiru, each of the teammates was as strong as her and the responsibility for success was not solely based on her performance. Unlike the 2015/2019 team. The only consistent scorer was Asisat Oshoala. In 2015, two other teammates scored but in 2019, only Asisat could score. It could also be maybe there isn’t a strong culture of team play. Maybe everyone struggled in scoring even in chances where they could have made an assist (speculations).
What isn’t speculation is that the team had done quite terribly before 2015 and the presence of Asisat led to an improvement in the team’s performance.
Lastly, Football might have just gotten more competitive. Although the data about the team’s possession is not what was analyzed due to missing data and all efforts to recover the data were futile, the little available in the original dataset shows that possession kept decreasing at what seems like a constant rate. This means our opponents are getting really better or the Falcons are getting weaker. Another point to look at would be the fact that the Super Falcons have won the AFCON 9 times. This means they performed exceptionally against other African countries and struggle with international players.
6. Recommendation

While the analysis could not give a clear reason as to why, we could all agree there were a few pointers.

More practice needs to be done to get on the international team’s level.
They could also improve team play and maybe each work and focus on improving their strengths.
The team can possibly scout for more exceptional talents to boost their overall performance.
7. Limitations of the analysis

I think extra research into the top three winners each year would fill the missing gap in the analysis. Also, regression analysis to identify significant factors affecting the team’s performance should give a clearer pointer. This might probably result in part two of this post.
