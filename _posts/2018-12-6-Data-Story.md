---
layout: post
title: Impacts of Globalization on Food
---

# Abstract
  With the fast growth and democratization of transports, the food we eat everyday no longer depends on the local production but tends to come from various parts of the globe. Using the Open Food Facts Dataset, our goal is to discover and analyze the various impacts of this food globalization.
  
  Our project will mainly focus on important actual issues regarding its ecological and health aspects. We will first get more insights about the food transportation process, about its origin and destination and the ecological footprint of this transportation. We will then get to find how food affects our health by comparing the food consumption of countries to their global health indicators and look for the effects of this uniformization of food consumption.


# The Data
The data used for this data story can be found on the [Open Food Facts website](https://world.openfoodfacts.org/data). This is a collaborative, free and open database of food products from around the world. A great number of products are referenced in this dataset, along with informations about them like their origin, ingredients, nutional score..

  To be able to study the food through various aspects, we also used data from the [World Bank website](https://www.worldbank.org/) to get statistics about countries like their GDP or life expectancy.

## Countries
We visualize here the number of products sold in each country. We see that the distribution is not uniform like we would have in an ideal case, it is highly unbalanced, more than half of the products in the database come from France. The vast majority of the products are present in countries like France, the United States or Switzerland. Hence we will have to focus our study on these countries having a sufficiently large number of products.
![_config.yml]({{ site.baseurl }}/images/hist_countries.png)

## Manufacturing Places
We also visualize the manufacturing places but as before the distribution is highly unbalanced. We will only use countries having a sufficient amount of manufactured products to avoid any eventual bias that we could have by using countries with very little products.
![_config.yml]({{ site.baseurl }}/images/hist_manu.png)

## Origins
Finally the origin of the ingredients is displayed. Again France is by far the country with the most products and the distribution is not uniform. We see that the second in the list is the European Union, France is part of this Union TODO ON FAIT QUOI DE FRANCE UE ??
![_config.yml]({{ site.baseurl }}/images/hist_origins.png)


# Maps
"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
<iframe src="https://adamanteam.github.io/products.html" width="100%" height="400px"></iframe>
  
# Food Societal Aspects

TODO We first observe the societal aspects of the food around the globe.

## Food quality and general health

TODO We would first like to discover if for a given country the quality of the food that is consumed there can have an influence on the global health of this country. To this purpose we will use the nutritional coefficients grades, (maybe the average number of nocive additives) and the life expectancy data.

## Food quality and general wealth

TODO We will also analyze the possible links between average food quality and the global wealth of a country. For this we will again use the nutritional coefficients grades, (maybe the average number of nocive additives) and the GDPs.
