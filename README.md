Fake News Detection

Fake News Detection in Python

This project, developed by Durga Sai Saketh, implements various natural language processing techniques and machine learning algorithms to classify fake news articles using Python’s Scikit-learn library.

Getting Started
These instructions will help you set up the project on your local machine for development and testing purposes. See deployment notes for live system implementation.

Prerequisites
Ensure you have the following installed:

Python 3.6
Download Python 3.6 from https://www.python.org/downloads/. After installation, set up the PATH variables if you want to run Python programs directly from the command prompt. You can follow instructions here: https://www.pythoncentral.io/add-python-to-path-python-is-not-recognized-as-an-internal-or-external-command/.
Alternatively, you can use Anaconda and its prompt to run the project. Download Anaconda from https://www.anaconda.com/download/.

Required Libraries
After installing Python or Anaconda, install the following libraries:

For Python:
pip install -U scikit-learn
pip install numpy
pip install scipy

For Anaconda:
conda install -c scikit-learn
conda install -c anaconda numpy
conda install -c anaconda scipy

Dataset
The project uses the LIAR dataset, which contains .tsv files for training, testing, and validation.

Original Dataset Columns:
1. ID of the statement
2. Label (True, Mostly-true, Half-true, Barely-true, FALSE, Pants-fire)
3. Statement
4. Subjects
5. Speaker
6. Speaker’s job title
7. State info
8. Party affiliation
9-13. Credit history counts (barely true, false, half-true, mostly true, pants on fire)
14. Context (venue/location)

For simplicity, only two columns were selected:
1. Statement (news headline/text)
2. Label (True, False)

Class Mapping:
Original -> New
True -> True
Mostly-true -> True
Half-true -> True
Barely-true -> False
False -> False
Pants-fire -> False

The processed datasets (train.csv, test.csv, valid.csv) are available in the repository.

File Descriptions
DataPrep.py: Preprocesses the data by reading files, tokenizing, stemming, and handling missing values.

FeatureSelection.py: Extracts and selects features using techniques like bag-of-words, n-grams, and tf-idf weighting.

classifier.py: Builds classifiers (Naive Bayes, Logistic Regression, Linear SVM, Stochastic Gradient Descent, Random Forest) and evaluates performance using f1 scores and confusion matrices.

prediction.py: Uses the best-performing model (Logistic Regression) to classify news articles and provides a probability of truth.

Performance
The Logistic Regression classifier performed best, with an f1 score in the 70s. Performance can be improved by using more data and advanced feature selection methods like POS tagging, word2vec, and topic modeling.

Installation and Execution
Clone the repository:
$ git clone https://github.com/Saketh562/FakeNewsDetectionSystem.git

For Anaconda:
Open Anaconda Prompt and navigate to the project directory:
cd C:/your/project/folder/path
Run the prediction script:
python prediction.py

For Python (without PATH setup):
Locate python.exe and use its full path:
c:/Python36/python.exe C:/your/project/folder/path/prediction.py

For Python (with PATH setup):
Navigate to the project directory:
cd C:/your/project/folder/path
Run the script:
python prediction.py

Input a news headline when prompted, and the program will classify it as “True” or “False” along with the probability of truth.

<hr>

Developed by Gedela Durga Sai Saketh
