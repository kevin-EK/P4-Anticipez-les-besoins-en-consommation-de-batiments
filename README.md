# Anticipez les besoins en consommation de batiments

## I. Contexte
  - Pour atteindre son objectif de ville neutre en émissions de carbone en 2050, la ville de Seattle s’intéresse de près à la consommation et aux émissions des bâtiments non destinés à l’habitation.
  
  - Des relevés minutieux ont été effectués par les agents de la ville en 2016.
  
  - Cependant, ces relevés sont coûteux à obtenir, et à partir de ceux déjà réalisés, nous souhaitons prédire :
    - les émissions de CO2 
    - la consommation totale d’énergie

## II. Problématique
Les prédiction doivent se baser sur les données structurelles des bâtiments  tel que:
  - La taille,
  - L’usage des bâtiments, 
  - La date de construction, 
  - La situation géographique, etc…

De plus nous devons également évaluer l’intérêt de l’  « ENERGY STAR Score » pour la prédiction d’émissions, qui est fastidieux à calculer avec l’approche actuel. 

Enfin seul les **bâtiments non destinés à l’habitation** nous intéressent. 

## III. Explaratory Data Analysis
![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/ba4790ac-0d60-4d4b-9527-48ae0012a5c9)

## IV. Modélisation et prédiction

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/feeef8c0-863a-45bc-8bbf-8a342670c666)

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/f0d195f8-5bdc-47e5-8ba1-cdabf393fad4)

### Encodage

L'encodage des données consiste à convertir des informations d'un format telles que le texte en un format numérique compréhensible par les ordinateurs. Cela implique souvent la représentation des données sous forme de bits, qui sont des 0 et des 1, afin de les traiter, les stocker et les manipuler efficacement.

Label Encoding :
  - consiste à attribuer un numéro unique à chaque catégorie dans une variable catégorique.
  - est utilisé lorsque les catégories ont une relation ordonnée ou hiérarchique.
Exemple : Si une variable catégorique "Couleur" a les catégories "Rouge", "Vert" et "Bleu", le label encoding attribuera les valeurs 0, 1 et 2 respectivement.
One-Hot Encoding :

Le one-hot encoding :
  - consiste à créer une nouvelle colonne pour chaque catégorie, et chaque colonne contient des valeurs binaires (0 ou 1) pour indiquer la présence ou l'absence de cette catégorie.
  - est utilisé lorsque les catégories ne présentent pas de relation ordonnée, et chaque catégorie est indépendante des autres.
Exemple : Pour la même variable catégorique "Couleur", le one-hot encoding créerait trois nouvelles colonnes : "Rouge", "Vert" et "Bleu", où chaque ligne aurait une seule valeur 1 pour indiquer la couleur correspondante et des valeurs 0 pour les autres.
En résumé, le label encoding est adapté aux variables catégoriques ordonnées, tandis que le one-hot encoding est utilisé pour les variables catégoriques non ordonnées et lorsque les catégories sont indépendantes les unes des autres.

### Scaling

Étant donné que la normalisation et la standardisation peuvent toutes deux être faussées par des valeurs aberrantes à travers la moyenne, l'écart-type, les valeurs min et max, j’utilise standardisation robuste RobustScaler.
 La normalisation robuste met à l'échelle les valeurs en utilisant la médiane et l'écart interquartile, et n'est donc pas influencée par quelques valeurs grandes ou petites. De cette façon, les valeurs extrêmes ne sont pas prises en compte dans la transformation.

 ![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/3012e888-a90b-42f2-8ac1-f1d2d6de72f0)

### Métrique d'évalution

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/6f06710b-5b70-4bf7-b364-037dcf55475e)

### Validation Croisée Imbriquée
![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/7cf8ea85-727d-428f-a3a3-12dfe2b05195)

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/724e1961-aa86-4c72-b0ef-bee8ad0a09b4)

### Comparaison des modèles
![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/6332f99e-2664-4c70-bc0b-5048cdf40c2f)

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/647e82ef-2737-45d5-8eb2-d66619ad7e85)

![image](https://github.com/kevin-EK/P4-Anticipez-les-besoins-en-consommation-de-batiments/assets/69479292/b5a4a24b-c5c4-4752-b883-9464d2d237a9)


