#  Duplicates in a series of question data
## File Contents
* [app/main.py](app/main.py) - python program to compute similarity bucketization based on user input. 
calculate elapsed time.
* [app/templates/index.html](app/templates/index.html) - home page html file.
* [app/templates/result.html](app/templates/result.html) - results page html file.
* [Procfile](Procfile) - list of process types in an app
## Data set
Dataset with the text of 10% of questions and answers from the Stack Overflow programming Q&A website.

https://www.kaggle.com/stackoverflow/stacksample?select=Questions.csv
## Deployed Python Flask App
https://naveen17euit093-duplicates.herokuapp.com/
## Algorithm 
Cosine similarity is the cosine of the angle between two n-dimensional vectors in an n-dimensional space. It is the dot 
product of the two vectors divided by the product of the two vectors' lengths (or magnitudes). We can use the 
Cosine Similarity algorithm to work out the similarity between two things
```
# clean strings - remove html tags and punctuations
cleaned = list(map(clean_text, input_data))
# create k vectors in n dimensional space, k - number of sentences and n - number of unique words in all sentences combined
vectorizer = CountVectorizer().fit_transform(cleaned)
# convert vector to array
vectors = vectorizer.toarray()
# calculate cosine similarity from vector
csim = cosine_similarity(vectors)
```
```
Total Data: 1264217
Questions Count: 100
Time elapsed:00:00:00
Questions Count: 1000
Time elapsed:00:00:03
Questions Count: 10000
Time elapsed:00:00:50
Questions Count: 100000
Time elapsed:00:01:19
Questions Count: 1000000
Time elapsed:00:01:47
```
Questions Count | Elapsed Time in Seconds |
:---: | :---: |
|100|< 0|
|1000|3|
|10000|50|
|100000|79|
|1000000|107|
## Screenshots
#### Home page
![Image](screenshots/home_page.png)
#### Results page - 100% similarity
![Image](screenshots/results_page_similarity_100.png)
#### Results page - 80% similarity
![Image](screenshots/results_page_similarity_80.png)
#### Results page - 0% similarity
![Image](screenshots/results_page_similarity_0.png)


In this application of finding the duplicates in the data,first of all we created the program using python in the web application by using flask.
with the help of flask it is uploaded in the web browser.
since it contains many files they are uploaded with the help of heruko the online host of the web.
they are all connected in them to application to apply the web.
By giving the data, they are used with the process of the hash set and they are used in the process and with the front end of html,css.

