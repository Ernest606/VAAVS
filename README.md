# Vartotojų atsiliepimų analizės variklio sukūrimas

## Tikslas
Sukurti atsiliepimų analizės įrankį, kuris atskirtų teigiamus ir neigiamus atsiliepimus, išskirtų grupę atsiliepimų, į kuriuos reikia sureaguoti, bei palygintų tris atsiliepimų klasifikavimo modelius.

## Duomenų rinkinys
Šiam projektui buvo naudojamas Yelp atsiliepimų duomenų rinkinys.
https://www.kaggle.com/datasets/omkarsabnis/yelp-reviews-dataset/data

## Metodai
- Teksto vektorizavimas: TF-IDF vektorizavimas
- Naudoti modeliai: Logistinė regresija, Atsitiktinių miškų modelis, Dirbtinis neuroninis tinklas

## Rezultatai
- Modelių palyginimas pagal Accuracy, Recall ir F1 score.
  - **Dirbtinis neuroninis tinklas**: Geriausias modelis su Accuracy: 0.91, Recall: 0.965, F1 score: 0.945
  - **Logistinė regresija**: Modelis su Accuracy: 0.888, Recall: 0.991, F1 score: 0.934
  - **Atsitiktinių miškų modelis**: Geriausias modelis su Accuracy: 0.828, Recall: 0.997, F1 score: 0.902

## Atsiliepimų, į kuriuos reikia sureaguoti, identifikavimas
Yra galimybe nustatyti raktinius zodsius, kuriuos radus atsiliepimas taps reakcijos reikalaujanciu
Taip pat atsiliepimas taps reakcijos reikalaujanciu jeigu medelio atsiliepimo sentimento analizes rezultatas bus lygus 0. 

## Išsaugoti modeliai
- `logistic_regression_model.pkl`: Išsaugotas Logistinės regresijos modelis
- `random_forest_model.pkl`: Išsaugotas Atsitiktinių miškų modelis
- `neural_network_model.pkl`: Išsaugotas Dirbtinis neuroninis tinklas
