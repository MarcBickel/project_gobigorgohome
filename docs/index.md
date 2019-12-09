---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
bigimg: /img/indexbg.jpg
---
# Tests
<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://marcbickel.github.io/project_gobigorgohome/boxplot_nutrition_grade.html" height="525" width="100%"></iframe>
## Abstract
"Nowadays, there exists a myriad of products, examples of an ever-growing consumption regime. Furthermore, the convenience of accessing such items is only a few clicks away for most of us. In this project, we will ground our reasoning on the consumer's point of view in todays world. Our starting point will be the Open food facts dataset, from which we will extract data on several different food products. Do the values that people hold dear stand up to the comparison with the food they actually buy ? Is the most sought after type of food really the one that should top such a ranking ? Are those products the ones that impact the most consumer health and are they the most environmentally-friendly ? We will try to answer these questions by coming up with a ranking containing top products regarding : consumer diet, travel from production site, carbon footprint, nutritional index, etc. These rankings will then be compared to the products bought online by consumers with the Instacart dataset, most noticeably with the popularity of particular items. We will then be able to create personalized recommendations for the consumers. They will highlight good shopping practices and the best-in-category products."

### Research questions

- What are the worst/best ranking products according to nutritional index ?
- Possible to identify specific diets ?
- How do these rankings compare to the products the users buy ?
- Can we create recommendations for users based on that data ?


> "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

### With footnotes too!

Back up your stuff with solid, clean citations. Footnotes can be written in markdown and appear like this.[^1] Use as many as you like.[^2]

## Milestone 2 feedback + auto-critic 

Notebook : project_notebook.ipynb

Following additionnal analysis of the data we have, we decided on dropping the Carbon Footprint aspect of the project. Very few items actually have that information, and our analysis would have been impossible to realise. Our aspect of "Data for good" will therefore be switched from: "suggest food items to reduce that carbon footprint" to: "suggest food items that are better for your health". We will do so be focusing on the nutritional grade of the food. Once we have extracted that information, we can also try to see if it is correlated to suger levels in the food, or other meaningful correlations.

## Datasets

- Open food facts database : We will use it to make statistics on different informations given about the food products (amongst others the nutritional index. Afterwards, we will combine different criteria in order to come up with food rankings giving for example the healthiest food for selected diets. 
- Instacart : In a second time, we will use the instacart database to find out which types of food are bought the most by the customers. We will then use this information to find out how well the most sought after products do in the rankings we established before. Also, if we find food that is similar to the ones users bought, but higher up in our rankings, we will be recommending that new food item to new. 

### Data cleaning

We started with the Open food facts database , where we removed the rows that have more than half of the data missing. These will introduce more problems than what they can actually contribute. 
Standard outliers and NaN removal has also been applied. 
We also remove columns that are mostly empty (  >850k rows have the corresponding value missing). We now have a size-reduced dataset, but the quantity of information itself did not get reduced very much. 

Concerning the instacart dataset, we created a product-centric dataframe, where each product is represented by a row. This view serves us much better than the previous one. We then only consider the 5% most popular products, to be able to reduce the size of the dataset. 

### Data augmentation

- ways to enrich, filter, transform the data according to your needs ?

Nutritionnal score and grade convey the same information, and the score offers more data and nuances. 

For relations and analysis between nutritionnal grade and differents food facts, please open the Notebook. 

#### Double dataset linking

We created a dictionnary of the most frequent words in each nutritionnal grade category (after some translation, to be able to use products regardless of origin/language). Some results are easily predictable, like "bio" being the most used word in grade A, and "chocolate" being its counterpart in grade E. Again, more info in the notebook. 
We then compute a similiraty score for each product, based on word occurences. This allows us to assign a grade to instacart items. 

### Data analysis

We started by looking at the relation between the grade we assigned to instacart products and the department of said product (examples are 'frozen', 'bakery', 'canned foods', amongst others). 
The results seem to match with common sense, such as alcohol being bad for the consumer's health. Our link between the two datasets seems to work. 
We will add other statistics to our analysis in the Milestone 3. 

## Data pipeline

- Sort data into different nutritionnal score
- Notice significant differences between different nutritionnal grades
- Focus on food with grade E (the worst)
    - Are the sugar levels related to the grade attribution ?
    - Is there a way to avoid foods that are in this category ? 
    
- Link the two databases together
    - Is there a general tendency discernable amongst orders ? Is it possible to extract buyer's profiles to be able to see if they hover aroung grade A good or are biaised towards grade E food ? 
    - Pinpoint specific diets
    - Recommendation system, where similar foods are bagged together, and the best nutritionnal score amongst them is then recommended to the user. 
- Establish food ranking, base on nutritionnal score, and other additionnal criteria if needed

## Questions for TAs


<img src="images/hello.svg" alt="sample image">



<hr>

##### Footnotes:

[^1]: This is a footnote. Click to return.

[^2]: Here is another.
