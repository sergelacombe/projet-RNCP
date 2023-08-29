# projet-RNCP

Captain LOG DU 29 08 2023 :

Le dataset "UNSW-NB15" est un ensemble de données largement utilisé dans le domaine de la cybersécurité pour l'évaluation et la validation de modèles de détection d'intrusion et d'attaques réseau. Il est souvent utilisé pour l'entraînement et le test de modèles de machine learning et de deep learning visant à détecter les activités malveillantes et les tentatives d'intrusion dans les réseaux informatiques.

Le suffixe "_c" dans "UNSW-NB15_c" pourrait faire référence à une version spécifique ou à un sous-ensemble particulier de ce dataset. Cependant, sans plus de contexte ou de détails, il est difficile de fournir une explication précise.

Généralement, le dataset UNSW-NB15 contient les caractéristiques suivantes :

Caractéristiques du réseau : Il s'agit des attributs extraits du trafic réseau, tels que les adresses IP source et destination, les ports source et destination, les protocoles, les indicateurs de connexion, etc.

Étiquettes d'intrusion : Chaque enregistrement dans le dataset est étiqueté comme soit une activité normale (non intrusive) ou comme une tentative d'intrusion spécifique (par exemple, attaque par déni de service, scan de port, etc.).

Données de charge utile (payload) : Certaines versions du dataset incluent également les données de charge utile (payload) des paquets réseau, qui peuvent être utilisées pour des analyses plus approfondies.
========================================================================================================================================================================================================================================================================
Le but de ce dataset est de fournir un environnement réaliste pour tester et évaluer les performances des algorithmes de détection d'intrusion. Cela aide à développer des modèles robustes pour détecter les activités malveillantes dans les réseaux et à renforcer la sécurité des systèmes informatiques.
========================================================================================================================================================================================================================================================================
Il est important de noter que les datasets de détection d'intrusion doivent être utilisés avec prudence et éthique, car ils contiennent souvent des données potentiellement sensibles ou personnelles. Avant d'utiliser ce genre de données, assurez-vous d'obtenir les autorisations appropriées et de respecter les réglementations en matière de confidentialité des données.



Comment nous allons utiliser le dataset UNSW-NB15 dans le cadre d'une pipeline de données pour la détection d'intrusion. Voici une approche simplifiée en plusieurs étapes :

1. Collecte des données : Télécharger le dataset UNSW-NB15 à partir de la source appropriée, comme le site web de l'organisme de recherche ou la plateforme où il est disponible.(KAGGLE)

2. Exploration et Préparation des données :

Charger le dataset dans un format compatible avec  notre environnement (par exemple, CSV).
Explorer les caractéristiques et les étiquettes d'intrusion pour comprendre la structure des données.
Effectuer des opérations de nettoyage, telles que la suppression de lignes dupliquées et le traitement des valeurs manquantes.

3. Prétraitement des données :

Encoder les caractéristiques catégorielles si nécessaire.
Diviser le dataset en ensembles d'entraînement, de validation et de test.

4. Développement du Modèle :

Choisir un algorithme ou un modèle adapté à la détection d'intrusion (par exemple, Random Forest, SVM, Réseau de Neurones, etc.).
Entraîner le modèle sur l'ensemble d'entraînement en utilisant les étiquettes d'intrusion comme cible.
Utiliser l'ensemble de validation pour ajuster les hyperparamètres du modèle.

5. Évaluation du Modèle :

Évaluer les performances du modèle sur l'ensemble de test en utilisant des métriques telles que la précision, le rappel, le F1-score, etc.

Identifier les types spécifiques d'attaques que notre modèle peut détecter avec succès.

6. Déploiement :

Une fois satisfait des performances, déployer le modèle dans un environnement de production. Cela peut impliquer de convertir le modèle en un format utilisable, par exemple TensorFlow Lite pour le déploiement sur des appareils mobiles ou Docker pour le déploiement sur des serveurs.

7. Surveillance et Amélioration :

Surveiller régulièrement les performances du modèle en production pour détecter tout déclin de la qualité.
Si nécessaire, réentraînez le modèle avec de nouvelles données pour maintenir sa précision.

8. Sécurité et Confidentialité :

S'assurer que les données d'intrusion utilisées pour l'entraînement sont gérées en toute sécurité et de manière confidentielle.
S'assurer que les prédictions du modèle sont protégées et que les accès à l'API sont sécurisés.

9. Documentation :

Documenter soigneusement chaque étape de la pipeline, y compris les prétraitements, les choix de modèle, les hyperparamètres, les résultats et les améliorations.
Garder à l'esprit que cette approche est simplifiée et qu'il peut y avoir des étapes plus spécifiques ou avancées en fonction de nos besoins et de notre expertise.

==================================================================================================================================================================================================
L'objectif est de créer une pipeline qui transforme les données brutes en un modèle capable de détecter les intrusions dans les réseaux.
==================================================================================================================================================================================================
