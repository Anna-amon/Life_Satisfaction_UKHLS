# Life_Satisfaction_UKHLS

Drawing upon the UKHLS data set, this analysis revealed an overall significant decrease in life satisfaction for each age group, with those aged 60+ and 16-35 being the hardest hit. Having poor mental well-being, alongside being lonely, socially isolated and lacking in companionship are important predictors of low life satisfaction across all ages. This indicates the importance of subjective indicators in predicting life satisfaction. In terms of objective indicators, having a health condition, poor health behaviors,  and living in rented accommodation are all important predictors of low life satisfaction across age groups. Being single and having low income also predict low life satisfaction, but these mostly appear as stronger predictors for the two youngest age groups. Posting on social media regularly predicts low life satisfaction for the oldest age group, but the results are mixed for the two youngest age groups. The granular analysis of the mean absolute SHAP values indicates a potential ceiling effect of life satisfaction across age groups. For these reasons, social policy initiatives should focus on improving the well-being of those at the lower end of the life satisfaction scale. These social investments should cut across age groups, but a particular focus on both younger and older adults may be needed due to the more significant decline being seen for these age groups. A future longitudinal study considering whether or not life satisfaction has declined more substantially post-COVID-19, for individuals whose life satisfaction was already below average pre-COVID-19, may be beneficial to provide clarity. Future policies need to prioritize mental health improvement initiatives, but these initiatives may need to be holistic in their approach, considering how community resources can develop social connection, alongside improved access to healthcare, a reduction in poor access to resources due to ill health, and increased financial support for those who need it. In particular, these interventions may need to consider inequality of resources, how this has been exacerbated by COVID-19, and how people understand their position in relation to others, when attempting to improve life satisfaction for those reporting the lowest well-being scores. 

# Life Satisfaction - background

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

# Life Satisfaction - Age

Perhaps one of the most significant findings relating to life satisfaction research is the U-shaped happinesscurve. This pattern describes how well-being is often highest in adolescence, then starts to decline from age 18, reaching its lowest points around age 35-50, with age 47 being the very lowest (Blanchflower 2007). After age 50, well-being starts to rise, reaching its highest point post 60 years (Blanchflower 2007). This pattern appears congruent in the UK, Europe and English-speaking countries outside of Europe (Blanchflower 2007).However, it is not universal (Steptoe et al., 2015). Easter European countries that used to form part of theSoviet Union show a decline in life satisfaction with age, and Sub-Saharan Africa and Latin America showonly minors shifts with age (Steptoe et al., 2015).

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

Young people’s lives are frequently characterised by a lack of economic stability and capital, both of which make it harder to navigate adversities. For example, young people are more likely to private rent, and live with strangers, which can put strains on their social lives and affect their mental health (Veeroja et al,.2023). Additionally, older people were, in general, perhaps less impacted by the economic affects of the pandemic and are less likely to have children living at home, which may prevent them from having the same
sleep problems and worries young people may be experiencing (Banks & Xu 2020). This is not to say that older age groups have not been affected - particularly in terms of the health consequences of the pandemic, older people were likely to experience worst outcomes (Lee et al., 2024). However, the focus here is on life satisfaction and well-being, and evidence shows younger people in general to be more negatively affected.

The decline in life satisfaction is a concern across all age groups, and we can see that the decline in life satisfaction may relate to inequalities beyond just age, such as income, gender and ethnicity. However, the decline in life satisfaction for younger age groups is particularly concerning when we consider longevity and the aging population. Within the UK, life expectancy is increasing, however, the average number of years spent in poor health is also increasing. This means although people are living longer, they are spending a
larger proportion of their lifetime in poor health (McKee et al. 2021). The health and social care issues this bring are compounded by the fact that a higher proportion of those aged over 50 are now living alone and do not have children to care for them (Centre for Ageing Better, 2024). Inequalities faced by people when they are younger can have compounding effects throughout their lifetime, resulting in difficulties with health and wealth later in life. Younger generations are therefore required to be more resilient and better
prepared to deal with economic and social instability throughout their lives, yet an individual’s subjective sense of well-being in older age may also depend on the fulfilment of their expectations. Unmet expectations in young people may lead to difficulties in adapting to adversity in later life, and such expectations may be perceived particularly strongly where the ability to keep up with an immediate peer group and comparison of your own circumstances to others is being perpetuated by widening levels of inequality and economic egalitarianism. The decline we are seeing in life satisfaction among younger people may therefore have long-lasting effects, influencing their health, social connectivity, and economic stability as they age.

# Life Satisfaction - Summary

We can see overall how reductions in life satisfaction are associated with decreased mortality, unemployment, lower productivity, poor physical and mental health, fewer social relations, limited leisure time, lower income satisfaction compared to reference groups, and a reduction in life expectancy. Increases in life satisfaction are associated with higher mortality and employment rates, increased years spent in good health, employee retention, productivity, feeling socially connected, trust in the community, a sense of belonging, increased physical activity, high-income satisfaction compared to reference groups, and higher life expectancy. The benefits of these interventions in some cases are evidenced as bi-directional; individuals with high life satisfaction are more likely to socialize, be employed, and be connected to their wider community, in addition to taking care of their physical and mental health, which in turn, may further improve life satisfaction. However, in order for people to be able to adopt a lifestyle that fosters high well-being, policy interventions that aid individuals to do so are essential.

The ability of the population, and in particular, young people, to bounce back during social and economic adversity will depend on their immediate environment and whether this nurtures the resources needed to improve well-being. This environment requires the key ingredients necessary to foster a high degree of resilience necessary to withstand change - a degree of equality in resources and social mobility, financial and emotional support, access to good quality medical care, and options for satisfying leisure time. It is
necessary for social policy aimed at improving well-being to consider both subjective and objective factors and to appreciate the holistic and interconnected nature of all of these, rather than heavily relying on one area. To gain a more in-depth, comprehensive, and robust understanding of how these subjective and objective variables relating to life satisfaction interact with one another, specific and granular measurements of some of these sub-components are needed.

## Analysis

# Data Source and Variables

The first focus of this study is whether or not life satisfaction has declined for all age groups from 2018 -2021, and whether the decline has been worse for younger people. The second focus is to provide a more granular analysis of whether or not the main predictors of life satisfaction differ by age. To complete the analysis, we have used survey data from the UKHLS, a large, longitudinal questionnaire, with Waves 1-13 available from Data Service UK.

The calendar Year 2021 dataset includes individuals from waves 11, 12 and 13. This dataset has already been created and is available from the UK Data Service. There are a series of data frames for the 2021 dataset that have been aggregated in this analysis via linking. For this analysis, the main dataset used is indresp which contains most of the mainstage variables needed. This analysis combined indresp with hhresp, which contains data on all people in the household. The datasets were merged on the variable klmhidp. The second dataset, the calendar year 2018 dataset, is not available from the UK Data Service. To create this dataset, the three waves from dataset indresp, namely waves i, j, and k, covering 2018, are combined into a long format. Firstly, to match individuals in each wave with their household level data, a different approach was taken to the 2021 dataset, as we are dealing with different waves for individual and household level files, as opposed to two calendar year files, each with waves already combined, as seen in the 2021 dataset. The individual datasets for each 2018 waves were merged with the household level datasets for the corresponding wave, using a left join and matching on hidp. These three final datasets for each wave, which now include individual and household level data, were then aggregated into a final 2018 dataset, using an outer join and matching on each unique pidp for every individual.

The majority of variables for the 2018 dataset have been answered at each wave. However, those that were not are filled as NaNs. The final dataset for 2018 has a considerable number of variables due to combining the datasets using left and outer joins. This is necessary to create final calendar year variables using combinations of variables across each wave. New calendar year variables have been created to combine the results from each wave, the majority of which used the mean across all three waves for each pidp. One example of this is the life satisfaction variable, which for most people, was answered at each wave. For those that are categorical, and have more than 2 categories, the new variable is created using the mode instead. The age variable has been re-coded into subsets of individuals aged 16-35, 36-59 and 60+. Finally, after combining waves and datasets, each calendar year dataset resulted in three, smaller datasets, one for each age group. Therefore we have six datasets in total. The number of individuals in each dataset can be seen
in Table 1.

