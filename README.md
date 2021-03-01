# Sentiment Analysis

## Intérêt 

Ici, un travail exploratoire de NLP(Natural language processing) sur des tweets. Ainsi le but est d'explorer les manières de faire du NLP et d'apprendre à récupérer les données twitter qui nous intéresse.
Les applications de ces sujets sont multiples:
* pour le  NLP:  
  * en publicité, en ciblant des personnes que l'on aurait détectées comme possiblement intéressé
  * En étude de marché pour trouver les nouveaux besoins
  * Analyse de retour sur un produit ou d'avis sur un sujet
  * En amélioration de la productivité:
    * tri automatique de mail    
    * Détection d'informations pertinentes par rapport à une recherche
    * traduction
    * correction d'orthographe et grammaire
* Et pour la récupération de donné twitter:  
  * 86 millions dutilisateurs quotidiens  
  * 6000 tweets /seconde  
  * Sujet varié, art, politique, humour, tranche de vie, ...  
  * recherche facile sur un sujet grace aux hashtags  
  * texte lié à un auteur et lui lié à d'autre auteurs et d'autre textes, cela contextualise la donnée.

## Contexte, données et outils
Pour le NLP nous utilisons principalement des bibliothèques classiques:

* Nltk ( https://www.nltk.org/ )

* Scikit-learn ( https://scikit-learn.org/stable/)

* Keras ( https://keras.io/api/)

* TensorFlow ( https://www.tensorflow.org/)

Enfin pour la récupération de données:

* Tweepy ( https://www.tweepy.org)

Pour l'entrainement des diferent modele, les données que j'utilise sont un dataset inclu dans NLTK. Scikit-learn est principalement utilisé pour les classifieur. ET Keras et Tensor-Flow pour les reduction de dimension.

Pour les données que j'ai récupérées grace à tweepy :
* adidasdatset.csv(34 Mo) https://drive.google.com/file/d/191R5v3XUJKb6T2QUe2HMlbn4NQj2fSpE/view?usp=sharing
* onedirdataset.csv(548 Mo) https://drive.google.com/file/d/1pjeG4DZgJBTYdq5Te-l_uGMskrUav4Pw/view?usp=sharing

Et les models que j'ai entraînés:
* reduc_cencoder.h5(59 Mo) https://drive.google.com/file/d/10CmwbPab8EKCVrwDJkev8-fFjYP0CyGU/view?usp=sharing
* reduc_part0.h5(91 Mo) https://drive.google.com/file/d/1KSO7wYycWiEkgy-2rfwGWAOIlUFh7xwy/view?usp=sharing
* qui vont de paire avec les deux fichiers texte du github, ce sont les liste des mots utilisé par ces models.

De plus, si vous voulez relancer le code ne pas hésiter à utiliser collab ( https:/colab.research.google.com) mais certains models sont lourds (40 min d'entraînement sur colab).

## le contenu du github

Ce github prend la forme d'un tutoriel pour effectuer une analyse de sentiment sur des tweet. Il est destiné aux personnes ayant un bagage généraliste sur l'apprentissage automatique et voulant se renseigner sur le NLP et explique comment récupérer des données twitter.
Ainsi les notebooks abordent chacun un sous-sujet et sont organisés de la manière suivante: 

* En premier lieu dataset.Ipynb qui explique comment nous formons le dataset pour l'apprentissage de nos modèles.  

* Puis Analyse_de_sentiment.ipynb où nous faisons une première approche sur l'analyse de sentiment.  

* reduction.ipynb nous approfondissons le précédent grace à la réduction de dimension.  

* Enfin recuperation_tweet.ipynb dans lequel nous abordons la récupération des données twitter. 

## Pour conclure

Bien sûr il y a encore d'autres manière de faire de l'analyse de sentiment, utiliser des n-gramme au lieu d'unigramme, réduire la dimension grace à des CBOW ou bien des skips Gram et aussi je n'ai pas été exhaustif dans l'ensemble des classifieurs possibles. Le NLP ne concerne pas que le sujet de l'analyse de sentiment, néanmoins le formatage des données, la réduction de dimension abordée ici et les type classifieur utilisé est assez classique et couramment utilisé.

Enfin en ce qui concerne l'extraction de données twitter, tweepy n'est pas le seul wrapper et ce qu'il y a est une utilisation classique. Comme dit au début de ce readme, on peut récupérer beaucoup de contexte, et ainsi le NLP n'est pas la seule utilisation. Par exemple en récupérant la liste des followers, nous pouvons reformer le réseau autour d'un utilisateur ou d'une communauté, en déduire qui sont les ponts entre chaque communauté, si certains groupes sont isolés, predire les inclinaison  du groupe et ou de la personne pour lui sugerer des contenus en adequation, ...

