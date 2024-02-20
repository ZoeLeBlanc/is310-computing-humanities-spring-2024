---
permalink: /dataset-creation
title: Build your own dataset! 
toc: true
toc_sticky: true
author_profile: false
---

This week, we discussed infrastructures, scale, representation and different barriers to the availability and accessibility of humanities data. Today, you will be working together on a hands on activity to practically explore some of these gaps and frictions by going through process of creating your own humanities dataset. 


## Group Activity

Working in groups of around 4, create a group Google Doc named Dataset Curation - [Group #] and share it with the class Slack channel.

Your goal for this assignment is to collaboratively create a new dataset that can be used to explore a cultural phenomenon broadly defined. This should be obtainable from publicly available data and shouldn't just be copied from another dataset from sites such as Kaggle or journal publications.

Some example topics: bestselling novels, viral tweets, blockbuster movies, Instagram posts, or music reception. 

Here's a short example of one type of data you could collect (but certainly not limited to this).


| Movie Title      | Director Gender | Oscar Nominations | Budget (Million $) | Gross (Million $) | Bechdel Test Passed? |
|------------------|-----------------|-------------------|--------------------|-------------------|----------------------|
| Barbie           | F               | 8                 | 151                | 1,445             | Yes                   |
| Avatar           | M               | 9                 | 237                | 2,847             | No                   |


### Defining the shape (schema) of your data

- [ ] After you come up with an area, brainstorm some fields for your dataset. Come up with at least 6 fields, both numeric and text, that could define your dataset. In addition to the movie example above, this could include things such as number of likes on social media posts, or more subjective evaluations like the quality of a work or the emotional valence of a TikTok. 
- [ ] Discuss different potential research questions this data can tackle. What dimensions were missing from the initial fields you brainstormed? Are there any that are superfluous to potential research questions?
- [ ] What are potential exclusions in your dataset? Are there potential groups of people who are impossible to represent in your schema? Are there categories that reinforce stereotypes or binaries?
- [ ] Finalize the six fields. Include at least one of each: text data (e.g. author, full text, title, social media platform), numerical data (revenue, readership, likes), and subjective data (quality of work, emotional valence of social media post, toxcicity)

Make a Google Sheets that contains your data and link it in your Google Doc. 


### Gathering data

Once you collectively agree on a topic and the fields, you can begin collecting data. 
You are free to use web scraping or programmatic API techniques, but simply doing research with Google or Wikipedia should suffice for most tasks. 
You can also directly collect samples of social media data by browsing and viewing posts. 

- [ ] Collect at least 4 different rows in your dataset per person. If one of your fields is missing or impossible to find, make a note. 
- [ ] Did you discover any problems with the way you defined the categories that didn't align with the data you observed in the real world? 
- [ ] Look over your teammates' entries: do you agree with all the information they found? Focus especially on the subjective category(s). Do you agree with their judgement? Brainstorm some ways that you can make the decisionmaking process more consistent. 


### Reflection and evaluation
Answer the following questions in the Google Doc:
- [ ] Is your dataset representative? Are there any glaring expections of groups of people or categories which have been excluded?
- [ ] Discuss the strategies you used to select samples for your data. Did you simply go through Google search results? Rely on social media algorithms to sort and retrieve posts? Decide based on your own tastes or preferences? How does your choice of selection criterion impact the examples you found?
- [ ] Finally, ask ChatGPT to generate a table with your area and fields.

| Movie Title      | Director Gender | Oscar Nominations | Budget (Million $) | Gross (Million $) | Bechdel Test Passed? |
|------------------|-----------------|-------------------|--------------------|-------------------|----------------------|
| Avatar           | M               | 9                 | 237                | 2,847             | No                   |
| Titanic          | M               | 14                | 200                | 2,195             | Yes                  |
| The Avengers     | M               | 1                 | 220                | 1,518             | No                   |
| Jurassic Park    | M               | 3                 | 63                 | 1,033             | No                   |
| The Lion King    | M               | 4                 | 45                 | 1,656             | No                   |
| Frozen           | F               | 2                 | 150                | 1,280             | Yes                  |
| Black Panther    | M               | 7                 | 200                | 1,346             | Yes                  |
| Harry Potter and the Sorcerer's Stone | M  | 3           | 125                | 974               | No                   |
| The Dark Knight  | M               | 8                 | 185                | 1,005             | No                   |
| Inception        | M               | 8                 | 160                | 829               | No                   |


- [ ] Compare the quality of your data with the sample provided by ChatGPT. Discuss any obvious errors or exclusions you observe. Does ChatGPT's judgment on the subjective field align with your choices? 
