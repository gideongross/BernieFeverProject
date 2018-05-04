
## Theoretical Overview

Hailed  as “the third age of political communication” (Larsson, 2014), the Internet is playing an increasingly significant role in politics across the world.  The latest US Presidential elections and the Brexit vote, have demonstrated how non-direct interests can manipulate the political conversation, particularly through Facebook.  But how do political figures themselves stimulate and influence public conversation through their own Facebook pages?

Political leaders use social media for both transparency and outreach (Aharony, 2012; Steinfeld, 2016).  Most studies have focused on social media use during campaigning or by political leaders in office.  However, less work has been done on the way in which opposition leaders use social media to build support.  The benefit of social media is that it offers political leaders a channel of communication that is not filtered by national or local media and therefore conveys unique agendas without censorship or filtering.  In this sense, it particularly serves politicians in opposition.   (Steinfeld, 2016)

Despite the revolutionary promise of social media to transform political debate and re-engage citizens, the Internet has enhanced existing behavioural patterns, broadcasting rather than stimulating dialogue (Sorensen, 2016; Carlisle & Parron, 2013; Fenoll & Cano-Orón, 2017).  Similarly, social media can favour ideological polarisation through the much-cited echo-chamber effect.          

Studies have tended to focus, therefore, on either the posts (identifying typographies or comparing activity across different leaders) or the dynamics of political conversations but less often combining both.  One exception found that participation and interaction amongst followers increases, the more negative the sentiment of the original post. (Fenoll & Cano-Orón, 2017).  This somewhat contradicts sociological studies of online behaviour which have found that positive emotions tend to spread more easily than negative emotions amongst groups of social media users (Ferrara & Yang, 2015).

Sentiment analysis of Facebook activity is common but fewer studies have applied this to political interactions online.  One exception, considering the online behaviours of local government representatives in Germany, found that neutrality dominated both comments and posts but that among those exhibiting emotional content, positive emotions were more common (Hoffman, 2013).

This study therefore contributes to the current literature on Facebook use by political leaders in several ways .  Firstly, by isolating the study to one political figure and adopting topic-based as opposed to typographical analysis, we can gain deeper insight as to how a political opposition leader contributes to the national political conversation.  Secondly, by combining an analysis of both posts and comments we can identify the different ways in which users interact with and respond to certain topics.  Finally, considering the comments also allows us to investigate the levels of emotion and the presence of emotional contagion in online political debate.



## Topic Clusters and Semantic Networks

After parsing the two corpuses, we extracted the 500 most frequent noun phrases and created a semantic network map with 200 nodes to get a first impression of the data. To create our own categories and clean the csv files, we downloaded the cluster categories. 

We realized that the names of the default topics created by Cortext were not very accurate, e.g. the topic richest country in the history & history of the world. Moreover, the terms do not always correspond to the default cluster. In some cases the mismatch was obvious, for instance, the noun phrase “newspapers and television” was associated with richest country in the history & history of the world. In some other cases, it was necessary to double-check the content of the posts using the corpus explorer to see how the terms are used in context. Also, some terms such as “next year” or “new report” were too general to be related to specific clusters and we deleted them manually. Based on these findings, we created a more refined list of topics.



## Topics Identified

1) Trump administration 

2) Healthcare

3) Education

4) CC [climate change] and sustainable energy

5) Corporate welfare (e.g. terms such as “tax breaks” or “tax cuts”)

6) Minimum wage

7) Socio-economic justice

8) Criminal justice

9) Gun control

10) Supreme Court [Supreme Court’s decisions]

11) Support for candidates [Iowa and Illinois elections]

12) Events [at which Sanders appears]

13) Negative comparison [Sanders often compares the U.S. with other countries to highlight the deficits of the U.S.]



## Methodology 

We uploaded the customized list as a terms list which we indexed to the 324 posts. 
Not all of the posts had an assigned topic. In total 59 posts were not labelled. We created a new terms list that did not include posts that had not be tagged to any of the topics. To link the posts and their topics to the respective comments, we built another corpus list which we indexed to the comments.

Meanwhile, we ran a sentiment analysis of all the comments. We decided to use Textblob and to focus on sentiment polarity which varies between -10 (very negative) and +10 (very positive). We sliced the data into the following six bins for better visualization: -10 to -5, -4 to -2, -1 to 1, 2 to 4, 5 to 7, and 8 to 10.

After having a first look at our data (showing post_id, post message, comment message, associated topic and associated sentiment polarity), using corpus explorer, we created a semantic network and a contingency matrix for visualization

![github_picture1](https://user-images.githubusercontent.com/38719684/39624719-a5cf3838-4f9a-11e8-888b-b4b420a47e5e.png)

![github_picture2](https://user-images.githubusercontent.com/38719684/39624720-a6a29606-4f9a-11e8-9f18-5c6a877fc8b8.png)

To have an in-depth analysis of these results, we created sub-corpuses for each cluster by running queries. Using the corpus explorer, we could do a qualitative analysis of the most interesting boxes from the contingency matrix.



## Analysis

### Figure 1: Epoch Bump Graph of Post Topics

![figure_1](https://user-images.githubusercontent.com/38719684/39634923-53e9bf08-4fbc-11e8-9c9a-70de436e7414.png)

This shows a temporal evolution of the topics of Bernie’s posts. We can see that socio economic justice, corporate welfare, trump administration, and healthcare were the dominant ones with some movement in terms of ranking among the top ones, but no drastic ones overall

### Figure 2: Network Modeling with aggregated sentiment score as tags

![figure_2](https://user-images.githubusercontent.com/38719684/39635063-b13a8fc0-4fbc-11e8-9b52-a234b72dee98.png)

The above figure provides us with a visualization of the connection between different topics in Bernie’s posts in clusters complimented by the average aggregated score of the sentiment analysis on the comments of the cluster. This network map (Figure 2) shows three main clusters of topics, meaning that one post could contain multiple topics that are within the same cluster or that share a node. For example some posts that are about minimum wage also mention socioeconomic justice or health care. The Yellow and blue clusters are connected whereas the green cluster is isolated. 

The results demonstrate that posts about topics in the blue cluster (immigration, events, and healthcare) and the green cluster (education, gun control,..etc) have an aggregated highly positive score of 8 to 10. This means that these posts generally generate comments with a positive sentiment such as agreement and praise. While topics in the yellow cluster such as the trump administration, socioeconomic justice, and the supreme court have comments with a highly negative sentiment score (-10 to -5). We believe that some negative comments are not necessarily about the topic itself or a criticism of the post’s content, but negative statements about Bernie himself such as “ Berinie where is your humanity? You are cruel.”

### Figure 3: Heat Map with sentiment score as third variable

![figure_3](https://user-images.githubusercontent.com/38719684/39635272-4ee339fc-4fbd-11e8-8a2d-74447d3e1ed3.png)

Figure 3 is a heat map showing the network mapping of the various topics contained in the posts, correlated by the average sentiment score that are conveyed in the comments.  Red is a more positive sentiment score with bright red being a score of 10. Blue is negative sentiment score, the darker it is the more negative the score is. White is a neutral sentiment score. Posts about immigration appear to elicit very positive comments. A closer look at the data, however, shows that immigration posts were very close in time suggesting that it was about a specific event which might explain why it has received a very positive score (Figure 4):

### Figure 4: Field Evolution of Immigration

![figure_4](https://user-images.githubusercontent.com/38719684/39635367-9722d8d0-4fbd-11e8-80fc-5fccc41d0b4c.png)

The corpus explorer on a subquery of all ‘immigration’ posts revealed that all those comments belonged in fact to three posts only. Nothing can thus be said about a sentiment trend on immigration posts:

### Figure 5: Network Maps

### Figure 6: Contingency Matrix: Post Topics and Comment Sentiment Scores



The contingency matrix above (figure 1) visualizes a joint distribution of our two variables: the topics addressed in Bernie’s posts on the X-axis and the sentiment score of the comments on the Y-axis. The colors demonstrate the degree of correlation between the two variables with red being the most correlated, blue anti-correlated, and white do not feature any correlation. 

Finally, the size of the cells both horizontally and vertically represent the portion of that category in the overall sample size. For the Y-axis, which contains the sentiment score, the length of the cell is proportional to the number of comments that belong to each category. In this case -1 to 1 is longest because a large part of the comments (for all of the posts) have that score (~ 50%)



The results of the contingency matrix demonstrate that there is a high correlation between the posts about the Trump administration and comments with a highly negative score (-10 to -5). There is also a strong correlation between posts on minimum wage and comments with a decent positive score (2 to 4) and immigration (and events) and comments with a highly positive sentiment score (8 to 10).

To have a closer look at the strong correlation results between ‘trump administration’ and the very negative sentiment range -10_-5 and ‘minimum wage’ and the positive sentiment range of 2_4, we created field evolution graphs isolating the ‘opinionated’ comments:


### Figure 7: Field Evolution of Opinionated Comments - Subcorpus ‘Trump Administration’


Though we can indeed see that negative comments mostly dominated throughout, we again see that there are event specific bumps that heavily influence the results. Without those, comments are not really as negative as the contingency matrix may suggest. The same holds true for the topic minimum wage:

### Figure 8: Field Evolution of Opinionated Comments - Subcorpus ‘Minimum Wage’





## References

Aharony, N. (2012) Twitter use by three political leaders: an exploratory analysis Online Information Review, Vol. 36, No. 4, pp. 587-603

Carlisle, J. & Patton, R. (2013) Is Social Media Changing How We Understand Political Engagement? An Analysis of Facebook and the 2008 Presidential Election Political Research Quarterly, Vol. 66, No. 4, pp. 883–895

Fenoll, V. & Cano-Orón, L. (2017) Citizen engagement on Spanish political parties’ Facebook pages: Analysis of the 2015 electoral campaign comments Comunicación y Sociedad Vol 30, No. 4, pp. 131-148

Ferrara, E. & Yang, Z. (2015) Measuring Emotional Contagion in Social Media PLOS ONE Vol 10, No. 11

Hofmann, S. et al (2013) What makes local governments' online communications successful? Insights from a multi-method analysis of Facebook Government Information Quarterly, Vol. 20, pp. 387-396

Larsson, A. (2014) Pandering, protesting, engaging. Norwegian party leaders on Facebook during the 2013 ‘Short campaign', Information, Communication & Society, Vol. 18, No. 4, pp. 459-473

Sorensen, M. (2016) Political Conversations on Facebook – the participation of politicians and citizens Culture & Society 2016, Vol. 38(5) 664–685

Steinfeld, N. (2016) The F-campaign: a discourse network analysis of party leaders’ campaign statements on Facebook Israel Affairs, Vol. 22, No. 3/4, pp. 743-759

We used two corpuses: the first one included all the 324 facebook posts of Bernie Sanders since Jan 2018; the second one is made of all the respective comments to the posts.
