# Pràctica Kaggle APC UAB 2022-23
### Nom: Oscar Moreno Ramos 
### DATASET: Pokemon with Stats
### URL: https://www.kaggle.com/datasets/abcsds/pokemon/code

El dataset utilitza dades que descriuen cada Pokemon on trobem les diferents estadístiques, el tipus i si es un Pokemon legendari o no.
Tenim 800 dades amb 13 atributs. 3 d'ells són categoric (Nom, Type 1 i type 2) i els altres 10 són numérics i estàn normalitzats.

### Objectius del dataset
Volem estudiar les dades del dataset, a més d'aprendre diferents models de processament de dades.
## Experiments
Durant aquesta pràctica hem realitzat diferents experiments, fent PCA i TSNE, a més de probar els mètodes de classificació de regressió logístic, SVM, KNN, Ensamble, Decision Tree i el Random Forest.
### Preprocessat
Com a proves per reduir la dimensionalitat em fet tant PCA com TSNE, així com el tractament de Nulls, en aquest cas només trobavem nulls a l'atribut Type 2, el que vol dir que en alguns casos no té aquest atribut i per tant, ho hem omplert amb 0. També hem realitzat l'estandarització de les dades.

### Model
| Model | Hiperparametres | Mètrica | Temps |
| Random Forest| 100 Trees amb 20% test  | 97.5% | 181ms |
| Random Forest | 1000 Trees amb 20% test | 96.87% | 1852ms |
| SVM | kernel: rbf C:10 amb 30% test| 93.33% | 1545ms|
| SVM | kernel: lineal C:10 amb 20% test| 96.25% | 144485ms |
| KNN | k=3,14 amb 20% de test | 97.25% | 11ms|
| Decission Tree | Classifier amb 30% de test | 99.16% | 3ms|
| Logístic | C=2.0 amb 30% de test| 94.16% | 23ms|


###Conclusions
Gairabé tots els models donen valors molt alts al voltant d'un 96%, això es degut a que es tracta de valors de un videojoc i per tant, amb el valor atribut de Legendari sempre hi haurà detalls que el diferencïin d'un altre normal, el que fa que la correlació inicial fos molt alta i que els valors dels diferents classificadors siguin molt propers. Tot i així trobem, els millors resultats amb KNN, random forest de 100, i sobretot, tenint en compte resultat i temps amb el decision tree, tot i això, pot ser que a mesura que es fan repeticions canviin les dades ja que son tots valors molt propers.

### Presentació
https://www.canva.com/design/DAFO2Bx0UhA/zy0exvCddbKyLWvs1XBShA/view?utm_content=DAFO2Bx0UhA&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
