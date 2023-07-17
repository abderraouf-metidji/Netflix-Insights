
# Netflix-Insights

 Project done using: 

`![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)`
`![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?style=for-the-badge&logo=jupyter&logoColor=white)`

## AI Watch

Let's start with a few definitions.

**<u>Artificial Intelligence</u>**: AI represents the theories and techniques used to develop complex programs that simulate aspects of the human intelligence (reasoning, learning...). AI encompasses a range of theories, techniques, and algorithms used to create intelligent systems that can perform tasks that typically require human intelligence.

**<u>Machine Learning</u>**: A technique used in programming that takes data and stats in order to give a computer program or model the capability to learn by themselves. We feed data to the computer program allowing it to identify patterns and make inferences. Once trained, the machine learning model can then be applied to new, unseen data to make predictions or decisions. It can recognize patterns, classify objects, predict outcomes, or perform other tasks based on what it has learned from the training data.

**<u>Supervised Classification</u>**: Supervised classification is a machine learning technique used to categorize or classify objects into different predefined classes based on a set of features or variables. It involves training a model on a labeled dataset, where each data instance is associated with a known class or category.

*<u>Example</u>*: Suppose you are working on a medical diagnosis task where you have a dataset containing various medical parameters of patients (such as blood pressure, cholesterol levels, age, etc.) along with their corresponding binary labels indicating whether they have a certain medical condition (e.g., diabetes or not). Your goal is to develop a supervised classification model that can accurately predict the presence or absence of the medical condition based on the given features. The problematic for supervised classification would involve training a model using the labeled data to learn the patterns and relationships between the input variables (medical parameters) and the target variable (medical condition). The model should be able to generalize from the training data and make predictions on new, unseen patient data.

**<u>Unsupervised Classification</u>**: Unsupervised classification is a machine learning technique used to discover patterns, relationships, or hidden structures in data without any predefined class labels or categories. Unlike supervised classification, unsupervised classification does not rely on labeled training data.

<u>*Example</u>:* Let's say that we have a dataset containing information about supermarket clients such as; age, income, purchasing history and so on. We would like an *Unsupervised Classification* in order to discover groups or segments of clients that are similar without using predefined categories. The *Unsupervised Classification* would then allow us to find a method or algorithm that regroups clients based on their shared characteristics without using a targeted variable. The goal would be to find clients that share similar purchasing habits, demographic profiles or other shared characteristics.

**<u>Descriptive Data Analysis</u>**: Descriptive Data Analysis is a statistical approach with the goal to explore, summarize and present the characteristics that are essential in a dataset. It allows the understanding and description of data in a concise and significant manner using visualization and stats. The goal of this analysis is to give an initial comprehension of the data, detect models or emerging tendencies, identify missing data etc.

*<u>Main techniques used</u>*:

* Measures of central tendency: These measures, such as mean, median, and mode, help understand the central or typical value of a variable.

* Measures of dispersion: They indicate the variability of the data and include standard deviation, range, variance, etc.

* Data visualization: Graphs and charts, such as histograms, box plots, scatter plots, etc., visually represent the data and highlight patterns or trends.

* Frequency analysis: It describes the distribution of data by counting the frequency of occurrence of different values or categories.

* Correlation analysis: It examines the relationships between variables and measures their degree of correlation using techniques such as Pearson correlation.

* Statistical summaries: They provide an overall overview of the data, including information on quartiles, percentages, ratios, etc.

---


### AI possibilities in a domain

Let's focus on the legal domain for this analysis / explanation of how AI can impact a domain and what it can do it that domain in particular.

Here are some example of how AI can improve Legal processes in a global manner:

- Legal Research: Utilizing AI, extensive datasets of legal documents, including laws, contracts, and regulatory documents, can be analyzed. This enables the extraction of valuable information, identification of legal trends, and assists lawyers in decision-making processes based on similar cases. Currently, this task is typically performed by paralegals.

- Contract Analysis: AI aids in the identification of key clauses, potential risks, and contractual obligations by analyzing previous contracts. This streamlines the review process and enhances lawyers' understanding of contractual implications and potential issues.

- Prediction of Judicial Results: By examining historical court decisions, AI can predict probable outcomes of legal disputes. This empowers lawyers to gauge the likelihood of success for a case and make informed strategic decisions.

- Automation of Repetitive Tasks: AI facilitates the automation of repetitive legal tasks such as generating standardized legal documents or producing reports for presentations or analyses. This allows lawyers to allocate their time and effort towards more critical matters.

- Case Law Analysis: AI supports lawyers in preparing their cases by analyzing prior cases, identifying patterns, motives, and legal interpretations. This enables lawyers to stay updated on potential changes or developments in the law.

- Virtual Assistance: Chat-bots or other AI-based virtual assistants can be utilized to answer common legal questions, provide information on general laws and regulations, and assist users in accessing relevant resources. This enhances accessibility to legal information and facilitates communication between lawyers and clients.

By leveraging AI in the legal domain, these advancements enhance efficiency, accuracy, and productivity for legal professionals. It is important to note that AI does not replace lawyers but rather complements their work by automating tasks and providing valuable insights for informed decision-making.


## Project & Data Context  

This project was used as an introduction to Data Analysis and the use of Jupyter Notebook. We have used a Netflix CSV that gives us a representation of the Netflix catalog and what it contains.

It has the following variables:
* show_id
* type
* title
* director
* cast
* country
* date_added
* release_year
* rating
* duration
* listed_in
* description  

| Variable     | Content                                                             |
| :----------: | :-----------------------------------------------------------------: |
| show_id      | id of the TV Show or Movie                                          |
| type         | gives us the information on whether it is a TV Show or a Movie      | 
| title        | title of the production                                             | 
| director     | name of the director                                                | 
| cast         | actors that were part of the production                             | 
| country      | country from which the production originated                        | 
| date_added   | date when the production was added to the catalog                   | 
| release_year | release year of the production                                      | 
| rating       | rating of the production (ex: PG-13)                                | 
| duration     | length of the production in minutes or in seasons                   |
| listed_in    | category in which the production is listed (comedy, drama, etc)     | 
| description  | a summary of the content of the TV Show, Movie                      | 

We have used these variables to generate graphs and analyze them in other to make observations and draw conclusions. 

There was missing data in the DataFrame:
* director: 29.91%
* cast: 9.50%
* country: 9.56%
* date_added: 0.11%
* rating: 0.05%
* duration: 0.03%

## Observations & Conclusion

The main thing that we were able to notice while working with this DataFrame is that the number of addition is decreasing. Meaning that Netflix has decided to lower the amount of content they add to their catalog. There was a constant increase until 2019 where it peaked at around 600 additions in a year for TV Shows and 1,400 for Movies. Then it started to decrease and in 2021 we reached about the same level of addition in a year than in 2017 for Movies (around 1,000) and 2019 for TV Shows (around 500).

With these numbers and the type variable we were also able to see that there are more than double the amount of Movies than TV Shows available in the Netflix catalog. It is around 70% for Movies and 30% for TV Shows.

But, we can also see that the number of Movies Added in a year has decreased much more than the number of TV Shows added in a year, 400 less Movies vs 100 less TV Shows. 

Also, we could also see that the release date of the Movies and TV Shows in the Netflix catalog is less recent. For example most of the Movies and TV Shows available are from 2018 (around 1,150). The number of Movies and TV Shows from 2021 for example is closer to 600. There are almost twice as many productions from 2018 available than productions from 2021 or 2016 for example. 

While observing the country from which these productions originate we could see that most of them come from the USA, which is not a surprise since they are the leader of Movie and TV Shows exportation around the globe. 

What is interesting is that we could see an increase in "foreign" (meaning non USA production) added to the Netflix catalog with an especially sharp increase for Indian production from 2016 to 2018. Since Netflix arrived in India in 2016 that might be the main reason.

This was a short analysis based on a few graphs. We didn't go in depth into some of the variable but we were able to get an overview of how Netflix content has evolved from the beginning to 2021 and how they focus on things like domestic productions when launching to a specific country. 