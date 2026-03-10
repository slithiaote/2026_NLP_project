# Objectifs du projet

Evaluer/comparer la performance de modéles de NER
Pour évaluer la performance d'un modèle de NER, il faut pouvoir quantifier les exemples positifs et négatifs.
pour des entités présentes : sont-elles retrouvées par le modèle ?
pour des entités absentes / les autres entités : sont-elles bien absentes ?

La difficulté est d'avoir un jeu d'entraînement : il faut annoter l'ensemble du texte pour indiquer quels mots font partie d'une entité.

Ici, on propose d'utiliser les annotations fournies (nom / prénom du titulaire, nom/prénom du suppléant) comme jeu de test. La métrique est alors : pour les documents dans lesquels le nom est indiqué, est-ce que le modèle reconnait l'entité.
Comme il s'agit d'ocr, il peut y avoir des erreurs

Note : un modèle a intérêt à tout déclarer comme entité. On controle en imposant que l'entité doit être un nom de personne.
Note : il faut des personnes "non connues" ?

# Outputs

Déterminer les entités présentes dans la profession de foi : nom / prénom du titulaire, nom/prénom du suppléant
Déterminer les segments du texte où ils apparaissent.

Calculer la probabilité de retrouver ces entités.
pour spacy et BERT
controler par le fait que les entités doivent être des personnes

Bonus : est-ce que l'on reconnaît plus facilement certaines entités? par exemple métropole outremer ? gauche / droite ?


# Consignes

Define a problem on the corpus requiring the use of NLP techniques.
Retrieve, format and describe the data statistically
Search the literature on the chosen problem and write a short state-of-the-art
Propose and justify of the choice of the model(s)
Experiment with the proposed model
Write an analysis of the results and a conclusion


Style analysis ⭐
Gender Classification: Is there a “feminine” or “masculine” rhetoric within the manifestos?
Political affiliation detection :
predict the titulaire-soutien (support) or liste (party list)
analyze confusion matrices to identify which parties “speak the same language”
compute the semantic similarity of the documents and display them in 2D with their political support or party list. Identify outliers.
Metadata extraction ⭐
Train a Named-entity extraction model using the metadata file.
Evaluate on the Archelec corpus
Evaluate on the more recent corpus https://github.com/regardscitoyens/professions-foi-candidats/tree/master
Sponsorship and personality extraction: Use NER to extract the names of national leaders mentioned (“De Gaulle” “Mitterrand”). Who cites whom? Does a local candidate prefer to link themselves to a national figure or distance themselves?
Spatial analysis: extract mentioned locations to determine if the discourse is purely rooted locally or if it projects toward national/international stakes.

