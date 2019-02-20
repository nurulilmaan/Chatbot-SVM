# Chatbot
Chatbot using Support Vector Machine and Cosine Similarity

## Getting Started

### Prerequisites
These are the things that you need for this project
```
Django == 2.1.2
django-cors-header
requests == 2.9.1
numpy == 1.15.4
pandas == 0.23.4
scikit-learn == 0.20.1
scipy == 1.1.0
```

### Dataset
Dataset fetched from [Informatika UNPAD](informatika.unpad.ac.id "Informatika UNPAD") and [UNPAD](unpad.ac.id/berita-unpad "UNPAD") and saved as ```QA.csv```

If you want to changed it, please select your own dataset, move to ```folder code/data/csv``` and change this code:
```
dataset = os.path.join(os.path.dirname(os.path.abspath(__file__)), "data", "csv", "changetoyourfilename.csv")
```

### User Interface
Because this is web based, using UI code from [Fabio Ottaviani](https://codepen.io/supah/pen/jqOBqp, "Direct Messaging UI") with some changes to fit the program.

### Support Vector Machine
Support Vector machine using [sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.svm.SVC.html "SVC").

### Cosine Similarity
Cosine Similarity using [sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html "Cosine Similarity").

## How It Works
The flow of this program is:
1. Observing website for the dataset
2. Preprocessing dataset
    1. Tokenization
    2. Stop Words Removal
    3. Stemming
3. Grid Search parameter to find optimal variable of C
4. Train SVM using Stratified 10-Fold
5. Get the user's message and preprocess it
6. Predict user message's label
7. Calculate the Cosine Similarity score for each dataset that has the same label as the user's message label
8. Get data that have the highest score
9. Reply with data that has been obtained from Cosine Similarity process
10. If score is below 0.5 then default message is given

## Authors
* **Nurul Ilma Asfiya N** - *Initial work* - [nurulilmaan](https://github.com/nurulilmaan)

## Reference
* [Indonesian Preprocessing](https://github.com/har07/PySastrawi) - PySastrawi
* [Banking FAQ Bot](https://github.com/MrJay10/banking-faq-bot) - MrJay10
* [FAQ Chatbot](https://github.com/donowhy/FAQ-Chat-Bot) - donowhy
* [Direct Messaging UI](https://codepen.io/supah/pen/jqOBqp) - Fabio Ottaviani
