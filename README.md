# Chatbot
Chatbot using Support Vector Machine and Cosine Similarity

## Getting Started

### Prerequisites
These are the things that you need for this project
```
Django 2.1.2
Requests 2.9.1
Numpy 1.15.4
Pandas 0.23.4
Scikit-learn 0.20.1
Beautifulsoup4 4.6.3
Scipy 1.1.0
```

### Dataset
Dataset fetched from [Informatika UNPAD](informatika.unpad.ac.id "Informatika UNPAD") and [UNPAD](unpad.ac.id/berita-unpad "UNPAD") and saved as ```data.csv```

If you want to changed it, please select your own dataset, move to ```folder data/csv``` and change this code:
```
dataset = os.path.join(os.path.dirname(os.path.abspath(__file__)), "data", "csv", "changetoyourfilename.csv")
```

### User Interface
Because this is web based, the program use UI code from [Fabio Ottaviani](https://codepen.io/supah/pen/jqOBqp, "Direct Messaging UI")

### Support Vector Machine
Support Vector machine from scratch is used for this program.

### Cosine Similarity
Cosine Similarity from scratch is used for this program.

## How It Works
The flow of this program is:
1. Scraping website for the dataset
2. Preprocessing dataset
    1. Tokenization
    2. Stop Words Removal
    3. Stemming
3. Grid Search parameter to find optimal variable of C, tol and max_iter
4. Train SVM using Stratified K-Fold
5. Get the user's message and preprocess it
6. Predict user message's label
7. Count Cosine Similarity scores  for each dataset that has label same as user massage's label
8. Get data that have the highest score
9. Reply with data that has been obtained from Cosine Similarity process

## Authors

* **Nurul Ilma Asfiya N** - *Initial work* - [nurulilmaan](https://github.com/nurulilmaan)

## Reference

* [Multiclass SVM](https://gist.github.com/mblondel/97cffbea574a5890f0d7) - Mblondel
* [Indonesian Preprocessing](https://github.com/har07/PySastrawi) - PySastrawi
* [Banking FAQ Bot](https://github.com/MrJay10/banking-faq-bot) - MrJay10
* [FAQ Chatbot](https://github.com/donowhy/FAQ-Chat-Bot) - donowhy
