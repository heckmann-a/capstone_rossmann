# capstone_rossmann

# Aufgabenstellung:
### Die Ermittlung von Vorhersagen der wöchentlichen Umsatzerlöse für den Drogeriemarkt Rossmann.
Dieses Projekt soll untersuchen, welche Erkenntnisse Rossmann gewinnen kann aus den eigenen historischen Verkaufs- und Werbedaten sowie Daten zu Ferien, Feiertagen und Wettbewerbern.\
Aktuell sind Filialleiter beauftragt, 8-Wochen-Prognosen zu erstellen.\
Daher sind Data Scientists des Unternehmens angewiesen worden, eine genaurere Vorhersagemethode zu ermitteln als die bisherige, über den histotischen Mittelwert.\
Die Zielfrage ist, wie man diese Daten nutzen kann, um den Betrieb zu optimieren und mehr Umsatz zu generieren.

# Datenquellen:
train.csv und store.csv: https://www.kaggle.com/c/rossmann-store-sales/data

# Technologien & Libraries:
* Python in Jupyter Notebook
* libs: pandas, numpy, seaborn, sklearn, IPython

# Beschreibung des Vorgehens:
* Daten eingelesen und bereinigt.
* Ein Teil der Daten vorbereitet, in dem die täglichen Daten in wöchentliche Intervalle aggregiert werden.
* Ein anderer Teil der Daten wird auf die Gesamtsumme der Tage aggregiert, um eine faire Performanceanalyse durchzuführen. Da einige Filialen in bestimmten Zeiträumen geschlossen waren.
* Relevante Datensätze miteinander kombiniert, um daraus eine explorative Datenanalyse durchführen zu können.
* Auswahl eines Machine-Learning-Modelltypen und vergleich mit der Durchschnittsmethode. (Die Durchschnittsmethode verwendet den historischen Mittelwert der vergangenen Beobachtungen.)
* Ermittlung der Prognosen.

# Ergebnisse:
Durch Auswahl eines geeigneten ml-modells kann die Genauigkeit drastisch gesteigert werden.\
Hier als Beispiell für die Filiale 764:

<img src="https://github.com/user-attachments/assets/9325125d-7bed-42d7-a04f-d7cdfe977b29" width=60% height=60%>

Mit der entsprechenden Prediction für das 8-Wochen-Intervall:

![predict764](https://github.com/user-attachments/assets/569d882f-7297-4443-b462-6b5351a9e01b)

# Auswertung der ML-Modelle:
Die besten Ergebnisse (absteigend): 
* Grandiant Boosting (95,7%)
* Random Forest (94,6%)
* MLPRegressor (82,8%)
* SGDRegressor (71,5%)

Am schlechtesten hat die Durchschnittsmethode für den historischen Mittel abgeschnitten.

![mlresults](https://github.com/user-attachments/assets/c3f2272f-e03b-4715-9075-f55be30ceb74)
