Projet : Prédiction des Prix de Voitures avec un Réseau de Neurones

Introduction

Ce projet consiste à prédire les prix des voitures à partir de diverses caractéristiques telles que le kilométrage, la marque, le modèle, le type de carburant, et bien plus encore. Pour ce faire, nous avons utilisé un réseau de neurones artificiels avancé afin de modéliser la relation complexe entre ces caractéristiques et le prix des voitures. Le but de ce projet est de créer un modèle prédictif précis, capable de généraliser correctement sur de nouvelles données.

Structure du Projet

Préparation des Données :

Chargement des Données : Nous avons travaillé avec un dataset contenant les caractéristiques des voitures, telles que le kilométrage, la marque, le modèle, le type de carburant, la transmission, le type d'offre, la puissance et l'année de production.

Prétraitement : Le prétraitement comprenait l'imputation des valeurs manquantes (utilisation de la moyenne pour les caractéristiques numériques et de la valeur la plus fréquente pour les caractéristiques catégorielles), la normalisation des variables numériques, et l'encodage des variables catégorielles.

Division des Données : Les données ont été divisées en ensembles d'entraînement et de test dans un rapport de 80/20.

Construction du Modèle de Réseau de Neurones :

Nous avons construit un réseau de neurones profond en utilisant TensorFlow et Keras. Le modèle comporte plusieurs couches cachées comprenant des couches Dense, des couches de BatchNormalization, et des couches de Dropout pour réduire le surapprentissage.

Le modèle utilise des fonctions d'activation ReLU et Leaky ReLU pour permettre une meilleure propagation des gradients et capturer les relations non linéaires dans les données.

Une régularisation L2 a été ajoutée à chaque couche dense pour pénaliser les poids trop importants et encourager une meilleure généralisation.

Compilation et Entraînement du Modèle :

Le modèle a été compilé avec une perte de Mean Squared Error (MSE) et optimisé avec l'algorithme Adam (taux d'apprentissage initial étant de 0,00005).

Nous avons utilisé des callbacks tels que EarlyStopping et ReduceLROnPlateau pour optimiser le processus d'entraînement et éviter le surapprentissage.

Le modèle a été entraîné sur 150 époques avec un batch size de 32, tout en surveillant la perte de validation.

Résultats et Analyse

Les résultats obtenus montrent que le modèle est capable de prédire les prix des voitures avec une grande précision, comme l'indiquent les courbes d'entraînement et de validation :

Perte (Loss) : La perte d'entraînement et de validation a diminué de manière rapide au début puis s'est stabilisée à une valeur proche de zéro. Cela montre que le modèle a appris de manière efficace à modéliser les relations entre les caractéristiques et le prix.

Erreur Absolue Moyenne (MAE) : La MAE a rapidement chuté à une valeur proche de zéro, ce qui signifie que l'erreur moyenne sur les prédictions de prix est très faible, aussi bien pour l'ensemble d'entraînement que pour l'ensemble de validation.

Les courbes d'entraînement et de validation sont très proches, ce qui indique une bonne généralisation du modèle. Le modèle ne présente pas de signes de surapprentissage, grâce à l'utilisation efficace de techniques de régularisation et de Dropout.

Visualisation des Résultats

Les graphes de l'évolution de la perte et du MAE montrent une convergence stable des deux métriques. Les courbes d'entraînement et de validation étant similaires et étant proches de zéro montrent que le modèle est très performant et n'a pas de problèmes significatifs de surapprentissage.

Conclusion

Ce projet a réussi à construire un modèle de réseau de neurones capable de prédire les prix des voitures avec une précision très élevée. Le modèle montre une bonne généralisation et une très faible erreur prédictive. Cela suggère que les méthodes utilisées, telles que la régularisation, la normalisation et l'utilisation de Dropout, ont été très efficaces pour obtenir un résultat robuste et précis.

Points à Améliorer

Validation Croisée : Pour une meilleure robustesse, il serait intéressant de mettre en place une validation croisée pour vérifier la stabilité des résultats sur différentes parties du dataset.

Test sur Données Réelles : Pour confirmer la performance du modèle en dehors de l'ensemble de validation, il est recommandé de tester sur un ensemble de données réelles jamais vues auparavant.


Technologies Utilisées

Python pour la programmation.

Pandas et NumPy pour la manipulation des données.

Scikit-Learn pour le prétraitement des données.

TensorFlow/Keras pour la construction et l'entraînement du réseau de neurones.

Matplotlib pour la visualisation des résultats.

