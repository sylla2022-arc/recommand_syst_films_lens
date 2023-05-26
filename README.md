## Checklist

Cet ensemble de données (**ml-25m**) décrit l'activité de classement **5 étoiles** et de marquage en texte libre de **MovieLens** , un service de recommandation de films. Il contient **25000095 classements** et **1093360 applications** de balises sur **62423 films**. Ces données ont été créées par **162541 utilisateurs** entre le **09 janvier 1995 et le 21 novembre 2019**. Cet ensemble de données a été généré le **21 novembre 2019**.


## Description des fichiers

Les données sont contenues dans 6  fichiers: 


* **movie.csv** qui contient des infos sur les films:

    * *movieId*, *title*, *genres*


* **rating.csv** qui contient les notes des films par les utilisateurs :

   * *userId*, *movieId*,  *rating*, *timestamp*



* **genome_scores.csv**   qui contient les données de pertinence des balises :

   * *movieId*, *tagId*, *relevance*
   

* **genome_tags.csv** qui contient les descritptions des balises:

   * *tagId*,  *tag*
   
   
* **tag.csv** qui contient des balises appliquées aux films par les utilisateurs :

    * *userId*, *movieId*, *tag*, *timestamp*
    
    
    
* **link.csv**  qui contient des identifiants pouvant être utilisés pour créer des liens vers d'autres sources:

    * *movieId*, *imdbId*, *tmbdId*

## Inventaire des variables:

Les données comprenent des variables  suivantes:

* **userId**:  *ID utilisateur*

    * Les utilisateurs de MovieLens ont été sélectionnés au hasard pour être inclus. Leurs identifiants ont été anonymisés. 
    * Les ID utilisateur sont cohérents entre **ratings.csv** et **tags.csv** (*c'est-à-dire que le même ID fait référence au même utilisateur dans les deux fichiers*).


* **movieID**: *ID de film*

    * Seuls les films avec au moins une **note** ou un **tag** sont inclus dans l'ensemble de données.
    * Les identifiants de film sont cohérents entre **ratings.csv**, **tags.csv**, **movies.csv** et **links.csv** (c'est-à-dire que le même identifiant fait référence au même film dans ces quatre fichiers de données).



* **title**: *Titre des films*

    * Les titres de films sont saisis manuellement ou importés de https://www.themoviedb.org/ et incluent l'année de sortie entre parenthèses. 
    * Des erreurs et des incohérences peuvent exister dans ces titres.


* **genres**: *Genre des films* : Les genres sont une liste séparée par des tubes (|) et sont sélectionnés parmi les suivants :

    * Action
    * Adventure
    * Animation
    * Children's
    * Comedy
    * Crime
    * Documentary
    * Drama
    * Fantasy
    * Film-Noir
    * Horror
    * Musical
    * Mystery
    * Romance
    * Sci-Fi
    * Thriller
    * War
    * Western
    * (no genres listed)


* **ratings**: *Les notes*
     * Les notes sont faites sur une échelle de 5 étoiles, avec des incréments d'une demi-étoile (0,5 étoiles - 5,0 étoiles).
     * Cela évalue la satisfaction de l'utilisateur.



* **timestamps** : *Horodatage*

 * Les horodatages représentent les secondes depuis minuit Temps universel coordonné (UTC) du 1er janvier 1970.
 * Le nombre de secondes écoulées depuis l'avis laissé par l'utilisateur.


* **genom**: *Génome (score and tags)*
    * Le génome des balises code la force avec laquelle les films présentent des propriétés particulières représentées par des balises (atmosphériques, stimulantes, réalistes, etc.). 
    * Le génome des balises a été calculé à l'aide d'un algorithme d'apprentissage automatique sur le contenu fourni par les utilisateurs, y compris les balises, les évaluations et les critiques textuelles.
    
    
* **relevance** Données de pertinence de balise de film



* **tagId**: Les tagId valeurs sont générées lorsque l'ensemble de données est exporté, elles peuvent donc varier d'une version à l'autre des ensembles de données MovieLens.

**A savoir plus** : **Jesse Vig, Shilad Sen et John Riedl. 2012** . Le génome de balise : codage des connaissances communautaires pour soutenir une nouvelle interaction. ACM Trans. Interagir. Renseignement. Syst. 2, 3 : 13 : 1–13 : 44. https://doi.org/10.1145/2362394.2362395

## Objectif

Notre objectif :
 
**1.** **_Nettoyage des données_**

**2.** **_Exploration_**

**3.** **_Construction de système de recommandation_**


## Description des données

Lien vers les données: https://grouplens.org/datasets/movielens/


## References : 

**F. Maxwell Harper and Joseph A. Konstan**. 2015. The MovieLens Datasets: History and Context. ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. <https://doi.org/10.1145/2827872>