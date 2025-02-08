# Life_Satisfaction_UKHLS

Drawing upon the UKHLS data set, this analysis revealed an overall significant decrease in life satisfaction for each age group, with those aged 60+ and 16-35 being the hardest hit. Having poor mental well-being, alongside being lonely, socially isolated and lacking in companionship are important predictors of low life satisfaction across all ages. This indicates the importance of subjective indicators in predicting life satisfaction. In terms of objective indicators, having a health condition, poor health behaviors,  and living in rented accommodation are all important predictors of low life satisfaction across age groups. Being single and having low income also predict low life satisfaction, but these mostly appear as stronger predictors for the two youngest age groups. Posting on social media regularly predicts low life satisfaction for the oldest age group, but the results are mixed for the two youngest age groups. The granular analysis of the mean absolute SHAP values indicates a potential ceiling effect of life satisfaction across age groups. For these reasons, social policy initiatives should focus on improving the well-being of those at the lower end of the life satisfaction scale. These social investments should cut across age groups, but a particular focus on both younger and older adults may be needed due to the more significant decline being seen for these age groups. A future longitudinal study considering whether or not life satisfaction has declined more substantially post-COVID-19, for individuals whose life satisfaction was already below average pre-COVID-19, may be beneficial to provide clarity. Future policies need to prioritize mental health improvement initiatives, but these initiatives may need to be holistic in their approach, considering how community resources can develop social connection, alongside improved access to healthcare, a reduction in poor access to resources due to ill health, and increased financial support for those who need it. In particular, these interventions may need to consider inequality of resources, how this has been exacerbated by COVID-19, and how people understand their position in relation to others, when attempting to improve life satisfaction for those reporting the lowest well-being scores. 

## Exploratory Analysis

Before undertaking analysis, the mean life satsifaction score was consider for all individuals, by age group, for each predictor variable. We can see large differences in scores dependent on outcomes in the exploratory tables below. For example, on average, those who hardly ever feel lonely have a life satsifaction average score of 5.9, compared to those who often feel lonely, having a score of 3.8. Similarly, in terms of how well an individual is managing financially, those who are 'living comfortably', have a mean score of 5.9, whilst for those who are 'finding it very difficult', have an average score of 3.1.

## Exploratory Tables: Mean Life Satisfaction of Individuals in 2018 Dataset

All values are presented as the mean life satisfaction score (M) and the percentage of individuals within each category for each variable (%). Values in the table correspond to the values after imputation of missing values by median for continuous variables and mode for categorical variables.

### Mental Health Likert
| Scale          | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------|-------|----|-------|----|-----|----|
| Least distressed (0)  | 4203  | 5.8| 7072  | 5.6| 6517  | 6.0|
| (1)            | 1555  | 5.6| 2206  | 5.5| 1792  | 5.6|
| (2)            | 1264  | 5.3| 1560  | 5.1| 1106  | 5.4|
| (3)            | 748   | 5.1| 1001  | 4.8| 606   | 5.1|
| (4)            | 750   | 4.8| 957   | 4.7| 513   | 4.8|
| (5)            | 392   | 4.7| 501   | 4.4| 306   | 4.6|
| (6)            | 458   | 4.3| 555   | 4.1| 286   | 4.2|
| (7)            | 274   | 4.2| 339   | 3.8| 174   | 4.1|
| (8)            | 290   | 3.9| 302   | 3.6| 188   | 3.9|
| (9)            | 140   | 3.5| 194   | 3.3| 92    | 3.6|
| (10)           | 136   | 3.3| 240   | 3.0| 102   | 3.4|
| (11)           | 85    | 3.0| 160   | 2.9| 75    | 2.8|
| Most distressed (12)| 81    | 2.5| 136   | 2.6| 64    | 2.6|

### How often feels lonely
| Frequency        | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| Hardly ever/never| 4912  | 5.8| 9197  | 5.6| 478  | 5.9|
| Some of the time | 4613  | 5.0| 5200  | 4.7| 3435 | 5.1|
| Often            | 851   | 3.7| 826   | 3.3| 7908 | 3.8|

### How often feels isolated from others
| Frequency        | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| Hardly ever      | 5294  | 5.7| 9182  | 5.6| 8052 | 5.9|
| Some of the time | 4398  | 4.9| 5312  | 4.6| 3387 | 5.0|
| Often            | 684   | 3.7| 729   | 3.3| 382  | 3.6|

### Recently felt cannot overcome difficulties
| Frequency                  | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Not at all                 | 2740  | 5.9| 4446  | 5.8| 4770 | 6.1|
| No more than usual         | 6142  | 5.2| 8990  | 5.1| 6122 | 5.4|
| Rather more than usual     | 1244  | 4.2| 1534  | 3.8| 808  | 4.0|
| Much more than usual       | 250   | 3.2| 253   | 2.7| 121  | 2.9|

### How often feels lack of companionship
| Frequency                  | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Hardly ever/never          | 4840  | 5.7| 8311  | 5.6| 7266 | 5.9|
| Some of the time           | 4859  | 4.9| 6096  | 4.8| 4034 | 5.2|
| Often                      | 677   | 4.0| 816   | 3.6| 521  | 4.0|

### Own property
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| No                         | 4492  | 5.0| 4129  | 4.7| 2261 | 5.2|
| Yes                        | 5884  | 5.4| 11094 | 5.3| 9560 | 5.6|

### Private rent
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| No                         | 8447  | 5.3| 13701 | 5.2| 11271 | 5.6|
| Yes                        | 1929  | 5.1| 1522  | 4.9| 550   | 5.2|

### Council flat rent
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| No                         | 8060  | 5.3| 12754 | 5.2| 10184 | 5.6|
| Yes                        | 2316  | 5.0| 2469  | 4.6| 1637  | 5.1|

### Relationship Status
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Not single                 | 6877  | 5.4| 11676 | 5.3| 7699  | 5.6|
| Single                     | 3499  | 5.2| 3547  | 4.7| 4122  | 5.4|

### How well managing financially
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Living comfortably         | 1990  | 5.8| 3292  | 5.7| 4701  | 5.9|
| Doing alright              | 5554  | 5.4| 6863  | 5.4| 4961  | 5.5|
| Just about getting by      | 1973  | 4.8| 3559  | 4.7| 1734  | 4.9|
| Finding it quite difficult | 746   | 4.1| 1308  | 4.0| 374   | 4.2|
| Finding it very difficult  | 113   | 3.7| 201   | 3.2| 51    | 3.1|

### Long standing physical or mental disability
| Status                     | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Yes                        | 1765  | 4.6| 4437  | 4.6| 5515  | 5.3|
| No                         | 8611  | 5.4| 10786 | 5.4| 6306  | 5.8|

### Physical health limits moderate activities
| Frequency        | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| Yes a lot        | 186   | 4.4| 715   | 3.6| 1596 | 4.6|
| Limited a little | 1449  | 4.8| 3035  | 4.7| 3861 | 5.4|
| No not at all    | 8741  | 5.3| 11473 | 5.4| 6364 | 5.9|

### Physical health limits amount of work
| Frequency        | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| All of the time  | 92    | 3.8| 310   | 3.1| 558  | 4.6|
| Most of the time | 424   | 4.2| 955   | 3.9| 1398 | 4.8|
| Some of the time | 1006  | 4.5| 1919  | 4.6| 2430 | 5.4|
| A little of the time| 3218| 5.1| 4905  | 5.1| 3760 | 5.7|
| None of the time | 5636  | 5.5| 7134  | 5.6| 3675 | 6.0|

### Smoker
| Status           | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| Yes              | 1516  | 4.8| 2245  | 4.7| 1094 | 5.2|
| No               | 8860  | 5.3| 12978 | 5.2| 10727| 5.6|

### Self reported health
| Status           | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| Excellent        | 1455  | 6.0| 1208  | 5.9| 477  | 6.3|
| Very good        | 4761  | 5.5| 5739  | 5.6| 3402 | 6.0|
| Good             | 2946  | 4.9| 5083  | 5.1| 4006 | 5.7|
| Fair             | 4761  | 4.2| 2464  | 4.4| 2953 | 5.1|
| Poor             | 165   | 3.2| 729   | 3.2| 923  | 4.0|

### Days vigorous activity last week
| Frequency        | 16-35 | M  | 36-59 | M  | 60+ | M  |
|------------------|-------|----|-------|----|-----|----|
| No days          | 4367  | 5.1| 6807  | 4.9| 7475 | 5.4|
| One day          | 1024  | 5.2| 1318  | 5.2| 830  | 5.7|
| Two days         | 2024  | 5.3| 2965  | 5.3| 1578 | 5.7|
| Three days       | 777   | 5.4| 951   | 5.3| 435  | 5.8|
| Four days        | 1057  | 5.4| 1688  | 5.4| 897  | 5.8|
| Five days        | 522   | 5.4| 653   | 5.3| 214  | 5.6|
| Six days         | 356   | 5.5| 509   | 5.4| 229  | 5.8|
| Seven days       | 251   | 5.3| 332   | 5.4| 163  | 5.8|

### Frequency of posting on social
| Frequency                  | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| Every day                  | 1150  | 4.9| 1687  | 4.9| 765  | 5.2|
| Several times a week       | 923   | 5.1| 1635  | 4.9| 910  | 5.2|
| Several times a month      | 1166  | 5.1| 1770  | 5.0| 836  | 5.3|
| Once a month               | 661   | 5.2| 923   | 5.1| 421  | 5.4|
| Less than once a month     | 1172  | 5.1| 1951  | 5.0| 1188 | 5.3|
| Never                      | 877   | 5.0| 2595  | 5.0| 4164 | 5.4|

### Individual income level scale
| Income Range               | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| £0 - £10,000               | 2045  | 4.9| 1960  | 4.8| 1665 | 5.3|
| £10,001 - £20,000          | 1986  | 5.1| 2887  | 4.9| 3135 | 5.2|
| £20,001 - £30,000          | 1355  | 5.2| 2831  | 5.0| 1877 | 5.4|
| £30,001 - £40,000          | 373   | 5.3| 1543  | 5.2| 858  | 5.5|
| £40,001 - £50,000          | 127   | 5.5| 653   | 5.3| 352  | 5.6|
| £50,001 - £60,000          | 40    | 5.3| 459   | 5.4| 241  | 5.6|
| £60,001 - £70,000          | 14    | 5.5| 136   | 5.5| 100  | 5.6|
| £70,001 - £100,000         | 9     | 5.6| 92    | 5.3| 56   | 5.6|

### Household income level scale
| Income Range               | 16-35 | M  | 36-59 | M  | 60+ | M  |
|----------------------------|-------|----|-------|----|-----|----|
| £0 - £10,000               | 798   | 4.6| 1440  | 4.5| 5732 | 5.4|
| £10,001 - £20,000          | 747   | 4.9| 1272  | 4.9| 810  | 5.2|
| £20,001 - £30,000          | 917   | 5.0| 1416  | 5.0| 581  | 5.2|
| £30,001 - £40,000          | 966   | 5.1| 1522  | 5.2| 423  | 5.2|
| £40,001 - £50,000          | 823   | 5.2| 1522  | 5.3| 273  | 5.2|
| £50,001 - £60,000          | 625   | 5.2| 1206  | 5.4| 177  | 5.0|
| £60,001 - £70,000          | 380   | 5.4| 870   | 5.5| 114  | 5.4|
| £70,001 - £100,000         | 507   | 5.3| 941   | 5.3| 110  | 5.6|
| £100,001 and above         | 186   | 5.3| 372   | 5.3| 64   | 5.5|


## Life Satisfaction - background

Within the UK and internationally, there has been a movement away from focusing solely on the financial aspects of a country’s growth and development, to supplementing these indicators with measurements of societal well-being (Barrington-Leigh 2021). To monitor and evaluate well-being levels and outcomes, the UK Government has set up the Measuring National Well-being Programme, an initiative to ensure policy decisions are evidence-based and that changes are being tracked over time (Office for National Statistics, 2024). As life satisfaction and well-being are a key concern for countries and Governments internationally, it is not surprising that there is a vast amount of literature on the subject. Predominantly, the literature focuses on traditional statistical analysis methods to evidence correlations or cause and effect of life satisfaction and other variables. One of the most recent and relevant examples to this research is a study considering life satisfaction in UK emerging adults during the pandemic (Li and Gutman, 2024). However, in more recent years, machine learning models and techniques have been applied to predict the life satisfaction of adults in Europe. The UK Centre for Economic Performance (UKCEP) considered life satisfaction across the UK, using the British Cohort Study, and a similar study of loneliness has been completed in Scotland (Clark et al., 2022; Osawa et al., 2022). Additionally, UKCEP have completed a machine learning longitudinal study, which considers factors predicting well-being across the UK, in comparison to two other European countries (Oparina et al., 2022). 

Living a satisfying, happy and meaningful life is important to most people, and is a goal of public policy due to the multitude of social benefits associated with high life satisfaction. However, understanding whether correlates of life satisfaction are the cause or the effect, and are therefore bidirectional, is not always straightforward (Marquez et al., 2023). In some cases, it may be that the variables associated with life satisfaction are both drivers and affects and are therefore bi-directional in nature. For example, trust in community positively predicts life satisfaction, and life satisfaction likewise predicts trust in community (Zhang, 2020). Yet other studies have found relationships that are not bidirectional, such as in the case of health predicting life satisfaction in older adults, but life satisfaction not predicting health (Moreno-Agostino, Abad \& Caballero, 2022). A common difficulty is that studies within this research area are mostly cross-sectional, and therefore unsuitable for inferring cause and effect, and unfortunately, longitudinal studies are sparse. For this reason, much of the research cited here is in relation to associations, as opposed to cause and effect relationships. 

There are numerous variables that influence, or are associated with, life satisfaction, including socio-demographic factors, which are often referred to as objective variables, and psychological characteristics, which are mentioned frequently as subjective variables. Subjective indicators demonstrate how an individual assesses and evaluates multiple domains of their life, whilst objective factors represent the physical and tangible aspects of people’s lives that are there to meet their needs, which in turn enhance their well-being. The subjective variables may include mental health variables and assessments of various domains of an individuals life, whilst life satisfaction as a whole concludes an integrated assessment of these different sub-components. For this reason, life satisfaction and the subjective variables often highly correlate (Fabian et al., 2021). 

If we first consider social life, those reporting higher life satisfaction are more likely to have a wide circle of friends and better-quality friendships (Amati et al., 2018). The social skills gained through these interpersonal relationships, such as cooperation and an ability to handle social stress, contribute to stronger relationships and an improvement in well-being (Amati et al., 2018). Furthermore, individuals reporting high life satisfaction are more likely to feel a sense of belonging and trust within their community (Hicks et al., 2013). A similar association has been shown between leisure activities and life satisfaction, indicating those with more leisure time may benefit from increased social interaction, resulting in higher well-being overall (Nimrod 2017). Research also indicates it is not just having leisure time itself that increases well-being, but how leisure time is spent (Mutz et al., 2020). If leisure time is spent performing physical activity, and in particular physical activity which fosters healthy social interactions among groups, this positively correlates with life satisfaction (Mutz et al., 2020). This also increases satisfaction with other domains of an individual’s life, such as their health, body, and appearance (Mutz et al., 2020). Increased physical activity during free time has also been proven to have a positive spillover effect on employment outcomes and well-being at work (Hecht \& Boies 2009).

There is a wide range of research considering the association with life satisfaction, employment, and occupational success, reasons of which relate to higher income, a sense of meaning and purpose, and social benefits of working (Dimari et al., 2019). On the other hand, having a reduced work capacity due to poor physical and/or mental health is associated with lower life satisfaction (Bakkeli 2021). It is not just employment that benefits well-being, but the nature of employment itself affects how satisfied individuals are with their jobs, which impacts their life satisfaction (Charles-Leija et al., 2023). A sense of autonomy and self-determination during working hours is an important factor in job satisfaction. If work is a source of intellectual stimulation, personal development and recognition, it can contribute more to individuals’ well-being than leisure time which is low effort, nonphysical and lacks stimulation (Charles-Leija et al., 2023). The benefits of a happy and fruitful working environment have been evidenced to increase productivity, performance and retention in the workplace (Dimari et al., 2019; Charles-Leija et al., 2023). Happy and satisfied working individuals are also more likely to be friendly at work, develop good working relationships, and help others (Dimari et al., 2019). Overall, this helps to make working environments more pleasurable, reduce staff turnover costs and may improve the country’s economic performance overall (Dimari aet al., 2019). 

If we consider income and well-being, the associations between these two variables are more complex than initially thought, and recent research provides an understanding of how macroeconomics affects psychology. Researchers are mostly in broad agreement that life satisfaction increases with income at country level, and also within countries. Therefore, on average, as a countries GDP increases, so does its citizens life satisfaction, and as an individuals income increases, so does their life satisfaction (Killingsworth, 2021; Jebb et al., 2018). On the other hand, more recent evidence shows what is commonly referred to as the Easterlin Paradox - in high GDP countries, over a length of time, economic growth stops positively correlating with life satisfaction. Reasons for this vary, but one explanation may be that income does in fact predict life satisfaction, but that how happy this makes people is being masked by the sacrifices made in other areas, such as lack of leisure time or time spent with family (Clark 2015). High-income inequality is considered to be the reason we do not see an incline in life satisfaction in countries with high GDP, as such growth is only affecting a smaller minority of people (Ortiz-Ospina \& Roser, 2013/2024). Another factor very much related to this, which has been more thoroughly researched, is that people not only become used to their income over time, but they also compare themselves to their peers. For this reason, income rank has become a key focus in this area, over absolute income (Fitzroy 2022). Individuals who perceive their income as lower to their immediate social groups (in terms of age, gender and place) report lower life satisfaction (Yu 2019). This effect is larger in countries with high disposable income inequality. High disposable income inequality therefore reaches a critical tipping point, where in the earlier stages, individuals may feel the benefits of upward social mobility and perceive that their circumstances can improve with effort. However, once this rises beyond a certain level, negative effects, such as jealousy and unhappiness become dominant (Yu \& Wang, 2017).  

Another important factor associated with increased well-being and life satisfaction is an individual’s health outcomes and how these relate to increased longevity and life expectancy. Longitudinal studies have confirmed that high well-being contributes between four to ten years additional life expectancy, in comparison to those with low well-being (Pavot \& Diener, 2008). In another longitudinal UK study, those with higher well-being in earlier life were shown to have greater physical health in older ages (Zaninotto 2019). They were less likely to live with chronic health conditions or diseases (Zaninotto 2019). Those with higher life satisfaction are therefore not only living longer but living longer in good health. 

It is already understood that life satisfaction may be best explained by subjective variables as opposed to objective variables, indicating it is an individuals’ perception of their life that is the most important factor in improving well-being. However, these variables are often inseparable from objective factors. This section addresses both the literature and ideas around the third focus of the analysis, this being the predictive models for both the extended set of variables, which includes both subjective and objective factors, and the limited sets of variables which include objective factors or subjective factors only. The importance of assessing these differences by each age group is in response to recent social policy arguments that appear to have perhaps overly relied on subjective indicators of well-being as opposed to objective, particularly for the younger age groups. These will be briefly explored below. 

As previously discussed, individuals' satisfaction with various aspects of their life is heavily influenced by social comparisons. This subjective perception is interdependent with societies objective conditions, especially where inequality is pronounced. In addition to social comparison, there are two other subjective variables that are frequently highly correlated with life satisfaction and relate to objective factors, these being mental health and resilience, both of which will be the focus here. 

Resilience is an important component of life satisfaction, particularly during stressful live events, as it increases the ability to cope with adversity. In terms of mental health, the above literature has already highlighted how this variable highly correlates with life satisfaction. Firstly, if we consider public sentiments on these topics, a very recent survey found that older generations, such as baby boomers and generation X, are more likely than younger generations to blame the increase of mental health problems in young people as being caused by them having less resilience (Policy Institute, King's College London, 2024). Similarly, the majority of the UK public believe youth mental health is best tackled by increased mental health services, whilst a much smaller minority cite structural drivers such as unemployment, economic problems, sexism and discrimination (Policy Institute, King's College London, 2024). The importance of mental health interventions as a dominant public policy focus in order to improve well-being has also been mirrored by a recent longitudinal study evidencing how life satisfaction in adults is best determined by emotional health as a child, a by product of parental mental health, and only marginally affected by income and education (Knies 2022). This study was later criticised as it negates the use of longitudinal research demonstrating how mental health largely relates to a history of poverty, highlighting the interplay between our environment, available resources and our well-being (Knifton 2020; Price 2017). 

Much more recently, the Conservative Government echoed similar beliefs of young people lacking resilience in their recent party manifesto, where it was suggested young people join the national service or a civil resilience programme (Conservative Party, 2024). And even further back in 2019, the UK Government expressed concerns that young people are less resilient than previous generations, and suggested school interventions to boost the resilience of young children (Snowdon 2019). This was later criticised by the British Psychological Society (BPS) as perpetuating the idea of individualistic responsibility - It is a grave error to conceptualise character and resilience as something that is purely situated within individual children and young people and that responds to individual interventions with children. The characteristics of the systems around young people are what determine how resilient they are and how resilient they become.'} (British Psychological Society, 2019). In other words, resilience is a dynamic property of social, economic and community systems, it can be learnt and nurtured, is not an inborn character trait, and the ability to adapt, cope with change and become more resilient, is interdependent with our environments (Rutter, 2012; Masten 2018). 

As the above has shown, there appears to be sentiments within the UK public, the Government and academia, of young people lacking in resilience, and this being a driver of increased mental health problems and poor well-being. Interventions for well-being focusing only on young people themselves, rather than considering the environmental context, may fail to take responsibility for wider difficulties young people are experiencing, which may relate to more objective indicators. As psycho-social variables highly correlate with life satisfaction, the analysis will focus on both the extended and limited set of variables to identify how much the objective features alone contribute to predictions, in comparison to a full model including both subjective and objective indicators. This may help to address whether the concern of mental health services and resilience building interventions being heavily, or perhaps overly, relied upon by public policy officials is warranted. Or, whether this may be a concerning way to avoid focusing on material needs, and to provide full consideration of how these factors interact with the social and economic environment (Price, 2017). 

## Life Satisfaction - Age

Perhaps one of the most significant findings relating to life satisfaction research is the U-shaped happiness curve. This pattern describes how well-being is often highest in adolescence, then starts to decline from age 18, reaching its lowest points around age 35-50, with age 47 being the very lowest (Blanchflower 2007). After age 50, well-being starts to rise, reaching its highest point post 60 years (Blanchflower 2007). This pattern appears congruent in the UK, Europe and English-speaking countries outside of Europe (Blanchflower 2007).However, it is not universal (Steptoe et al., 2015). Easter European countries that used to form part of the Soviet Union show a decline in life satisfaction with age, and Sub-Saharan Africa and Latin America showonly minors shifts with age (Steptoe et al., 2015).

There is a substantial amount of literature concerning life satisfaction and age, and the associations which may explain some of these differences. Certain individual perceptions of what makes a good and satisfying life differ dependent on age-related values and variances in the importance individuals place on certain aspects of their life, whether this be their finances or physical health (Siedlecki et al., 2008). These differences inform people’s perceptions of their own life and how satisfied they are. For example, younger adults have been shown to place more meaning on a satisfying job and personal goals whilst older adults with less lifetime left may prioritise close relationships (Siedlecki et al., 2008). If we consider economic theory, its understood that people work harder in middle age, and enjoy the benefits of their efforts in later years, leading to a rise in satisfaction (Fabian et al., 2021). Furthermore, those in middle age may experience what is commonly referred to as a midlife crisis, alongside increased care-giving responsibilities and financial burdens. They may be more likely to regret not having achieved expectations, whereas these factors diminish as people get older, and acceptance of one’s circumstance replaces prior regrets (Fabian et al., 2021). In other words, a higher level of emotional maturity and acceptance occurs.

With life satisfaction being an important policy indicator of societal health, development and growth, generally, we hope that life satisfaction will increase over time, or at the least, remains flat. However, if we instead shift our attention to life satisfaction within the UK over the last 12 years, there is evidence of a decline (Blanchflower 2024). The Governments national well-being dashboard shows an increase in the percentage of individuals in the UK measuring their life satisfaction as low from 2018 in comparison to 2023 (Office for National Statistics, 2018). 

A similar dashboard from the UKHLS shows a decrease of life satisfaction for all ages, however this overall decline appears from the descriptive statistics to have started from the much earlier date of 2010, with periods of growth in-between (Figure 1; Understanding Society, 2024). If we are to consider the two calendar year periods which are the focus of this study; pre-COVID and during COVID, we can see from 2018 to 2021, the dashboard shows a decline in well-being across all age groups. Of the three age groups, prior to 2021, the highest life satisfaction can be found in those aged 55 or over, followed by those aged 16-34, whilst those aged 35-54 reported the lowest. From 2021, we can see a change in life satisfaction across these age groups. Those aged 55 or over continue to have the highest life satisfaction. This is then followed by those aged 35-54 and those aged 16-34 now appear to have the lowest life satisfaction. Overall, life satisfaction may have declined for all age groups between 2018 to 2021, and possibly since 2011, with the steepest decline being for the youngest age group.

![image](https://github.com/Anna-amon/Life_Satisfaction_UKHLS/blob/main/UKHLS%20Wellbeing%20Dashboard.jpeg)

If we consider life satisfaction more generally by age, there is evidence from the World Happiness Report of life satisfaction decreasing more substantially for those aged 15–24 than for any other age group (World Happiness Report, 2024). There is also evidence of a significant decline in adolescents, aged 11-15, since 2011. During the pandemic, a decline in life satisfaction has been evidenced as most significant for people aged 18-29 (Li and Gutman, 2024). To understand and confirm these shifts, we may consider other well-being measurements, such as mental health scores. Prior to 2011, the research evidenced a hump shape observed in mental health scores; good mental health was high for young people, then gradually declined and became worse around mid-age, and then began and continued to rise for those 7 reaching older age (Blanchflower et al., 2024). If we consider mental health scores within the UK post 2011, a similar trajectory seen with life satisfaction and age has been observed for mental health. The youngest age group now having the highest rate of poor mental health, and this declines with age in a linear fashion (Blanchflower et al., 2024). Using data from the UKHLS, approximately 8 percent of all respondents were in despair in 2010, compared to 12 percent in 2021 (Blanchflower et al., 2024). The sharpest incline can be seen for young women, rising from 8 percent to 20 percent (Blanchflower et al., 2024). Since 2018, the previous U-shaped anxiety curve has been reshaped into a linear decline with age.

If we turn to global literature on well-being and age, it can be seen that similar trends are occurring across English speaking countries, such as the UK, Australia, the US and Canada, however, quite disturbingly, the UK are the most largely affected by this difference in well-being across age groups (Blanchflower et al.,2024). These over-arching changes to the pattern in the U-shaped curve within the UK may relate to three large social and economic shocks that worsened well-being for everybody, but specifically, for those experiencing the negative effects of pre-existing inequalities, creating further division in terms of age, income, gender and ethnicity. These shocks are the 2008 recession, COVID-19 and social media (Blanchflower et al., 2024).

If we consider social media, there has not yet been a study proving causation of social media usage and declining well-being in the young, due to the nature of both events occurring around the same point in time, with Instagram being released in 2010. However there is evidence of screen time among young people rising rapidly since 2011, and that restricted access to smartphones correlates with improved well-being (Ho, Yu & Brown, 2024; Haidt 2024; Blanchflower and Bryson 2024b). In addition to this, considering Social Comparison Theory and the effects on life satisfaction, those that have access to the internet are more likely to compare their income to their peers (Clark, Flèche & Senik, 2015). Older and middle-aged people may also be less affected by the rise in technology, internet access, smartphones and social media, therefore it is likely young people will be impacted the most (Haidt 2024; Twenge 2018).

Considering the wider environment alongside these three shocks, the wider global context of income inequality and where the UK falls on this scope may also be a contributing factor. If we consider inequality in disposable incomes, that is income after taxes and benefits, the UK has one of the highest levels of income inequality in Europe (Francis-Devine 2024). Given this pre-existing income inequality existing within the UK, there is evidence to show that COVID-19 exacerbated difficulties for certain groups of individuals, who
already experienced disadvantage (Kerschbaumer et al., 2023). The impact was realised not only in terms of health outcomes, but social and economic outcomes too (Kerschbaumer et al., 2023). The predominant focus for this study is age, but other demographics, such as gender and income, are relevant. If we consider gender, women are more likely to be employed in ’Covid-riskier’ jobs, to have lost their jobs because of the pandemic, to have reduced their hours, and to shoulder the weight of care giving responsibilities, in comparison to men (Oreffice & Quintana-Domeque, 2020/2021). The COVID 19 pandemic worsened mental health on average for all ages, yet hit young people and women the hardest, exacerbating pre-existing inequalities for these individuals (Banks & Xu 2020). If we consider the shorted period of time during COVID-19, from May 2020 to September 2021, young adults with greater perceived current financial difficulties, mental and physical health conditions, and higher loneliness experienced lower life satisfaction. On the other hand, high life satisfaction was related to living with a partner and more face-to-face social interactions (Li and Gutman, 2024).

The specific reasons for the worsening in mental health of young people and women, and therefore in particular, young women, may be explored by considering the differences in mental health (GHQ) scores. The young people affected the most were those aged 16-24 and aged 25-34 and adults aged under 45 were also more affected than the older age group (Banks & Xu 2020; Blanchflower 2024). These findings were strengthened by the Annual Population Survey, where we can see a rise in anxiety for the general population, since 2011, but specifically for white females under 25 years of age (Blanchflower et al,. 2024). Young people who are women, unemployed, less educated and unable to find work present the worst mental health scores (Blanchflower et al,. 2024). Specific dimensions of the survey questions relating to mental health, show young people and women as more likely to be negatively impacted by areas such as depression, sleep and a sense of purpose (Blanchflower et al,. 2024). In addition, an increasing proportion of young people generally
report being less satisfied with their health, and as having more financial difficulties, the latter affecting men in particular, than other age groups (Blanchflower et al,. 2024). It is also noted that these changes were seen pre-pandemic (Blanchflower et al,. 2024).

Young people’s lives are frequently characterised by a lack of economic stability and capital, both of which make it harder to navigate adversities. For example, young people are more likely to private rent, and live with strangers, which can put strain on their social lives and affect their mental health (Veeroja et al,.2023). Additionally, older people were, in general, perhaps less impacted by the economic affects of the pandemic and are less likely to have children living at home, which may prevent them from having the same
sleep problems and worries young people may be experiencing (Banks & Xu 2020). This is not to say that older age groups have not been affected - particularly in terms of the health consequences of the pandemic, older people were likely to experience worst outcomes (Lee et al., 2024). However, the focus here is on life satisfaction and well-being, and evidence shows younger people in general to be more negatively affected.

The decline in life satisfaction is a concern across all age groups, and we can see that the decline in life satisfaction may relate to inequalities beyond just age, such as income, gender and ethnicity. However, the decline in life satisfaction for younger age groups is particularly concerning when we consider longevity and the aging population. Within the UK, life expectancy is increasing, however, the average number of years spent in poor health is also increasing. This means although people are living longer, they are spending a
larger proportion of their lifetime in poor health (McKee et al. 2021). The health and social care issues this bring are compounded by the fact that a higher proportion of those aged over 50 are now living alone and do not have children to care for them (Centre for Ageing Better, 2024). Inequalities faced by people when they are younger can have compounding effects throughout their lifetime, resulting in difficulties with health and wealth later in life. Younger generations are therefore required to be more resilient and better
prepared to deal with economic and social instability throughout their lives, yet an individual’s subjective sense of well-being in older age may also depend on the fulfilment of their expectations. Unmet expectations in young people may lead to difficulties in adapting to adversity in later life, and such expectations may be perceived particularly strongly where the ability to keep up with an immediate peer group and comparison of your own circumstances to others is being perpetuated by widening levels of inequality and economic egalitarianism. The decline we are seeing in life satisfaction among younger people may therefore have long-lasting effects, influencing their health, social connectivity, and economic stability as they age.

## Life Satisfaction - Summary

We can see overall how reductions in life satisfaction are associated with decreased mortality, unemployment, lower productivity, poor physical and mental health, fewer social relations, limited leisure time, lower income satisfaction compared to reference groups, and a reduction in life expectancy. Increases in life satisfaction are associated with higher mortality and employment rates, increased years spent in good health, employee retention, productivity, feeling socially connected, trust in the community, a sense of belonging, increased physical activity, high-income satisfaction compared to reference groups, and higher life expectancy. The benefits of these interventions in some cases are evidenced as bi-directional; individuals with high life satisfaction are more likely to socialize, be employed, and be connected to their wider community, in addition to taking care of their physical and mental health, which in turn, may further improve life satisfaction. However, in order for people to be able to adopt a lifestyle that fosters high well-being, policy interventions that aid individuals to do so are essential.

The ability of the population, and in particular, young people, to bounce back during social and economic adversity will depend on their immediate environment and whether this nurtures the resources needed to improve well-being. This environment requires the key ingredients necessary to foster a high degree of resilience necessary to withstand change - a degree of equality in resources and social mobility, financial and emotional support, access to good quality medical care, and options for satisfying leisure time. It is
necessary for social policy aimed at improving well-being to consider both subjective and objective factors and to appreciate the holistic and interconnected nature of all of these, rather than heavily relying on one area. To gain a more in-depth, comprehensive, and robust understanding of how these subjective and objective variables relating to life satisfaction interact with one another, specific and granular measurements of some of these sub-components are needed.

# Analysis

## Data Source and Variables

The first focus of this study is whether or not life satisfaction has declined for all age groups from 2018 -2021, and whether the decline has been worse for younger people. The second focus is to provide a more granular analysis of whether or not the main predictors of life satisfaction differ by age. To complete the analysis, we have used survey data from the UKHLS, a large, longitudinal questionnaire, with Waves 1-13 available from Data Service UK.

The calendar Year 2021 dataset includes individuals from waves 11, 12 and 13. This dataset has already been created and is available from the UK Data Service. There are a series of data frames for the 2021 dataset that have been aggregated in this analysis via linking. For this analysis, the main dataset used is indresp which contains most of the mainstage variables needed. This analysis combined indresp with hhresp, which contains data on all people in the household. The datasets were merged on the variable klmhidp. The second dataset, the calendar year 2018 dataset, is not available from the UK Data Service. To create this dataset, the three waves from dataset indresp, namely waves i, j, and k, covering 2018, are combined into a long format. Firstly, to match individuals in each wave with their household level data, a different approach was taken to the 2021 dataset, as we are dealing with different waves for individual and household level files, as opposed to two calendar year files, each with waves already combined, as seen in the 2021 dataset. The individual datasets for each 2018 waves were merged with the household level datasets for the corresponding wave, using a left join and matching on hidp. These three final datasets for each wave, which now include individual and household level data, were then aggregated into a final 2018 dataset, using an outer join and matching on each unique pidp for every individual.

The majority of variables for the 2018 dataset have been answered at each wave. However, those that were not are filled as NaNs. The final dataset for 2018 has a considerable number of variables due to combining the datasets using left and outer joins. This is necessary to create final calendar year variables using combinations of variables across each wave. New calendar year variables have been created to combine the results from each wave, the majority of which used the mean across all three waves for each pidp. One example of this is the life satisfaction variable, which for most people, was answered at each wave. For those that are categorical, and have more than 2 categories, the new variable is created using the mode instead. The age variable has been re-coded into subsets of individuals aged 16-35, 36-59 and 60+. Finally, after combining waves and datasets, each calendar year dataset resulted in three, smaller datasets, one for each age group. Therefore we have six datasets in total. The number of individuals in each dataset can be seen
in Table 1.

#### Table 1: The number of individuals in the final 2018 and 2021 Calendar Year datasets, for each age group

These are the final dataset numbers used for the models.

| Calendar Year | Age Group | Instances |
|---------------|-----------|-----------|
| **2018**      | 16-35     | 10,376    |
|               | 36-59     | 15,223    |
|               | 60+       | 11,821    |
| **2021**      | 16-35     | 5,949     |
|               | 36-59     | 10,561    |
|               | 60+       | 8,284      |

The life satsifaction outcome measure used is a single scale from 1-7, 7 indicating a very high level of life satisfaction, and 1 indicating very low life satisfaction. The survey question is framed as: ‘How satisfied are you with your life overall?

Completely Dissatisfied (1), 
Mostly Dissatisfied (2), 
Somewhat Dissatisfied (3), 
Neither Satisfied or Dissatisfied (4), 
Somewhat Satisfied (5), 
Mostly Satisfied (6), 
Completely Satisfied (7). 

Across each dataset, the life satisfaction variable is left skewed for all age groups, demonstrating how for the majority of people, their life satisfaction is rated above 5 on this scale. Before considering the predictor variables, the mean score for each age group (for each year, as opposed to the larger groupings) has been plotted for both the 2018 and 2021 datasets and can be seen in Figures 3 and 4. For both years, we can see those aged 60+ report higher life satisfaction, and the mean becomes much more volatile in older years, as people approach the end of life. If we compare the two years, we can see in the earlier year, 2018, the youngest age group of those aged 16-35, are reporting higher life satisfaction overall, compared to those ages 36-59. This reflects the U-shaped well-being curve. However, we can see a difference in the 2021 dataset. The youngest age group are no longer demonstrating higher well-being than the middle age group. Instead, from years 20-29, this appears lower, on average, than those aged 35-60 overall, with some similarities for those aged 40-45. This indicates a trend change from the U-shaped curve, and now there is a leveling out with age between 16-60 years, and then a steep linear incline with age from aged 60+. This potentially points to younger people, particularly those aged 20-29, being particularly impacted by COVID-19.

### Figure 3: Life Satsifaction by age, from the 2018 dataset
![image](https://github.com/Anna-amon/Life_Satisfaction_UKHLS/blob/main/2018%20DATASET.jpeg)

### Figure 4: Life Satsifaction by age, from the 2021 dataset
![image](https://github.com/Anna-amon/Life_Satisfaction_UKHLS/blob/main/2021%20DATASET.jpeg)

The predictor variables are based on prior research defining determinants of life satisfaction, most of which have been identified in the literature above. These can be broadly categorised into demographic variables (relationship status), socio-demographic variables (tenure, individual income, household income, how well managing financially), health behaviours ( smoker, how many days vigorous activity), physical health (health limits work, health limits moderate activities, subjective general health), social media usage (frequency of posting on social media) and social connection (how often feels isolated, how often feels lack of companionship, how often feels can overcome difficulties, how often feels lonely). The inclusion of GHQ into the model is based on previous research mentioned above, indicating associations between mental health and life satisfaction.

## Descriptive Statistical Analysis

Descriptive analysis was first undertaken using Python 3.11. Variables initially considered yet having over 40 percent of missing values were removed from the analysis, which left us with the variables listed above. Any negative values were also removed. For the use of the machine learning algorithms, each categorical variable is converted into binary numeric variables, 0 and 1 one for each category. For multiple categorical variables, such as Tenure, the variables have been re-coded where necessary, and then one hot encoded. For
Tenure, the re-code values created ‘own property’ for those who owned either with a mortgage or outright. Those who rented from a local authority or housing association are coded as ‘council flat rent’ and those who rented from an employer or private unfurnished are re-coded as ‘private renting’. Continuous variables are kept as they are.

The mean life satisfaction scores have been calculated, alongside the percentage of individuals within each category for each variable, for both the 2018 and 2021 datasets. These are listed in tables 19 and 20, in the appendix. From the descriptive statistics alone, it appears that those with higher mental health scores, and lower scores for variables relating to social connections, are also showing lower levels of life satisfaction. Similarly, those who have limited health and engage in less health behaviours also show lower levels of life satisfaction. However, in terms of age, from the descriptive statistics there doesn’t appear to be huge differences across age groups.

One point to note is that the median and mean has changed for the life satisfaction variable after removal of NaNs for the predictor variables in the 2021 dataset used in the final model, for the youngest age group. The differences can be seen from Table 2. This may indicate that for this younger age group, those with lower life satisfaction may not have responded to certain questions during COVID-19, and were therefore more likely to be removed from the dataset.

#### Table 2: The mean and median life satisfaction for the 2018 and 2021 Calendar Year datasets, for each age group, both before and after removal of NaNs

| Calendar Year | Age Group |          | Median before removal | Median after removal | 
|---------------|-----------|----------|-----------------------|----------------------|
| **2018**      | 16-35     | **Median** | 6                     | 6                    |                                  
|               |           | **Mean**   | 5.2                   | 5.3                  |                    
|               | 36-59     | **Median** | 6                     | 6                    |                    
|               |           | **Mean**   | 5.1                   | 5.2                  |                     
|               | 60+       | **Median** | 6                     | 6                    |                     
|               |           | **Mean**   | 5.5                   | 5.5                  |                     
| **2021**      | 16-35     | **Median** | 5                     | 6                    |                     
|               |           | **Mean**   | 5.0                   | 5.1                  |                    
|               | 36-59     | **Median** | 5                     | 5                    |                   
|               |           | **Mean**   | 5.0                   | 5.0                  |                   
|               | 60+       | **Median** | 6                     | 6                    |                     
|               |           | **Mean**   | 5.3                   | 5.3                  |             

## Statistical Analysis - Methods

To assess whether the decline in well-being for each age group is statistically significant, the life satisfaction variable has first been checked for normality. Having confirmed the variable is right skewed, the MannWhitney U-test, a non-parametric statistical test used for comparing two different samples, to assess whether there is a difference in the central tendency, is used. It is important to note here that the data used for these tests are the full calendar year datasets, before removal of individuals with NaN values for certain predictor variables. This is beneficial as it provides a more accurate representation of those surveyed.

To analyse the main predictors of life satisfaction, this research uses machine learning algorithms ‘white box models’, as they are easier to interpret than other algorithms such as neural networks. These three models are; Regression Trees (RT), Random Forests (RF) and eXtreme Gradient Boosting (XGBoost). There are a handful of reasons for the use of machine learning over traditional statistics. Firstly, Research complete by the UKCEP confirms that machine learning algorithms such as RF and XGBoost provided more predictive accuracy than traditional statistical methods (Oparina et al., 2022). This is measured by the r-squared (R²) value. Furthermore, these algorithms are highly suited to the UKHLS dataset due to their ability to deal with non-parametric, categorical, and continuous data. They are capable of analysing patterns among variables in order to predict outcomes, which provides a benefit over traditional statistics where you have to manually specify interactions between features (Géron 2023). Machine learning can therefore indicate new variables that may be overlooked in traditional statistics, and the algorithms can explore the interactions between them (Géron 2023).

Machine learning algorithms also work well with meta-data and in particular, meta-data that includes missing values (Géron 2023). After completing this cross-sectional study, the next step for this data set will be to use the UKHLS data from 2011, to complete a longitudinal study, tracking changes over time for individuals within different age brackets. When dealing with longitudinal data, missing data becomes a frequent occurrence due to survey changes and completion rates over time, therefore these algorithms will be better suited than traditional statistical methods, particularly where the dataset is large. RT are the baseline models, as these are simpler than RF and XGBoost, however, they are more prone to over-fitting to the training data. RF and XGBoost are based on RT and help to ensure the algorithm is not over-fitting to the training data (Géron 2023). Overall, there are 30 models in total: three for each age group, per each calendar year, for the extended set of variables. The best performing model on the extended set of variables is then applied to each limited variable dataset, of which there are 12 in total, 6 objective-only datasets, and 6 subjective-only datasets. Each of the models have been trained on 80 percent of the training data, and then tested on the remaining 20 percent of unseen data. The dataset has been stratified on the target variable to ensure an equal distribution of individuals measuring their life satisfaction from low to high in both the train and test set. A Grid Search has been completed to automate the process of searching across the parameter grid, in order to find the best parameters for the model. 5-fold cross-validation is then used to assess the performance of each parameter combination.

The scoring metrics used for each model are the Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-Squared (R²). The former assesses the predictive accuracy of each model and enables us to understand which model performs the best, whilst the latter will help us to understand model fit (Géron 2023). R² represents the proportion of the variance for a dependent variable that’s explained by the independent variables. A higher R² value indicates a model that more accurately represents the data. In order to further understand model accuracy, the different predictive accuracy for thresholds will be explored. The threshold will be based on the life satisfaction variable scale of 1 – 7. An accuracy score for each threshold will be given as a percentage of correct predictions. We will use a threshold of 1 as an acceptable margin of error, as the aim of the research is to not to base policy decisions on predictions for each individual, but to understand the main predictors for each age group generally. For this reason, we can trade predictive accuracy for a more interpretative model that is able to broadly categorise people within 1 point on the scale.

The highest absolute SHapley Additive exPlanations (SHAP) values is the model interpretation method used for this study. SHAP values tell us how much each feature contributes to moving the model output, from a base level to the actual model output, and then averaging these values across the dataset, to arrive at the average contribution of each feature to the model output (Molnar, 2024). This is particularly useful for this research as it helps us to understand how significant the subjective and objective variables are for the
predictions, in the two limited datasets, and therefore allows us to understand the areas that should be best prioritised by social policy. To visualize and provide granular insights into the SHAP values, a bee swarm plot is used to summarise the distribution of the values for each feature. This will provide an overview of how each feature impacts the prediction, in terms of the direction of the relationship between the predictor variables and the outcome variable in the model.

# Analysis - Results

## Traditional statistics - Mann-Whitney U test

The results of the Mann Whitney U-test confirm the p-values are highly statistically significant for each age group. In order of statistical significance, those aged 60+ show the highest statistical significance, with a p-value of p = 3.99084 × 10−20. The result for those aged 16-35 shows less significance than those aged 60+, with a p-value of p = 4.515883921555554 × 10−12, yet a higher statistical significance than for those aged 36-59, with a p-value of p = 3.723723744523904 × 10−7. We can therefore confirm that life satisfaction has significantly declined for all age groups, from 2018 to 2021, but most significantly for those aged 60+, followed by those aged 16-35, and the least significance shows for those aged 36-59.

## Machine learning - extended set of variables

To start, we will consider results from the 2018 Calendar Year dataset, and then the 2021 Calendar Year dataset, for the extended set of variables only. Table 2 provides the optimal hyper-parameters and Table 3 provides the RMSE, MSE and R² results for the RT, RF and XGBoost for the three 2018 datasets covering each age group. The XGBoost performed best for each age group, however, for both the RF and XGBoost, the results were improved for the two older age groups. This indicates the models found it easier to make predictions for the two older age groups. This may be due to less variability in the life satisfaction variable for the older age group, although, it may also be due to the two datasets containing more instances than the youngest age group, enabling the model to learn on more patterns in the training data.

#### Table 3: 2018 Calendar Year Hyper-Parameters for the Algorithms in the Extended Set of Variables

| Algorithm       | Age Range | MaxDepth | Min Samples Split | N Estimators | Learning Rate |
|-----------------|-----------|----------|-------------------|--------------|---------------|
| Regression Tree | 16-35     | 5        | -                 | -            | -             |
|                 | 36-59     | 6        | -                 | -            | -             |
|                 | 60+       | 5        | -                 | -            | -             |
| Random Forest   | 16-35     | 7        | 10                | 300          | -             |
|                 | 36-59     | 8        | 10                | 200          | -             |
|                 | 60+       | 7        | 10                | 300          | -             |
| Gradient Booster| 16-35     | 0.1      | -                 | 100          | 3             |
|                 | 36-59     | 0.1      | -                 | 100          | 3             |
|                 | 60+       | 0.1      | -                 | 100          | 3             |

#### Table 4: 2018 Calendar Year: MRSE, MSE, and R² of Predicting Life Satisfaction. The table shows the MRSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²   | Accurate Predictions % |
|-----------------|-----------|------|------|------|------------------------|
| Regression Tree | 16-35     | 0.94 | 0.97 | 0.40 | 71%                    |
|                 | 36-59     | 0.87 | 0.93 | 0.44 | 75%                    |
|                 | 60+       | 0.91 | 0.95 | 0.35 | 77%                    |
| Random Forest   | 16-35     | 0.87 | 0.93 | 0.45 | 73%                    |
|                 | 36-59     | 0.81 | 0.90 | 0.48 | 76%                    |
|                 | 60+       | 0.85 | 0.92 | 0.39 | 78%                    |
| Gradient Booster| 16-35     | 0.84 | 0.92 | 0.46 | 75%                    |
|                 | 36-59     | 0.79 | 0.89 | 0.49 | 77%                    |
|                 | 60+       | 0.82 | 0.91 | 0.41 | 78%                    |

Next, we can consider the results of the 2021 dataset. Table 4 provides the optimal hyper-parameters and Table 5 provides the RMSE, MSE and R² results for the RT, RF and XGBoost for the three 2021 datasets covering each age group. The XGBoost performed the best for each age group in comparison to the RT and RF, and for each age group, the XGBoost again performed best for the older age group across all metrics.

#### Table 5: 2021 Calendar Year Hyper-Parameters for the Algorithms in the Extended Set of Variables

| Algorithm       | Age Range | MaxDepth | Min Samples Split | N Estimators | Learning Rate |
|-----------------|-----------|----------|-------------------|--------------|---------------|
| Regression Tree | 16-35     | 5        | -                 | -            | -             |
|                 | 36-59     | 6        | -                 | -            | -             |
|                 | 60+       | 5        | -                 | -            | -             |
| Random Forest   | 16-35     | 7        | 10                | 300          | -             |
|                 | 36-59     | 7        | 10                | 300          | -             |
|                 | 60+       | 7        | 10                | 200          | -             |
| Gradient Booster| 16-35     | 3        | -                 | 50           | 0.1           |
|                 | 36-59     | 3        | -                 | 50           | 0.1           |
|                 | 60+       | 4        | -                 | 50           | 0.1           |

#### Table 6: 2021 Calendar Year Extended Set of Variables: MRSE, MSE and R² of Predicting Life Satisfaction. The table shows the MRSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²   | Accurate Predictions % |
|-----------------|-----------|------|------|------|------------------------|
| Regression Tree | 16-35     | 1.17 | 1.08 | 0.39 | 69%                    |
|                 | 36-59     | 1.20 | 1.09 | 0.37 | 70%                    |
|                 | 60+       | 1.15 | 1.07 | 0.35 | 74%                    |
| Random Forest   | 16-35     | 1.05 | 1.02 | 0.45 | 71%                    |
|                 | 36-59     | 1.09 | 1.04 | 0.43 | 72%                    |
|                 | 60+       | 1.09 | 1.04 | 0.38 | 74%                    |
| Gradient Booster| 16-35     | 1.05 | 1.02 | 0.45 | 71%                    |
|                 | 36-59     | 1.07 | 1.04 | 0.44 | 72%                    |
|                 | 60+       | 1.07 | 1.03 | 0.39 | 75%                    |


## Machine learning - limited set of variables (objective)

This section of the analysis considers the results from the machine learning models, for the limited set of objective variables, displayed in Tables 8 and 9. Given the best performing model for the extended set of variables is the XGBoost, we have only used this model for the limited set of variables. The R² is highest for the middle age group, indicating these variables have the best model fit for this group, which may be due to the dataset containing more instances. If we compare the results of the limited datasets with the extended datasets, we can see the percentage of accurate predictions, within a threshold of one, are much lower for the limited datasets, and the RMSE and MSE is much higher. The biggest differences can be seen by the R² results, which demonstrate how objective variables alone explain a smaller proportion of the variance in the life satisfaction variable, in comparison to the extended model with both subjective and objective variables.

#### Table 8: 2018 Calendar Year Limited Set of Objective Variables: RMSE, MSE, and R² of Predicting Life Satisfaction. The table shows the RMSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²   | Accurate Predictions % |
|-----------------|-----------|------|------|------|------------------------|
| Gradient Booster| 16-35     | 1.33 | 1.15 | 0.16 | 63%                    |
|                 | 36-59     | 1.16 | 1.08 | 0.25 | 67%                    |
|                 | 60+       | 1.13 | 1.06 | 0.19 | 68%                    |

#### Table 9: 2021 Calendar Year Limited Set of Objective Variables: RMSE, MSE, and R² of Predicting Life Satisfaction. The table shows the RMSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²   | Accurate Predictions % |
|-----------------|-----------|------|------|------|------------------------|
| Gradient Booster| 16-35     | 1.66 | 1.29 | 0.13 | 62%                    |
|                 | 36-59     | 1.58 | 1.26 | 0.18 | 62%                    |
|                 | 60+       | 1.47 | 1.21 | 0.16 | 64%                    |


## Machine learning - limited set of variables (subjective)

Next, the XGBoost has been applied to the limited set of subjective variables. This part of the analysis is to assess how accurate the predictions are on each dataset once the objective variables have been removed, to help clarify how much the model relies on objective variables in making its predictions, and how accurate predictions may be if we are to remove these entirely. As can be seen from the performance metrics in tables 10 and 11, the datasets containing subjective variables only are producing similar results to the model performance on extended datasets, containing both objective and subjective variables. This is the case of performance across all metrics, indicating the model relies almost predominantly on the subjective indicators when predicting life satsifaction.

#### Table 10: 2018 Calendar Year Limited Set of Subjective Variables: RMSE, MSE, and R² of Predicting Life Satisfaction. The table shows the RMSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²   | Accurate Predictions % |
|-----------------|-----------|------|------|------|------------------------|
| Gradient Booster| 16-35     | 0.85 | 0.92 | 0.46 | 74%                    |
|                 | 36-59     | 0.81 | 0.90 | 0.48 | 77%                    |
|                 | 60+       | 0.83 | 0.91 | 0.40 | 78%                    |


#### Table 11: 2021 Calendar Year Limited Set of Subjective Variables: RMSE, MSE, and R² of Predicting Life Satisfaction. The table shows the RMSE, MSE, and R² of predicting life satisfaction with 80 percent of the sample in each training set and the error calculated on the remaining 20 percent of each test set. The percentage of accurate predictions are those that have been correctly predicted within a threshold of 1.

| Algorithm       | Age Range | MSE  | RMSE | R²  | Accurate Predictions % |
|-----------------|-----------|------|------|-----|------------------------|
| Gradient Booster| 16-35     | 1.05 | 1.02 | 0.45| 72%                    |
|                 | 36-59     | 1.08 | 1.04 | 0.44| 72%                    |
|                 | 60+       | 1.08 | 1.04 | 0.39| 75%                    |

## Mean absolute SHAP values - extended set of variables

Having considered the performance metrics for each dataset, we can now explore the determinants of happiness for each age group, for each year, using the mean absolute SHAP values from the XGBoost models. Table 12 displays the mean absolute SHAP values for the 2018 calendar dataset, for each age group. The higher the mean absolute SHAP value, the higher the likelihood of this variable contributing to the life satisfaction outcome variable. If we firstly consider the differences across age groups, we can see that each group shares the same four most important variables as predictors, namely mental health (GHQ) scores, how well they are managing financially, feelings of isolation and lacking in companionship. All of the top variables for each age group are subjective, and the objective variables are placed at the lower end of the scale in terms of importance.

#### Table 12: Ordered Mean Absolute SHAP Values for Features by Age Group in 2018 Dataset (Extended Set of Variables)

| Feature                           | Age 16-35 SHAP  | Feature                           | Age 36-59 SHAP  | Feature                         | Age 60+ SHAP    |
|-----------------------------------|-----------------|-----------------------------------|-----------------|---------------------------------|------------------|
| Subjective wellbeing GHQ          | 0.288           | Subjective wellbeing GHQ          | 0.304           | Subjective wellbeing GHQ        | 0.24             |
| How well managing financially     | 0.153           | How well managing financially     | 0.176           | How well managing financially   | 0.14             |
| HO feels lack of companionship    | 0.121           | HO feels can overcome difficulties| 0.111           | HO feels can overcome difficulties| 0.13            |
| How often feels isolated          | 0.095           | HO feels lack of companionship    | 0.092           | HO feels isolated               | 0.10             |
| HO feels can overcome difficulties| 0.080           | HO feels lonely                   | 0.086           | HO feels lack of companionship  | 0.07             |
| HO feels lonely                   | 0.077           | HO feels isolated                 | 0.075           | Household income level scale    | 0.06             |
| Health limits work                | 0.042           | Health limits work                | 0.055           | HO feels lonely                 | 0.04             |
| Relationship status               | 0.040           | How many days vigorous activity   | 0.017           | Health limits work              | 0.03             |
| Household income level scale      | 0.038           | Household income level scale      | 0.016           | Individual income level scale   | 0.02             |
| Individual income level scale     | 0.037           | Individual income level scale     | 0.014           | Relationship status             | 0.01             |
| How many days vigorous activity   | 0.020           | Smoker                            | 0.013           | How many days vigorous activity | 0.01             |
| Own property                      | 0.017           | Relationship status               | 0.009           | Other                           | 0.00             |
| Smoker                            | 0.011           | LS physical or mental disability  | 0.007           | Health limits moderate activities| 0.00            |
| Private rent                      | 0.005           | Health limits moderate activities | 0.006           | Private rent                    | 0.00             |
| Council flat rent                 | 0.004           | Own property                      | 0.003           | Own property                    | 0.00             |
| LL physical or mental disability  | 0.003           | Private rent                      | 0.001           | LS physical or mental disability| 0.00             |
| Other                             | 0.000           | Other                             | 0.000           | Smoker                          | 0.00             |
| Health limits moderate activities | 0.000           | Council flat rent                 | 0.000           | Council flat rent               | 0.00             |

Table 13 shows the mean absolute SHAP value results for the 2021 dataset. The results are similar to the 2018 dataset, although some differences can be seen due to the 2021 dataset containing more variables. If we consider the other variables, which carry less weight overall, for the 16-35 and 36-59 age groups, relationship status and property ownership contribute more to the predictions for the younger age group, whilst local authority renting contributes more to the predictions for the 60+ age group. However, these difference are not large. Interestingly, frequency of posting on social media contribution is the same across age groups.

#### Table 13: Ordered Mean Absolute SHAP Values for Features by Age Group in 2021 Dataset (Extended Set of Variables)

| Feature                           | Age 16-35 SHAP  | Feature                           | Age 36-59 SHAP  | Feature                           | Age 60+ SHAP    |
|-----------------------------------|-----------------|-----------------------------------|-----------------|-----------------------------------|------------------|
| Subjective wellbeing GHQ          | 0.328           | Subjective wellbeing GHQ          | 0.325           | Subjective wellbeing GHQ          | 0.298           |
| Subjective general health         | 0.179           | Subjective general health         | 0.172           | HO feels can overcome difficulties| 0.165           |
| How well managing financially     | 0.173           | How well managing financially     | 0.160           | How well managing financially     | 0.149           |
| HO feels lonely                   | 0.167           | HO feels can overcome difficulties| 0.135           | Subjective general health         | 0.138           |
| HO feels can overcome difficulties| 0.115           | HO feels isolated                 | 0.110           | HO feels lonely                   | 0.087           |
| HO feels lack of companionship    | 0.081           | HO feels lack of companionship    | 0.093           | HO feels isolated                 | 0.074           |
| Health limits work                | 0.060           | HO feels lonely                   | 0.091           | HO feels lack of companionship    | 0.068           |
| Frequency of posting on social    | 0.037           | Health limits work                | 0.035           | Household income level scale      | 0.043           |
| HO feels isolated                 | 0.036           | Relationship status               | 0.016           | Health limits work                | 0.023           |
| Relationship status               | 0.031           | Health limits moderate activities | 0.010           | Frequency of posting on social    | 0.013           |
| Own property                      | 0.021           | Own property                      | 0.010           | Individual income level scale     | 0.012           |
| Smoker                            | 0.014           | Frequency of posting on social    | 0.007           | Local authority property          | 0.007           |
| Health limits moderate activities | 0.012           | Household income level scale      | 0.007           | How many days vigorous activity   | 0.006           |
| Household income level scale      | 0.009           | Smoker                            | 0.006           | Relationship status               | 0.004           |
| Local authority property          | 0.008           | Individual income level scale     | 0.004           | Smoker                            | 0.003           |
| How many days vigorous activity   | 0.004           | Private renting                   | 0.001           | LS physical or mental disability  | 0.002           |
| Individual income level scale     | 0.002           | How many days vigorous activity   | 0.000           | Health limits moderate activities | 0.001           |
| Private renting                   | 0.000           | Local authority property          | 0.000           | Own property                      | 0.001           |
| LS physical or mental disability  | 0.000           | LS physical or mental disability  | 0.000           | Private renting                   | 0.001           |

## Mean absolute SHAP values - limited set of variables

This final section of the analysis considers the mean absolute SHAP values for the XGBoost models applied to the objective variables limited dataset. The subjective variables limited dataset is not being considered in-depth as, given the extended dataset relied more heavily on subjective variables, the SHAP is likely to be similar for the limited dataset containing subjective variables only. Here, we are interested in whether the order of objective variables changes when the models make predictions on datasets containing only objective variables.

The top objective variables are largely similar across age groups, and remain the same both pre and post COVID-19. Consistently, the most important variable for predictions across age groups is health limits work. Interestingly, with the extended model, having a long standing physical or mental health condition was not so much of an important predictor in the model as it is for the limited objective only model. This likely points to the mediating and indirect affects being captured between variables in the extended model, making other objective variables more important than they are in the objective only model, due to the interaction effect with other, subjective predictors.

#### Table 14: Ordered Mean Absolute SHAP Values for Features by Age Group in 2018 Dataset (Limited Set of Variables)

| Feature                           | Age 16-35 SHAP  | Feature                           | Age 36-59 SHAP  | Feature                           | Age 60+ SHAP    |
|-----------------------------------|-----------------|-----------------------------------|-----------------|-----------------------------------|------------------|
| Health limits work                | 0.254           | Health limits work                | 0.310           | Health limits work                | 0.278           |
| LS physical or mental disability  | 0.141           | LS physical or mental disability  | 0.116           | Household income level scale      | 0.098           |
| Relationship status               | 0.086           | Relationship status               | 0.084           | Health limits moderate activities | 0.079           |
| Household income level scale      | 0.086           | Household income level scale      | 0.065           | LS physical or mental disability  | 0.065           |
| Smoker                            | 0.078           | Own property                      | 0.047           | Own property                      | 0.038           |
| How many days vigorous activity   | 0.055           | Health limits moderate activities | 0.037           | Individual income level scale     | 0.032           |
| Own property                      | 0.031           | Smoker                            | 0.029           | Smoker                            | 0.028           |
| Council flat rent                 | 0.013           | How many days vigorous activity   | 0.017           | Relationship status               | 0.027           |
| Individual income level scale     | 0.011           | Individual income level scale     | 0.014           | How many days vigorous activity   | 0.012           |
| Health limits moderate activities | 0.003           | Council flat rent                 | 0.012           | Council flat rent                 | 0.005           |
| Private rent                      | 0.003           | Private rent                      | 0.001           | Private rent                      | 0.004           |

#### Table 15: Ordered Mean Absolute SHAP Values for Features by Age Group in 2021 Dataset (Limited Set of Variables)

| Feature                           | Age 16-35 SHAP  | Feature                           | Age 36-59 SHAP  | Feature                           | Age 60+ SHAP    |
|-----------------------------------|-----------------|-----------------------------------|-----------------|-----------------------------------|------------------|
| Health limits work                | 0.222           | Health limits work                | 0.254           | Health limits work                | 0.277           |
| LS physical or mental disability  | 0.128           | LS physical or mental disability  | 0.135           | Household income level scale      | 0.097           |
| Relationship status               | 0.117           | Relationship status               | 0.109           | Health limits moderate activities | 0.083           |
| Own property                      | 0.068           | Health limits moderate activities | 0.074           | LS physical or mental disability  | 0.081           |
| Household income level scale      | 0.062           | Own property                      | 0.064           | Relationship status               | 0.071           |
| How many days vigorous activity   | 0.056           | Household income level scale      | 0.062           | Individual income level scale     | 0.042           |
| Smoker                            | 0.054           | How many days vigorous activity   | 0.046           | Frequency of posting on social    | 0.033           |
| Health limits moderate activities | 0.040           | Individual income level scale     | 0.041           | Own property                      | 0.032           |
| Frequency of posting on social    | 0.037           | Smoker                            | 0.023           | Local authority property          | 0.024           |
| Individual income level scale     | 0.034           | Frequency of posting on social    | 0.016           | Smoker                            | 0.012           |
| Local authority property          | 0.026           | Local authority property          | 0.004           | How many days vigorous activity   | 0.010           |
| Private renting                   | 0.006           | Private renting                   | 0.001           | Private renting                   | 0.003           |




