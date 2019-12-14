---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
bigimg: /img/indexbg.jpg
---
# Do you buy healthy ?
Go big or go home narrative

## Data Story
### Abstract
Nowadays, there exists a myriad of products, examples of an ever-growing consumption regime. Furthermore, the convenience of accessing such items is only a few clicks away for most of us. In this project, we will ground our reasoning on the consumer's point of view in todays world. Our starting point will be the Open food facts dataset, from which we will extract data on several different food products. Do the values that people hold dear stand up to the comparison with the food they actually buy ? Is the most sought after type of food really the one that should top such a ranking ? Are those products the ones that impact the most consumer health and are they the most environmentally-friendly ? We will try to answer these questions by coming up with a ranking containing top products regarding : consumer diet, travel from production site, carbon footprint, nutritional index, etc. These rankings will then be compared to the products bought online by consumers with the Instacart dataset, most noticeably with the popularity of particular items. We will then be able to create personalized recommendations for the consumers. They will highlight good shopping practices and the best-in-category products. 

### Yolo

Every food has intrisic nutritive and health attributes. Our body needs some nutrients and vitamins in order to functin properly, and and failing to meet its demands can result in bad life hygiene or even disease. Some people pay very close attention to such properties of the products they buy, and they can enjoy their body operating at its full potential. Others however, buy ingredients thinking nutrition is not a primordial argument in the choice they make. These are the people we are going to help. 

First, the Open Food Facts database allows us to get data about every possible type of food, and we primarily focus on the nutrional index and nutritional score. This data represents a condensed form of the health impact that particular food has on the human body. Namely, A represents very healthy food, such as vegetables, and E is what we should avoid eating, such as chocolate. Of course, this is often the food we crave the most. The index allows for a fine-grained score. 

### Présentation des datasets
description des datasets, avec quelque stats dessus

#### Openfoodfacts
We will use it to make statistics on different informations given about the food products (amongst others the nutritional index. Afterwards, we will combine different criteria in order to come up with food rankings giving for example the healthiest food for selected diets. 

#### Instacart
In a second time, we will use the instacart database to find out which types of food are bought the most by the customers. We will then use this information to find out how well the most sought after products do in the rankings we established before. Also, if we find food that is similar to the ones users bought, but higher up in our rankings, we will be recommending that new food item to new. 

We started with the Open food facts database , where we removed the rows that have more than half of the data missing. These will introduce more problems than what they can actually contribute. 
Standard outliers and NaN removal has also been applied. 
We also remove columns that are mostly empty (  >850k rows have the corresponding value missing). We now have a size-reduced dataset, but the quantity of information itself did not get reduced very much. 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://marcbickel.github.io/project_gobigorgohome/html/850k-filter.html" height="525px" width="100%"></iframe>

Concerning the instacart dataset, we created a product-centric dataframe, where each product is represented by a row. This view serves us much better than the previous one. We then only consider the 5% most popular products, to be able to reduce the size of the dataset. 
On se concentre sur les produits qui forment 95% des commandes, en tout environ 3000 produits. 

### différents food grades
avec différences entre les food grades
word clouds


### Linker les deux datasets

We created a dictionnary of the most frequent words in each nutritionnal grade category (after some translation, to be able to use products regardless of origin/language). Some results are easily predictable, like "bio" being the most used word in grade A, and "chocolate" being its counterpart in grade E. Again, more info in the notebook. 
We then compute a similiraty score for each product, based on word occurences. This allows us to assign a grade to instacart items. 

graphiquement représenter des dictionnaires ?
Is there a general tendency discernable amongst orders ? Is it possible to extract buyer's profiles to be able to see if they hover aroung grade A good or are biaised towards grade E food ? 

formule mathématique pour lier les deux datasets et faire notre ranking

bubble plot pour nombre de mots par langue

### food rankings ? 
like the best food, based on nutritionnal score, and other additionnal criteria if needed
examples de food qu'il est possible de remplacer par d'autres foods et monter en grade avec ce remplacement
top 5 dans cahque catégorie nutritionnelle avec nombres d'achats pour pouvoir répondre à la question Do you buy healthy
### FIndings
est-ce qu'on a genre des facts/résultats à montrer à la fin ?
Des fun facts ?

### To go further
Instacart ça a quelle base d'utilisateurs ?
Ceux qui commandent la bouffe pour qu'elle soit livrée, ils ont assez de tune pour faire gaffe à manger sain ?

### boxplots
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://marcbickel.github.io/project_gobigorgohome/html/html_boxplot_carbohydrates_100g.html" height="525px" width="100%"></iframe>


<img src="img/wordcloud.png">
