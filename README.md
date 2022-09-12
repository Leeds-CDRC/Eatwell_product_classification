# Eatwell Classification Tool

## Version 1.0


This version of the Eatwell classification tool takes product information e.g. (product name, description, shelving categories) and uses the developed text matching algorithms to assign the food product to a segment of the Eatwell Guide. To reflect real-world baskets in addition to the five standard segments defined in the Eatwell guide products can also be classified as an alcoholic beverage, non-alcoholic beverage, discretionary food, composite food, baby/toddler foods, other (e.g. spices and flavouring) or non-food items (i.e. items that may be purchased alongside food items such as kitchen foil, tooth paste etc.). The full category descriptions, logic behind their inclusion and examples are given in table 1. 


|Category |Detail |Example(s)|
|---------|-------|--------|
|Fruit and Vegetables |**Eatwell food category**, recommended to be 39% of food consumed (by weight) | Carrots, Apple, Kiwi, Salad |
|Potatoes, bread, rice, pasta and other starchy carbohydrates |**Eatwell food category**, recommended to be 37% of food consumed (by weight) | Wholegrains, Porridge, Cous cous, Cereals |
|Beans, pulses, fish, eggs, meat and other proteins|**Eatwell food category**, recommended to be 12% of food consumed (by weight) | Lentils, Chickpeas, Meat, Fish, Eggs|
|Dairy and alternatives|**Eatwell food category**, recommended to be 8% of food consumed (by weight) |Milk, Cheese, Soya milk |
|Oils and spreads|**Eatwell food category**, recommended to be 1% of food consumed (by weight) |Olive oil, Sunflower spread |
|Discretionary Foods |Corresponds to those foods that should be eaten less often and in small amounts (Remaining 3% of foods consumed by weight) |Cakes, Crisps, Biscuits, Chips,| 
|Alcoholic Beverages | Alcoholic drinks (not included in Eatwell guidance)|Wines, Beers, Spirits |
|Non-alcoholic Beverages | Non-alcoholic drinks (not included in Eatwell guidance)- user discretion to include as discretionary where appropriate |Squash, Cordial, Juice, Fizzy drinks|
|Composite foods| Foods that are made up of more than one food group[^1] |Ready meals, Lasagne, Quiche |
|Toddler and baby food | Toddlers and babbies have differenet diary recommendaitons to the Eatwell Guide therfore are sperated out for ease|Formula, baby purees |
|Other foods|Food items without a significant nutrtional contribution i.e. flavourings, herbs, spices, |Dried herbs and spices, pepper, salt |
|Non-food items |Products potentially errouniously included as they are typically purchased alongside a food shop| Kitchen foil, Toothpaste, Homeware|

## How the Algorithm works 

 
The text mining algorithm uses an iteratively developed lexicon to assign the product of interest to one of the extended Eatwell categories outlined in table 1. The algorithm first matches to N number of categories and then uses rules based on expert domain knowledge to assign the final category. Matching justifications are provided and are modifiable by the user for transparency.  
 
  E.g. “Eton Mess: Strawberries and Meringue” would match to two categories: Fruit and Vegetables and Discretionary, however as one of the rules is that any product with a Discretionary element is classified as such, therefore the final Eatwell Category assigned would be discretionary.  
 
  E.g. “Garden Salad: Lettuce, Tomato, Cucumber” would match four times to the Fruit and Vegetable Eatwell Category so would be assigned to that category and an indication of high probability of correct classification given.  





##




## Upcoming .. version (2.0)
Classification of food products based on product name and description to Eatwell categories 
