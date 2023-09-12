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


Contient des fichiers d'analyse de données exploratoires, des modèles de détection d'intrusion réseau et de classification des attaques pour le problème décrit ci-dessous -

La détection des intrusions sur le réseau et la catégorisation des attaques sont un domaine de recherche actif, mais l'un des problèmes majeurs auxquels sont confrontés les chercheurs est l'indisponibilité d'ensembles de données simulant le trafic réseau moderne. Il existe plusieurs autres ensembles de données disponibles, tels que KD98, KDDCUP99 ( KDD Cup 1999 Data ) qui ont été générés dans le but de développer des systèmes de détection d'intrusion réseau capables de détecter la différence entre les « mauvaises » intrusions réseau et les « bonnes » connexions réseau, mais ces ensembles de données ont été générés il y a environ 20 ans et ne représentent pas de manière adéquate le trafic réseau généré par les ordinateurs modernes.

L'ensemble de données UNSW-NB15 a été créé dans le but de combler cette lacune.

L'ensemble de données contient 9 types d'attaques, à savoir Fuzzers, Analysis, Backdoors, DoS, Exploits, Generic, Reconnaissance, Shellcode et Worms.

Dans les fichiers ipynb, une EDA détaillée est effectuée ainsi que les performances de conception et d'analyse de divers modèles de détection d'intrusion réseau et de classification des attaques.
=========================================================================================================================================
En préambule, nous avons scrappé un site de cybersecurité, afin de pouvoir faire une analyse descriptive de l etat des attaques et surtout une donnée manquante : les couts en dollars.
Apres la concatenation des fichiers csv dans knime nous avons obtnu e un fichier csv qui nous a permis de progresser avec un collab pour pour explorer et preparer un machine learning KNN (classification binaire) qui s'impose compte tenu de la nature du dataset si ce modele ne fonctionne ne fonctionne nous allons utiler l'alghromithe DBSCAM (classification mutiple avec 10 classe dont la derniere sera "pas d'attaques') et enfin nous allons deployer l interface de reconnaissance d'intrusion dans streamlit.
