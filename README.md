# AdA Project: Team go Big or go Home

# Title : Where do your purchases rank in our analysis ?

# Abstract

Nowadays, there exists a myriad of products, examples of an ever-growing consumption regime. Furthermore, the convenience of accessing such items is only a few clicks away for most of us. In this project, we will ground our reasoning on the consumer's point of view in todays world. Our starting point will be the Open food facts dataset, from which we will extract data on several different food products. Do the values that people hold dear stand up to the comparison with the food they actually buy ? Is the most sought after type of food really the one that should top such a ranking ? Are those products the ones that impact the most consumer health and are they the most environmentally-friendly ? We will try to answer these questions by coming up with a ranking containing top products regarding : consumer diet, travel from production site, carbon footprint, nutritional index, etc. These rankings will then be compared to the products bought online by consumers with the Instacart dataset, most noticeably with the popularity of particular items. We will then be able to create personalized recommendations for the consumers. They will highlight good shopping practices and the best-in-category products. 

# Research questions

- What are the worst/best ranking products according to carbon footprint ? 
- What are the worst/best ranking products according to nutritional index ?
- Combination of these criteria, correlation between them ?
- Possible to identify specific diets ?
- How do these rankings compare to the products the users buy ?
- Can we create recommendations for users based on that data ?
- New carbon footprint index based on how popular the product is

# Dataset

- Open food facts database : We will use it to make statistics on different informations given about the food products (amongst others the nutritional index and the carbon footprint). Afterwards, we will combine different criteria in order to come up with food rankings giving for example the healthiest food for selected diets or ecological values. 
- Instacart : In a second time, we will use the instacart database to find out which types of food are bought the most by the customers. We will then use this information to find out how well the most sought after products do in the rankings we established before. 

# A list of internal milestones up until project milestone 2

- Import and clean the data
- Sort the data and extract the products we will work with
- Do aggregation and statistics 
- Explain our reasoning, comment and write the notebook

# Questions for TAa
-Do you have any recommendations on how to link the two datasets ?
-What are the possible biases in our methodology ?



# Milestone 2

Enlver les rows qui ont plus de la moitié des infos manquantes dans openfoodfacts

Se concentrer sur le nutirotional grade E
Faire analyse du sucre machin sur openfoodfacts



## ce qu'on a changé yo

- Show that we can handle the data in its size ?
- Expliquer un peu plus la data
- ways to enrich, filter, transform the data according to your needs ?
- That you have updated your plan in a reasonable way, reflecting your improved knowledge after data acquaintance. In particular, discuss how your data suits your project needs and discuss the methods you’re going to use, giving their essential mathematical details in the notebook.
abandonné le carbon footprint car suelement 1000 rows avaient cette données sur 1000000000000000
    Grâce aux conseils du maginfique TA aussi 

## NEW PIPELINE
trier selon nutriitional score 
    voir les différences entre les diffrents grades
    d'abord se concenter sur les alimetns avec grade E 
    lier la shit à l'instacart (commandes avec grade plutôt haut ou plutôt bas, erst-ce qu'on arrive à dégager des profils types d'acheteurs)
    faire un ranking
