# Stack Overflow Question Status Classification

## This project demonstaring binary and multiclass classifaction on stackOverflow.com data
It involves using finetuned BERT models in order to classify question status into open/closed status and to attempt to prescribe some info as to why that quesation may have been closed with the multiclass BERT model. 

You can read more in the project report provided. 

#### In order to run the models it is recommened that you use google colab in order to avoid having to overwork your machine and to take advatage of gpu training 

### Steps to reproduce results (colab)
First upload the code in this github repo to google colab and unzip the data files provided and add them to your google drive.

Once you have uploaded the data and opened one of the notebookes in google colab you will be able to run the file. 
After running the mounting cell
```
from google.colab import drive
drive.mount('/content/drive')
```
use the colab prompt to allow access to your drive and ensure that the path is correct to that of your drive. 

Now you will be able to run the notebook succesfully. 

### Steps to reproduce results (local)
If you want to run the models locally you will need to edit the code that is using the google drive mounting features to access the data. You will need to change this path to be the path of the unzipped data files on your local machine. 

First unzip the data files and add them to the directory of the project

This will involve deleting the cell used to mount drive 
```
from google.colab import drive
drive.mount('/content/drive')
```

And also changing the file path to match that of your local system
```
df = pd.read_csv('/content/drive/MyDrive/stack_nlp_large.csv') - should become -> pd.read_csv('./data/stack_nlp_large.csv')
```