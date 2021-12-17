# Project 2 - Ames Housing/Garage Data and Kaggle Challenge

### Problem Statement

If you own a car and you're looking for a house, you probably want a garage to come with the house. But does the garage alone mean the house is too expensive? This project aims to not only determine how different garage attributes affect the price of a house, but also how those three factors compare to non-garage statistics in doing so. The answer will come out through fitting a linear model on both garage-focused and other attributes to predict price.

### Datasets

* [`train.csv`](../datasets/train.csv): The training set used for modeling, containing information on sold houses in Ames, Iowa, including prices. ([source](https://www.kaggle.com/c/hopper-project-2-regression-challenge/data))
* [`test.csv`](../datasets/test.csv): The test set used for modeling, containing information on a different set of sold houses in Ames, Iowa, not including prices. ([source](https://www.kaggle.com/c/hopper-project-2-regression-challenge/data))

### Data Dictionary

These are the twelve columns that are included in the final model predicting sale price.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**Garage Cars**|*int*|train & test|The number of cars that can fit inside the house's garage.|
|**AttachedGarage**|*int*|N/A|Set to 1 if the garage is attached to or inside the house and 0 if it is outside or there is no garage. Based on data from the column 'Garage Type' in the train & test sets.|
|**Garage Finish**|*int*|train & test|The state of the garage's interior finish: finished, rough finished, unfinished, or none.|
|**Overall Qual**|*int*|train & test|The overall quality of the house on a scale of 1 to 10.|
|**Overall Cond**|*int*|train & test|The overall condition of the house on a scale of 1 to 10.|
|**Year Built**|*int*|train & test|The year the house was originally built.|
|**Total Bsmt SF**|*int*|train & test|The total area (in square feet) of the basement.|
|**Residential**|*int*|N/A|Set to 1 if the building is residential and 0 if the building is agricultural, commercial, or industrial. Based on data from the column 'MS Zoning' in the train & test sets.|
|**Expensive Nbrhd**|*int*|N/A|Whether the house is located in one of the six most expensive Ames neighborhoods. Based on data from the column 'Neighborhood' in the train & test sets.|
|**PosProx**|*int*|N/A|Whether the house is close to positive off-site features. Based on data from the columns 'Condition 1' and 'Condition 2' in the train & test sets.|
|**Grd Liv Area**|*int*|train & test|The total area (in square feet) of the above-ground living area.|
|**WoodRoof**|*int*|N/A|Whether the house's roof is made of wood. Based on data from the column 'Roof Matl' in the train & test sets.|

### Conclusions & Recommendations

The three garage categories which you should focus on while trying to figure out the price of the house you want are the number of cars, the state of the interior finish, and whether the garage is connected to the house or not, in that order.

Easily the most impactful of the three is the number of cars, likely because higher area in general greatly increases price.

Future research would need to include garage-specific statistics that could greatly affect price and are more than likely not correlated with the rest of the home. These include the date the garage was built and (for garages not built into the home) what the roofing material of the garage is.