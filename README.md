# NaturalLanguageProcessing

Projektname: Natural Language Processing

Anleitung zum Betrieb des Codes:

1. MyBinder über den BinderBatch öffnen
2. Nach dem öffnen des MyBinder, das Notebook ist auf der Linken Seite der Webpage zu finden, durch doppelklick wird es geöffnet.
3. Über den PlayButton können Sie das Notebook Schritt für Schritt durchführen.
    
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Phips91/NaturalLanguageProcessing.git/HEAD)


Diese Dokumentation erläutert einen Python-Code für ein NLP (Natural Language Processing)-Projekt, bei dem Yelp-Bewertungen in Kategorien mit 1 Stern oder 5 Sternen klassifiziert werden. Das Projekt verwendet Textanalyse, insbesondere die Verarbeitung von Textdaten, um diese Klassifikation durchzuführen. Hier ist eine Zusammenfassung des Codes und der erwarteten Ergebnisse:

**Schritt 1: Imports**
In diesem Schritt werden die erforderlichen Python-Bibliotheken NumPy und Pandas importiert.

**Schritt 2: Daten einlesen**
Die Yelp-Bewertungsdaten werden aus einer CSV-Datei namens "Yelp.csv" eingelesen und in ein Pandas DataFrame mit dem Namen "yelp" geladen.

**Schritt 3: Datenüberblick**
Dieser Schritt bietet einen Überblick über die Daten. Es werden der Kopf des DataFrames ("yelp.head()"), Informationen zur Datenstruktur ("yelp.info()") und eine statistische Zusammenfassung der Daten ("yelp.describe()") angezeigt. Außerdem wird eine neue Spalte namens "text length" erstellt, die die Anzahl der Zeichen in der "text"-Spalte enthält.

**Schritt 4: EDA (Explorative Datenanalyse)**
In diesem Schritt werden Visualisierungen durchgeführt, um die Daten besser zu verstehen. Es werden Histogramme basierend auf den "stars" erstellt und ein Boxplot der Textlänge für jede Sternkategorie angezeigt. Außerdem wird ein Countplot erstellt, um die Anzahl der Bewertungen in jeder Sternkategorie anzuzeigen. Die durchschnittlichen Werte der numerischen Spalten werden für jede Sternkategorie berechnet und in einem separaten DataFrame namens "stars" gespeichert. Schließlich wird die Korrelation zwischen den numerischen Spalten in "stars" untersucht und in Form einer Heatmap visualisiert.

**Schritt 5: NLP-Klassifizierungsaufgabe**
Hier beginnt die eigentliche NLP-Klassifizierungsaufgabe. Es werden nur Bewertungen mit 1 oder 5 Sternen verwendet. Ein neues DataFrame namens "yelp_class" wird erstellt, das nur diese Bewertungen enthält. Dann werden zwei Objekte, "X" (Text) und "y" (Sterne), erstellt.

**Schritt 6: Textverarbeitung**
Der CountVectorizer wird importiert und ein CountVectorizer-Objekt ("cv") erstellt. Dieses Objekt wird auf den Text ("X") angewendet, um die Textdaten in numerische Vektoren umzuwandeln.

**Schritt 7: Train-Test-Aufteilung**
Die Daten werden in Trainings- und Testsets aufgeteilt, wobei 70% der Daten für das Training und 30% für Tests verwendet werden. Dies wird mithilfe der Funktion "train_test_split" durchgeführt.

**Schritt 8: Modelltraining**
Ein Multinomial Naive Bayes-Modell (NB) wird erstellt und auf den Trainingsdaten angepasst.

**Schritt 9: Vorhersagen und Auswertung**
Das trainierte Modell wird verwendet, um Vorhersagen für die Testdaten zu treffen. Es wird eine Confusion Matrix und ein Classification Report erstellt, um die Leistung des Modells zu bewerten.

**Schritt 10: Verwendung von TF-IDF**
Es wird die Verwendung von TF-IDF (Term Frequency-Inverse Document Frequency) in die Pipeline integriert, um die Textdaten zu verbessern.

**Schritt 11: Pipeline verwenden**
Die Pipeline wird genutzt, um die Daten erneut zu verarbeiten und das Modell zu trainieren. Es wird erwartet, dass die TF-IDF-Integration die Ergebnisse beeinflusst.

**Schritt 12: Vorhersagen und Auswertung mit TF-IDF**
Die Pipeline wird verwendet, um Vorhersagen für die Testdaten zu treffen. Es wird erneut eine Confusion Matrix und ein Classification Report erstellt, um die Leistung des Modells mit TF-IDF zu bewerten.

Die erwarteten Ergebnisse des Codes sind:

- Eine detaillierte Analyse der Yelp-Bewertungsdaten, einschließlich Visualisierungen und statistischer Zusammenfassungen.
- Die Klassifizierung von Yelp-Bewertungen in 1-Stern- oder 5-Stern-Kategorien mit einem Multinomial Naive Bayes-Modell.
- Die Auswertung der Modellleistung durch Confusion Matrices und Classification Reports sowohl für das ursprüngliche Modell als auch für das Modell mit TF-IDF.
- Die Möglichkeit zur weiteren Verbesserung des Modells durch Anpassung der Schritte in der Pipeline oder durch die Verwendung anderer ML-Klassifizierungsmodelle.

Der Code dient dazu, die Grundlagen des NLP und der Textklassifikation zu demonstrieren und wie diese auf reale Daten angewendet werden können, insbesondere die Verwendung von TF-IDF zur Verbesserung der Modellleistung.
