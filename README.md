# Eatwell Classification Tool

[![DOI](https://zenodo.org/badge/516698036.svg)](https://zenodo.org/badge/latestdoi/516698036)
## Overview:
This tool classifies food items to food group segments of the UK’s EatWell Guide  ![Eatwell Guide](https://github.com/Leeds-CDRC/Eatwell_product_classification/blob/main/Eatwell_guide_colour.pdf)(https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/528193/Eatwell_guide_colour.pdf). It is designed to aid automated food group classification for big data sources, such as grocery retailer transaction records.

## Version 1.0


This version of the Eatwell classification tool takes product information e.g. (product name, description, shelving categories) and uses the developed text matching algorithms to assign the food product to a segment of the Eatwell Guide. To reflect real-world baskets in addition to the five standard segments defined in the Eatwell guide products can also be classified as an alcoholic beverage, non-alcoholic beverage, discretionary food, composite food, baby/toddler foods, other (e.g. spices and flavouring) or non-food items (i.e. items that may be purchased alongside food items such as kitchen foil, tooth paste etc.). The full category descriptions, logic behind their inclusion and examples are given in Table 1. 


|Category |Detail |Example(s)|
|---------|-------|--------|
|Fruit and Vegetables |[**Eatwell food category**](https://www.gov.uk/government/publications/the-eatwell-guide), recommended to be 39% of food consumed (by weight) | Carrots, Apple, Kiwi, Salad |
|Potatoes, bread, rice, pasta and other starchy carbohydrates |[**Eatwell food category**](https://www.gov.uk/government/publications/the-eatwell-guide), recommended to be 37% of food consumed (by weight) | Wholegrains, Porridge, Cous cous, Cereals |
|Beans, pulses, fish, eggs, meat and other proteins|[**Eatwell food category**](https://www.gov.uk/government/publications/the-eatwell-guide), recommended to be 12% of food consumed (by weight) | Lentils, Chickpeas, Meat, Fish, Eggs|
|Dairy and alternatives|[**Eatwell food category**](https://www.gov.uk/government/publications/the-eatwell-guide), recommended to be 8% of food consumed (by weight) |Milk, Cheese, Soya milk |
|Oils and spreads|[**Eatwell food category**](https://www.gov.uk/government/publications/the-eatwell-guide), recommended to be 1% of food consumed (by weight) |Olive oil, Sunflower spread |
|Discretionary Foods |Corresponds to those foods that should be eaten less often and in small amounts (Remaining 3% of foods consumed by weight) |Cakes, Crisps, Biscuits, Chips,| 
|Alcoholic Beverages | Alcoholic drinks (not included in Eatwell guidance)|Wines, Beers, Spirits |
|Non-alcoholic Beverages | Non-alcoholic drinks (not included in Eatwell guidance)- user discretion to include as discretionary where appropriate |Squash, Cordial, Juice, Fizzy drinks|
|Composite foods| Foods that are made up of foods in more than one category[^1] |Ready meals, Lasagne, Quiche |
|Toddler and baby food | Toddlers and babies have different diary recommendations to the Eatwell Guide therefore are separated out for ease |Formula, baby purees | 
|Other foods |Food items without a significant nutritional contribution i.e. flavorings, herbs, spices, |Dried herbs and spices, pepper, salt | 
|Non-food items |Products potentially erroneously included as they are typically purchased alongside a food shop| Kitchen foil, Toothpaste, Homeware| 

Table 1.: Overview of the food categories used in the Eatwell Classification Tool

[^1]: The user can decide how to handle these composite foods dependent on the research question being asked, later versions will assist in claucalitng fruit and vegetable portions in these food groups.




## How the Algorithm works 

 
The text mining algorithm uses an iteratively developed lexicon to assign the product of interest to one of the extended Eatwell categories outlined in table 1. The algorithm first matches to N number of categories and then uses rules based on expert domain knowledge to assign the final category. Matching justifications are provided and are modifiable by the user for transparency.  
 
- E.g. “Eton Mess: Strawberries and Meringue” would match to two categories: Fruit and Vegetables and Discretionary, however as one of the rules is that any product with a Discretionary element is classified as such, therefore the final Eatwell Category assigned would be discretionary.  
 
- E.g. “Garden Salad: Lettuce, Tomato, Cucumber” would match four times to the Fruit and Vegetable Eatwell Category so would be assigned to that category and an indication of high probability of correct classification given.  

## Algorithm Development 
Using real world product data, the algorithm has been designed iteratively to capture a wide range of products. To ensure commercial sensitivity brand names are not used to inform classification, however there is the option for users to assign brand items to an Eatwell category to improve business specific classification. The algorithm and underlying database will continue to be updated to further improve product classification.  
 
## Caveats 
Assumptions on the data may need to be modified dependent on end use 
It is recommended that all classifications are validated against nutritional information. We have produced interactive visualisations (see notebook___) to assist in visual validation of the data. 
Check back regularly for code updates 


## Upcoming .. version (2.0)
 - An interactive web dashboard is planned for version 2.0 to allow the use of the Eatwell classification tool without programming experience.  
