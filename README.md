# rumour-veracity
Course project for Text Analysis and Retrieval at Faculty of Electrical Engineering and Computing, University of Zagreb


[Competition website][1]  \
[Dataset][2] 

Entry points: 
 > [RumourEval 2019: Determining Rumour Veracity and Support for Rumours][3] \
 > [SemEval-2017 Determining rumour veracity and support for rumour][4]


Additional works:
 > [Joint Rumour Stance and Veracity][5] \
 > [Veracity assessment of online data][6]

Previous submissions:
 > [1][7]\
 > [2][8]\
 > [3][9]

[1]:https://competitions.codalab.org/competitions/19938
[2]:https://figshare.com/articles/dataset/RumourEval_2019_data/8845580
[3]:https://aclanthology.org/S19-2147.pdf
[4]:https://aclanthology.org/S17-2006.pdf
[5]:https://aclanthology.org/W19-6122.pdf
[6]:https://www.sciencedirect.com/science/article/pii/S0167923619301617
[7]:https://www.acl-bg.org/proceedings/2017/RANLP%202017/pdf/RANLP005.pdf
[8]:https://arxiv.org/pdf/1704.07221.pdf
[9]:https://aclanthology.org/S17-2086.pdf



# Solution draft

#### Data format
* user_metadata (that can be extracted from data)
* post_id
* post_content
* parent_post_id (null for source posts)

The rest should be discarded.

#### Preprocessing
Tools: spaCy

* tokenization
* stopword removal
* 
* 

## Subtask A

SDQC classification of tweets and Reddit comments/posts

Type of ML task: multiclass classification \
Input: a) **isolated comment** b) comment sequence \
Output: class label \
Features: \
* word-vector
* sentiment (extracted using sentiment analysis tools)
* post_content length
* question mark present
* exclamation mark present
* count of standard negative connotation words (word set to be defined)
* count of standard positive connotation words (word set to be defined)
* similarity to the source post (cosine)
* capitalization

#### Evaluation method: model selectionofficial competition evaluation metric, microaveraged accuracy, statistical significance testing, comparison to baseline and previously submitted work

Possible problems:
* Distribution of classes is skewed towards comments \
Possible solutions:
* First classify posts to comments and non-comments, then do the SDQ classification on non-comments, as suggested in previous works

Possible models: multiclass SVM, multinomial logistic regression
Choosing a best performing model vs. majority voting

## Subtask B

Determining rumour veracity

Open vs. **closed** variant


## Project timeline
* **week 6** - data loading and formatting module
* **week 7** - Subtask A - Defining models, features, feature extraction tools and methods
* **week 8** - Subtask A - Feature extraction, model training and evaluation
* **week 9** - Subtask A - Model training and evaluation
* **week 10** - Subtask B  
* **week 11** - Subtask B
* **week 12** - Research paper writing and final corrections
* **week 13** - Submission



