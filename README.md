# Employer-Review
Employer Review About Their Organization

<hr>

# Background
![dataset.png](https://raw.githubusercontent.com/ReynaraEzra/Employer-Review/main/images/Indeed%20Review.png)
Employer Review is a form that refers to content written by an employer or employee against his company that can be uploaded publicly or not. Every organization certainly needs someone to move the organization. Therefore, every review given to a product, service, or related to the company will certainly have an impact on the company. Every review, whether positive or negative, will influence the decision of a person or group of people who want to join, use services, or buy products from the company. By knowing how the reviews given by employees to the company, it is hoped that the company can evaluate if there are many negative reviews or maintain performance and continue to innovate if there are positive reviews.

## Audience
This problem can occur in organizations or companies around the world. As an organization that always wants to grow, it is only natural that service improvement is carried out based on the reviews provided. The use of this case can be used for company management to see how employees view their company so that further analysis can be carried out.

## Dataset
Source dataset retrieved via https://www.kaggle.com/muhammedabdulazeem/employer-review-about-their-organization. Data was collected on the Indeed website which is one of the world's #1 job vacancies with over 250 million unique visitors2 each month. Indeed is committed to putting job seekers first, giving them free access to job search, CV creation, and company research. Every day Indeed connects millions of people to new opportunities.

Description of columns:
<br>
| Columns                           |   Description                                                     |
|:----------------------------------|------------------------------------------------------------------:|
| **ReviewTitle**                   | The topic of the review.                                          |
| **CompleteReview**                | rating from the reviewer, from 1 (unsatisfied) to 5 (satisfied)   |
| **URL**                           | Uniform Resource Locator                                          |
| **Rating**                        | The rating given by company employees                             |
| **ReviewDetails**                 | Details about reviews.                                            |

## Plan
The problem to be solved is to create a model to perform text classification on reviews given by employees to the company. The information that will be obtained is to find out whether the type of review given is `positive`, `neutral`, or `negative`. The model creation process begins with preprocessing data, conducting exploratory data analysis (EDA) processes, building deep learning models using a neural network architecture with an embedding layer and `LSTM`, performing upside processes to improve model performance, selecting the best model, and making predictions for text review. which is not yet known.

## Conclusion
- After carrying out the `Exploratory Data Analysis (EDA)` process, the average rating given by employees to the company is **4.053/5** which indicates that the majority of the reviews given are positive. Based on the type of employee, more reviews are given by Former Employees, which are **79377** reviews compared to Current Employees with **65672** reviews. Based on the year, **2017** was the year with the highest number of reviews compared to other years. Based on the month, March is the month with the highest number of reviews compared to other months. The 5 companies with the highest number of reviews are `Tata-Consultancy-Service`, `IBM`, `Infosys`, `Accenture`, and `Cognizant Technology Solutions` with the number of reviews for each company exceeding **8000** reviews. Viewed by type of employee, employees with former employee status give more high rating values than employees with current employee status.
- The process of predicting reviews given by employees to their companies can be predicted using the Deep Learning process with Neural Network architecture. The process is carried out by performing a `tokenizer` with the `num_words` parameter adjusted to the selection of the effective word count by looking at the occurrence of the frequency of each word in the text and a padding process is carried out to make the length of each sentence the same. Then the Neural Network architecture is made using the Embedding layer to group words that have similar meanings and is given a `Long Short Term Memory (LSTM)` layer to recognize the meaning of a sentence based on the word order in the sentence. Based on this Neural Network architecture, 4 models were built, namely `model_1` for the model without oversampling process and without removing stopwords, `model_2` for the model without oversampling process and with removing stopwords, `model_3` for the model with the oversampling process and without removing stopwords, and `model_4` for the model with process oversampling and with the removal of stopwords. Using these four models, the accuracy value is **77.40%** for `model_1`, **77.02%** for `model_2`, **60.87%** for `model_3` and **57.76%** for `model_4`. So, to make predictions in the next review classification, `model_1` can be used, namely a model without oversampling and without removing stopwords.


## Reference : 
- https://www.nltk.org/
- https://docs.python.org/3/library/re.html
- https://www.geeksforgeeks.org/removing-stop-words-nltk-python/
- https://www.geeksforgeeks.org/python-stemming-words-with-nltk/
- https://docs.python.org/3/library/re.html
- https://www.kite.com/python/answers/how-to-use-re.sub()-in-python
