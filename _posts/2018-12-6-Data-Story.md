---
layout: post
title: Impacts of Globalization on Food
---

# A Story of Food Globalization
  Is is something we may not pay much attention to or that may have become normal in our everyday lives but the food we buy at the supermarket comes from further and further locations across the globe. If we just think of the products we ate today it is probable that some were grown or manufactured on another continent. With the fast growth and democratization of transports, the food we eat everyday no longer depends on the local production but tends to come from various parts of the globe. 
  
  This has a lot of consequences that we are not always aware of. At a time when global warming is more than ever an actual issue we can ask ourselves questions about the ecological impact of this phenomenon. Does food globalization have an important ecological fooprint ? But we can also ask ourselves about the health aspect, does this change in the way we feed ourselves has an impact on our health ? Using the Open Food Facts Dataset we will discover and analyze the various impacts of this food globalization.
  
  
<!---  Our project will mainly focus on important actual issues regarding its ecological and health aspects. We will first get more insights about the food transportation process, about its origin and destination and the ecological footprint of this transportation. We will then get to find how food affects our health by comparing the food consumption of countries to their global health indicators and look for the effects of this uniformization of food consumption. -->

# The Data
The data used for this data story can be found on the [Open Food Facts website](https://world.openfoodfacts.org/data). This is a collaborative, free and open database of food products from around the world. A great number of products are referenced in this dataset, along with informations about them like their origin, ingredients, nutional score...
Note that since that data is maintained by users, some of its information can be false or very biased. The data was cleaned but some errors could still be present.

  To be able to study the food through various aspects, we also used data from the [World Bank website](https://www.worldbank.org/) to get statistics about countries like their GDP or life expectancy.

<!---

## Countries
We visualize here the number of products sold in each country. We see that the distribution is not uniform like we would have in an ideal case, it is highly unbalanced, more than half of the products in the database come from France. The vast majority of the products are present in countries like France, the United States or Switzerland. Hence we will have to focus our study on these countries having a sufficiently large number of products.
![_config.yml]({{ site.baseurl }}/images/hist_countries.png)

## Manufacturing Places
We also visualize the manufacturing places but as before the distribution is highly unbalanced. We will only use countries having a sufficient amount of manufactured products to avoid any eventual bias that we could have by using countries with very little products.
![_config.yml]({{ site.baseurl }}/images/hist_manu.png)

## Origins
Finally the origin of the ingredients is displayed. Again France is by far the country with the most products and the distribution is not uniform. We see that the second in the list is the European Union, France is part of this Union TODO ON FAIT QUOI DE FRANCE UE ??
![_config.yml]({{ site.baseurl }}/images/hist_origins.png)



# Food Manufacturing and Transportation
We start our journey by visualizing on a map the places where the products referenced in our data are manufactured. Like we observe the majority of our products are produced in Europe (which is not surprising since the foundation behind this data is french) but we also have products manufactured in almost every continent. You can zoom in and out on the map and by doing this we can see that the countries having the most represented products are France, the United States, Switzerland and Germany. We will take some of these as case studies later in our story.
<iframe src="https://adamanteam.github.io/products.html" width="100%" height="400px"></iframe>

--->

# Where does the food sold in France comes from ?
We start our journey by visualizing on a map from where are the origins of food imported in France. Why in France ? Because the dataset we have contains mostly food product sold in France, therefore we will get the most interesting results.

*Map of all origins of ingredients*
<iframe src="https://adamanteam.github.io/geodesic_map.html" width="100%" height="400px"></iframe>

On this map, we have a whooping number of 87 countries. The food french people eat comes from really all over the world. 


# Food Societal Aspects
TODO We first observe the societal aspects of the food around the globe.

## Food quality and general health
TODO We would first like to discover if for a given country the quality of the food that is consumed there can have an influence on the global health of this country. We represent on a world map the average nutritient score for products in a country, for countries having a sufficient amount of product with this data. Unfortunately like we see a large amount of countries do not meet this requirement. We see that globally nothern countries seems to obtain a better score on average.

<iframe src="https://adamanteam.github.io/nut_scores.html" width="100%" height="400px"></iframe>

We can now try to answer our previous question : does food quality have an impact on our heatlth ? We can try to analyze this by looking if we can make any correlation between the average score of a country and its GDP. A high score would indicate that a country has a better alimentation in general and the life expectancy is a good indicator of the global health of a country. This is why we represent the life expectancy next to a normalized average nutritient scores, for the countries for which we have data.

![_config.yml]({{ site.baseurl }}/images/grade_lexp.png)

We observe that countries with low nutritient scores seem to have on average a lower life expectancy like it is the case for Romania. The countries with the highest scores, Sweden and the Netherlands, also have some some of highest life expectancy of the set. This could suggest that there may be some correlation between the two. We compute that their correlation score is of 0.502. This show that a correlation may be possible but is not completely sufficient to prove it. We would need more data to confirm or infirm this assumption. 

## Food quality and general wealth
TODO We will also analyze the possible links between average food quality and the global wealth of a country. For this we will again use the nutritional coefficients grades, (maybe the average number of nocive additives) and the GDPs. TODO correlation of 0.373

![_config.yml]({{ site.baseurl }}/images/grade_gdp_capita.png)
