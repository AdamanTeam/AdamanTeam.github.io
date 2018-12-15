---
layout: post
title: A Story of Food Globalization
---

  It is a simple thing we may not pay much attention to or that may have become normal in our everyday lives but the food we buy at the supermarket comes from further and further locations across the globe. If we just think of the products we ate today it would not be surprising that some were grown or manufactured on another continent. With the fast growth and democratization of transports, the food we eat everyday no longer depends on the local production but tends to come from various parts of the globe.

  This has a lot of consequences that we are not always aware of. At a time when global warming is more than ever an actual issue we can ask ourselves questions about the ecological impact of this phenomenon. Does food globalization have an important ecological fooprint ? But we can also ask ourselves about the health aspect, does this change in the way we feed ourselves has an impact on our health ? Using the Open Food Facts Dataset we will discover and analyze the various impacts of this food globalization.


<!---  Our project will mainly focus on important actual issues regarding its ecological and health aspects. We will first get more insights about the food transportation process, about its origin and destination and the ecological footprint of this transportation. We will then get to find how food affects our health by comparing the food consumption of countries to their global health indicators and look for the effects of this uniformization of food consumption. -->

# The Data
The data used for this data story can be found on the [Open Food Facts website](https://world.openfoodfacts.org/data). This is a collaborative, free and open database of food products from around the world. A great number of products are referenced in this dataset, along with informations about them like their origin, ingredients, nutional score..
Note that since that data is collaborative and maintained by users, some of it can be false or very biased. The raw data was cleaned as much as possible but some errors could still be present. We can show an example of this just by plotting the distribution of the number of products we have in our dataset per country.

*Number of products in the dataset by country*
![_config.yml]({{ site.baseurl }}/images/hist_countries.png)

As we can see on the plot this dataset is largely dominated by French products followed by product from the US. This is due to the fact that this collaborative website from which the data was taken is french and visited mostly by french users. To talk about the effect of globalization the best case would have been to have data from all over the world but we can still manage to get interesting results by focusing our analysis on some of these beautiful countries like France!

We can also visualize this on a map to get a better feeling of how these product repartition is made. Here the log is taken because the number of products from France was too great compared to other countries.

*Map of the number of products in the dataset by country (log visualization)*
<iframe src="https://adamanteam.github.io/map_occurences.html" width="100%" height="400px"></iframe>

 We see that we most of the products are located in european countries like France or Switzerland. Also some countries like the United States, Mexico or Australia are represented. This is not the ideal case like we already said but this is a common thing to have unperfect data like this in the real world so we will work with it.

  To be able to study the food through various aspects, we also used data from the [World Bank website](https://www.worldbank.org/). These are statistics about countries like their GDP per capita or life expectancy, that we will use later in our story. We are now ready to begin our study. We start by trying to answer the first question that came to our minds : food products often travel hundreds or even thousands of kilometers before reaching our plates, what is then the environmental impact of this food globalization ?

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

# The environmental impact of food globalization
We start by the origins : before being transported and then consumed the food needs to be produced or manufactured somewhere. Where is somewhere will you ask ? Well we can discover that by drawing on a map all the locations from which the food in our dataset originates.

*Cluster map of all places of origins present in the dataset*
<iframe src="https://adamanteam.github.io/cluster_map.html" width="100%" height="400px"></iframe>

We can see on the map that the locations are more precise in Europe where the majority of our products are from, especially in France where there is a clear cluster of points of origins. As we saw previously, since most of our products are located in France this large number of French made products does not surprise us. We can also spot locations in North and South America as well as in Asia.

## Globalization through the case of France

As we already saw France is the country which has the richest amount of data, of consumed and produced products in our data. This is why we now chose focus on France as this is by studying specifically this country that we will get the most interesting results. A first step to observe the globalization would then be to look at where does the food consumed in France come from ?

*Map of French ingredients importations*
<iframe src="https://adamanteam.github.io/geodesic_map.html" width="100%" height="400px"></iframe>

The first thing that suprises us on this map is that we have a whooping number of 87 different origin countries! The food french people import not only comes from close european countries like we could expect but really comes from all over the world. Almost every continent is well represented and food can come from countries as far as New-Zealand. We see that indeed talk today about a globalization of food .

This map however doesn't tell us how much ingredients comes from each country, therefore we now display a Bubble map where the circles are proportional to the number of ingredients originating from that country and sold in France. This will give us additional information about french importations and allow to quantitize them.

*Bubble map proportional to number of products with ingredients originating in the country*
<iframe src="https://adamanteam.github.io/bubble_map.html" width="100%" height="400px"></iframe>

What we notice is that most of the imported products comes from relatively close countries like Spain, Italy and the United Kingdom by a large margin. This is something we could have expected since the European Union favorizes the trade of food and products of agriculture among european countries. We still notice that there is a non-negligeable amount of products coming from other continents like Asia, America or Africa. We expect this quantities to be underestimated compared to the reality since our data is biased like we saw.

We now know what quantities of products are transported to France and from where. It could now be interesting an interesting idea to look at what kind of products are the most imported from these countries. We visualize these using  WordClouds where the size of the name of a product is relative to the frequency it appears in the data. Hence the bigger a product appears, the most it is imported to France from this country. We take the case of Spain, Italy and United Kingdom as these three appeared previously to be the biggest exporters to France.

**Spain**
{:refdef: style="text-align: center;"}
![_config.yml]({{ site.baseurl }}/images/spain_to_france.png)
{: refdef}

Here we see that these products consists mainly of olive extracts or fruits and vegetables, the most exported products being Huile d'olive, Olives Vertes, Tomate, Citron, Orange, Miel, Framboise. These products, specifically fruits and vegetables do not last long so it is understandable that there are mostly exported to the neighboring country of France. These country seems rather healthy and we could say that Spain has a rather positive effect on french alimentation.

**Italy**
{:refdef: style="text-align: center;"}
![_config.yml]({{ site.baseurl }}/images/italy_to_france.png)
{: refdef}
Here we also see prodcuts like Miel, Vinaigre balsamique, Parmigiano Reggiano, Riz, Pomme, Jus de citron but also some typically italian products like Pizza, Parmigiano Reggiano and Spaghetti.

**United Kingdom**
{:refdef: style="text-align: center;"}
![_config.yml]({{ site.baseurl }}/images/uk_to_france.png)
{: refdef}
The products exported by the United Kingdom mostly consists of fish or seafood : Saumon fumé, Coquille Saint Jacques, Noix de Saint Jacques, but also alcohols like Whisky.

Now that we have a more precise idea about the food transportation across the world, where does it comes from, to where, which kind of food, we can look at the environmental impact of all this transportations.

## Environmental impact

After analyzing how the globalization of food affect the life of people around the world we now want to see how it does affect the planet too. In order to be able to eat food that is not produced in the country, the country needs to import it from the outside. As we saw before with the case of France most countries prioritize importations and exportations from the neighboring countries in order to reduce the ecological impact but also for practical purposes. However, sometimes these countries do not have another option than importing products from far away countries. 

To compute the impact of this transportation we decided to make an estimation of the quantity of CO2 emitted. We decided to keep 0.023 kg per km and per gram of packaged used as a global approximation of the emiteed quantity, since we do not have detailed information about the mode of transportation and path followed by each product. This is not meant to give a precise number of the emissions but rather to allow us to get an idea and a rough approximation of these. 

Also as shown previously some countries have a larger amount of products in our dataset, this does not mean they import more, at least not in the way we could observe. That is why we decided to normalize the data and hence focus on how countries do import products, i.e do they import from far away countries or more locally?

<iframe src="https://adamanteam.github.io/co2_per_country.html" width="100%" height="400px"></iframe>

First we see that the european countries seems to produce less C02 emissions on average from their food importations than the other countries. This can easily be explained because as we saw before, countries inside the European Union tend to trade large amount of food between them since it is a free market. Hence the food imported to countries like France, Germany or Italy mostly comes from "local" european countries, emitting less C02. 

More isolated countries like the United States or China, known to be huge consumers seems to not produce enough and need to import products from further located countries. They emitt more C02 than the previous countries. The worst emitters seems to be some african countries like Cameroun or Guinée. The food production seems to be not enough and since the neighboring countries also lack production, they need to import bigger amounts of products from abroad and have then a bigger environmental impact. These are only interpretations and the observed results may also rely on other hidden factors. With more data we would have been able to get more accurate and trustable results.

# Food Societal Aspects
We will now try to observe the societal aspects of food around the globe.

## Food quality and general health
Before getting started we need to explain the notion of Nutrition Score: The Nutrition Score is a score given to each aliment were they perform an analysis of 26 positive and negative factors compared to the calories in the food. The positive factors are those such as vitamins, minerals, proteins, etc. and the negative ones are those such as cholesterol, saturated fat, sugar, etc.


We would first like to discover if for a given country the quality of the food that is consumed there can have an influence on the global health of this country. We represent on a world map the average nutritient score for products in a country, for countries having a sufficient amount of product with this data. Unfortunately like we see a large amount of countries do not meet this requirement. We see that globally nothern countries seems to obtain a better score on average.

<iframe src="https://adamanteam.github.io/nut_scores.html" width="100%" height="400px"></iframe>

We can also visualize the distribution of the nutritient scores for the countries having the most products in the dataset.

![_config.yml]({{ site.baseurl }}/images/grades_dist.png)

We can now try to answer our previous question : does food quality have an impact on our heatlth ? We can try to analyze this by looking if we can make any correlation between the average score of a country and its GDP. A high score would indicate that a country has a better alimentation in general and the life expectancy is a good indicator of the global health of a country. This is why we represent the life expectancy next to a normalized average nutritient scores, for the countries for which we have data.

![_config.yml]({{ site.baseurl }}/images/grade_lexp.png)

We observe that countries with low nutritient scores seem to have on average a lower life expectancy like it is the case for Romania. The countries with the highest scores, Sweden and the Netherlands, also have some some of highest life expectancy of the set. This could suggest that there may be some correlation between the two. We compute that their correlation score is of 0.502. This show that a correlation may be possible but is not completely sufficient to prove it. We would need more data to confirm or infirm this assumption.  We draw here a scatter plot to visualize the dependency between the two.

{:refdef: style="text-align: center;"}
![_config.yml]({{ site.baseurl }}/images/grade_lexp_corr.png)
{: refdef}

## Food quality and general wealth
We can now ask ourselves if there exists any possible links between the average food quality and the global wealth of a country. For this we again make use of the nutritional coefficients grades and the GDPs. We plot the results as a bar chart representing the GDP per capita for each country next to a normalized version of their average nutritient score and try to observe if we see any possible dependency.

![_config.yml]({{ site.baseurl }}/images/grade_gdp_capita.png)

We see that there does not seems to be any real correlation between the two data. Wealthy countries like Switzerland, the United States or Australia obtain worse grades than countries with a much lower GDP per captia like Spain or Mexico. This suggest that the wealth of a country does not seems to have any direct influence on the quality of the food that is eaten there. It is not because a country can afford to produce and consume higher quality food that it does. We compute the correlation coefficient of this data and get a value of 0.373. As expected this does not indicate any correlation between the wealth and the food quality. We draw again a scatter plot of the values.

{:refdef: style="text-align: center;"}
![_config.yml]({{ site.baseurl }}/images/grade_gdp_corr.png)
{: refdef}

As we see there does not seems to be a clear correlation between the two. More data would have been necessary to confirm this with more confidence.

<iframe src="https://plot.ly/~MaxL./0.embed" width="100%" height="400px"></iframe>


