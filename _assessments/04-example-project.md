---
permalink: /assessments/04-example-project
title: Example Final Project
toc: true
toc_sticky: true
classes: wide
---

This is a very brief, example project to help you as you work to complete your final project. You are not expected to follow this example exactly, but hopefully it can help give you a sense of what a final project might look like. You are welcome to reuse some of the materials you generated for the proposal and project update.

This example will be built around our class example of exploring the Humanist Listserv [https://humanist.kdl.kcl.ac.uk/](https://humanist.kdl.kcl.ac.uk/). While the example below contains the overall structure, we will be discussing in class how to present this work publicly and how to document it in a way that is accessible to others (one of the requirements of the project), which will slightly change the structure of the final project though the content will remain the same.

# Sample Project: Humanizing Technology: Computationally Exploring the Humanist Listserv & the Rise of Web Technologies

## Introduction

- Ideally this section should introduce your project, why you decided to study it, and what you hope to achieve. The goal is to really explain why this topic is relevant to the course and interesting to you. I would also include any details about having to pivot or change your project, if that happened.
- In this section, I would lay out what the Humanist Listserv is and why I decided to study it. So for example, I might say something like the following:

> While working with cultural materials is relatively new, scholars have been experimenting with how computing can help us understand the humanities for decades. One of the earliest examples of this is the Humanist Listserv, a long-standing email listserv for the digital humanities community that has been in operation since 1987 and continues to run today. The archives of this listserv are publicly available and contain a wealth of information about how digital humanists have communicated with one another over the years. However, while this listserv is open and accessible, trying to understand the conversations that have taken place on it can be challenging. For example, much of the current listserv is provided as one long text file, which can be difficult to read and explore patterns over time. In this project, I explore how we can transform these listserv archives into data and in turn demonstrate how this  computational methods to understand the conversations that have taken place on the listserv.
> In particular, I'm interested in exploring how humanities scholars have discussed various technologies over time, especially since the listserv coincided with the rise of the internet. For instance, can we find patterns that correspond to the rise of the web, or the development of new tools like XML or TEI? Furthermore, do the types of problems and discourses stay the same but simply the names of the technologies change? By exploring these questions, I hope to demonstrate how we can use computational methods to understand the history of the digital humanities and how scholars have engaged with technology over time.

- In this section, I would also include a brief literature review of the Humanist Listserv to help explain how scholars have studied it and its origins. So for example, I might say something like the following:

> Scholars like Julia Nyhan have explored the history of the Humanist listserv. In her chapter, "In Search of Identities in the Digital Humanities: The Early History of Humanist," Nyhan traces the origins of the listserv and how it has evolved over time. She argues that the listserv has been a key site for the development of the digital humanities and has helped to shape the field in important ways. Established in 1987 by Willard McCarty, Humanist was conceived as a proto-social media platform that facilitated critical discussions on the intersection of computing and humanities, rather than serving as a mere publication outlet. The discourse within this community reflected a complex engagement with technology—while some members championed digital tools as a means to innovate and break down disciplinary barriers, others expressed reservations, warning against the potential dehumanization of the humanities. Such debates highlighted the community's struggle to balance traditional humanistic values with the opportunities presented by technological advancements, ultimately striving to define a new identity for humanities scholars that integrates digital methods while maintaining the discipline's core principles. This discourse on Humanist not only influenced humanities research practices but also highlighted the broader implications of digital integration in reshaping academic and disciplinary boundaries.[^nyhan]
> This project builds on Nyhan's work by exploring how we can use computational methods to understand the conversations that have taken place on the listserv and how these conversations have evolved over time.


## Data Collection & Curation

- In this section, I would describe how I collected and curated the data for this project. This could include everything from how I web scraped the listserv archives to how I cleaned and transformed the data. In particular, I would try to detail how I'm meeting this requirement of the project: "some form of hand curated or computationally derived data". In the case of the humanist listserv, I would likely detail how I would used named entity recognition and manual data cleaning to extract technologies and topics from the listserv archives.
- So I would try to have the following figures and details:
  - Show a sample of the website structure to contextualize and explain how I scraped the website, as well as detailing some of the code for scraping.
  - Show a sample of the initial scraped dataset and detail choices on how to structure the data, including any choices I eventually revised.  
  - Introduce named entity recognition and how I used it to extract technologies from the listserv archives. Show some of the pipeline and also any validation or iterations I had to make.
  - Show a sample of the final dataset and how I structured it for analysis, and detail the final documentation choices and discuss how the envisioned audiences who might use these datasets informed those choices.
- In this section, I would also include, if relevant, a brief discussion of how others have collected and curated data for similar projects. So for example, I might include the following projects/examples:
  - Scholars who have explored Usenet archives, which are early internet discussion forums, and how they have used computational methods to understand these archives.
  - Projects that have used named entity recognition to extract topics from large text corpora, and how they have structured and cleaned these datasets for analysis.
- And, I would include also any citations or quotations to readings from the course that are relevant:
  - So for example, I might include some references to *Data Feminism* because that influenced my approach to organizing this data.
- Finally, I would also include any reflections on how my thinking about data collection and curation process changed through this process.

## Data Analysis & Methods

- In this section, I would detail how I analyzed the data for this project and share some of the aggregate data visualizations of the data. In particular, I would try to visualize how the NER extracted technologies have changed over time and how they relate to the rise of the web. I would also detail some of the choices I've made in my use of methods and data visualizations to make my interpretations clear (so for example, things I did not include or experiments that I decided were not useful but provided a foundation for my thinking and later experiments/visualizations).
- I would also detail some experiments of using TF-IDF and topic modeling to understand the conversations on the listserv and how these methods helped me to understand the data. I might not have a final answer to my initial question but showing some trends and using those to speculate about how these technologies have changed over time and how they have been discussed on the listserv. I would also detail any challenges I faced in using these methods and how I overcame them.
- In this section, I would also include, if relevant, a brief discussion of how others have analyzed data for similar projects. So for example, I might include the following projects/examples:
  - Scholars and/or projects who have used topic modeling or TF-IDF to understand the historic documents and how they have visualized these results to understand the development of discourses.
- I would also again include relevant citations from our course readings and how they influenced my thinking about data analysis and methods.
  - So I might include a reference to Melanie Walsh and Maria Antoniak's work with GoodReads since that influenced my approach to topic modeling.
- Finally, I would also include any reflections on how my thinking about data analysis and methods changed through this process.

## Conclusion & Reflection

- In this section, I would detail any big picture takeaways about what I learned from this project and how it has helped me to understand working with cultural data and computing in the humanities, and then specifically what this project has found over how the development of technology over time shaped discourses on the Humanist Listserv.
- I would also reflect and summarize any challenges I faced in completing this project and how I overcame them, as well as any future directions I might take this project.
- Finally, I would also include any guidance for others who might want to utilize this data or methods in their own research, and how they might go about doing so.

---
    
[^nyhan]: Nyhan, Julia. "In Search of Identities in the Digital Humanities: The Early History of Humanist." *Social media archeology and poetics* (2016).