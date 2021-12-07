# The network of Nobel Prize laureates 

This webpage showcases the work we did for the project assignment of the course Social graphs and interactions. 

## Introduction

We chose to build the network of Nobel Prize laureates, using a list of Nobel laureates found on [Wikipedia](https://en.wikipedia.org/wiki/List_of_Nobel_laureates#List_of_laureates), in which there is an edge between two laureates if one of the laureate's Wikipedia page contains a link to the other laureate's page. The network consists in 969 nodes and 3220 edges. We decide to add the attributes year, prize, age, country of birth and gender, retrieved from the laureates' Wikipedia pages, to the nodes of the network. 

Through our analysis of the network, we would like to better understand Nobel Prize laureates and the prizes themselves. In particular, we would like to know what characterizes Nobel laureates in terms of age, gender and nationality, how they are connected to each other and what are the communities of laureates. Finally, we will analyze the Nobel lectures of the laureates, that we extracted from nobelprize.org, to understand their sentiments and how they evolve through time. 

## Network visualization

Below, we visualize the network, where laureates are represented by nodes whose size is proportional to their degree and which are colored according their prize, and edges are colored in red if they connect laureates that were awarded different prizes. 

<p align="center">
  <img src="/images/Network.png">
</p>

Prizes seem to form clusters. But whereas Economics, Peace and Literature form three distinguishable clusters, the scientific prizes, Physics, Chemistry and Physiology or Medicine, seem to form one big cluster. Indeed, these three scientific fields are interdependent, so their clusters are highly interconnected. In addition, the Economics, Peace and Literature clusters seem quite interconnected and well separated from the science cluster, with Peace lying between Literature and Economics which is a little farther. Nevertheless, there is still a significant amount of links that connect these three prizes to the science cluster, revealing the interdependency of the fields. 

Moreover, four bigger nodes stand out: the biggest node of the network, which is Albert Einstein in Physics, followed by the European Union in Peace, and two black nodes, Linus Pauling and Marie Curie, in the science cluster.

You can explore yourself the network with the interactive visualization below and look at the different laureates and their attributes. 

<iframe src="https://github.com/fontaluc/Nobel/images/bokeh.html"
    sandbox="allow-same-origin allow-scripts"
    width="100%"
    height="500"
    scrolling="no"
    seamless="seamless"
    frameborder="0"> </iframe>
    
## Statistics

To know more about the network of laureates, we will compute basic statistics about the number of laureates in each prize, the age of laureates, their gender, country of birth and connectivity. The most interesting results have been summarized below, and more statistics can be found in the explainer notebook which you can find in the GitHub repository of the webpage.

### Number of laureates in each Nobel Prize

Before studying the attributes of laureates, let's look at how they are distributed in the different Nobel prizes.

<p align="center">
  <img src="/images/prize_distribution.png">
</p>

The scientific prizes have the most laureates because it is common that they are jointly awarded to several laureates at the same time, whereas the Literature Nobel Prize usually awards only one laureate every year. It shows that science relies on the multiple perspectives of different researchers on the same topic, unlike literature which is more centered on the individual perspective of a single writer.

<p align="center">
  <img src="/images/prize_distribution_evolution.png">
</p>

According to this plot, the total number of laureates has increased with the years, due to the increase in laureates in almost all of the prizes (except Litterature, with one laureate almost every year) and the introduction of the Economics Nobel Prize in 1969, until 2000 when it begins to stabilize. In addition, we can see two noticeable holes in the plot at the time of the two world wars.

Moreover, this plot explains the distribution of laureates in the different prizes, as seen in the previous figure. Indeed, according to the bar plot, the Peace Nobel Prize is usually awarded to one or two laureates every year, that's why it has an intermediate position in the previous figure. In addition, the Economics Nobel Prize has been introduced later than the other prizes, so it has fewer laureates.

### Age 

Let's find out at what age you can expect to be awarded a Nobel Prize. 

<p align="center">
  <img src="/images/age.png">
</p>

The age to receive a Nobel Prize seems normally distributed around 60, with a mimimum of 17 and a maximum of 97. Let's look at how it differs according to the prize.

![Age distribution per prize](/images/prize_age.png)

All the prizes seem to have roughly a normal distribution for age, with a mean around 60 and maximum around 90. However, the Peace Nobel Prize begins to be awarded earlier in life, with a minimum age of 17, contrary to the Literature and Economics Nobel prizes, which begin to be awarded much later in life, at 42 and 47 respectively. This can be explained by the fact that a writer or an economist, or any scientist, has to build a sufficient amount of work to be recognized, while activists can quickly impact society, with the example of Malala which was awarded the Nobel Prize at the age of 17.

### Gender

Nobel Prizes are awarded to individuals but also organizations, in the case of the Peace Nobel Prize. By looking at the gender of individual laureates, we will be able to assess the Nobel Prize gender gap. 

<p align="center">
  <img src="/images/gender_proportion.png">
</p>

Females account for less than 10% of all the individual laureates. 
But in which prizes are they distributed? Are there more feminine Nobel prizes?

<p align="center">
  <img src="/images/female_distribution.png">
</p>

According to this plot, 30% of all female laureates were awarded the Peace Nobel Prize, followed closely by Literature with more than 25% and Medicine with 20%.

Finally, we would like to know if the Nobel Prize gender gap has been reduced over time.

<p align="center">
  <img src="/images/gender_gap_evolution.png">
</p>

This figure suggests that the Nobel Prize gender gap is reducing in recent years. Indeed, according to the plot, the frequency and yearly number of female laureates has increased since 1960-1970 and reaches a significant proportion of all individual laureates since 2000. But has it improved in all Nobel prizes, including the most masculine field, Physics?

<p align="center">
  <img src="/images/prize_gender_gap_evolution.png">
</p>

There is indeed a recent increase in the frequency and number of female laureates in all Nobel prizes. But this increase is unequal according to the prize. In particular, Physics and Economics Nobel Prizes are still not much awarded to female laureates even nowadays.

### Country of birth

Are there countries from which most of the laureates come from?

<p align="center">
  <img src="/images/top_countries.png">
</p>

The Unites States clearly has by far the most laureates: by counting only the laureates whose country attribute is not 'Unknown', more than 25% of all laureates were born in the United States. Many of the laureates were also born in Germany and France, with respectively more than 10% and 5% of all laureates. More surprising is the fact that Austria, Russia and Poland are in the top 10 countries even though today they are not considered among the most advanced countries in the world, but this could be explained by their past contribution to science. On the contrary, China, which is today one of the most powerful countries in the world, and competes wih the United States on the international stage, is not in the top 10 countries, because it is still an emergent country. To confirm these hypotheses, we investigated the evolution of the number of laureates from these 4 countries.

<p align="center">
  <img src="/images/odd_countries.png">
</p>

Laureates from Austria, Russia and Poland were indeed mostly awarded in the past. According to the plots, laureates from Austria and Poland frequently received Nobel Prizes in the past but the frequency seems to decrease with time, especially for Poland. On the other hand, Russia had a high frequency of Nobel Prizes during the Cold War. On the contrary, Nobel Prizes were not much awarded to Chinese laureates in the past, but it has become more frequent since 1990, which makes sense given that China is an emergent country.

Finally, we would like to know if the top countries are the same for all Nobel Prizes, and if any country is especially strong in one field.

<p align="center">
  <img src="/images/prize_top_countries_small.png">
</p>

According to the plots, the United States is the first country for all Nobel Prizes. It is especially good in Economics, for which almost 50% of the laureates come from the United States, but less in Literature, for which France has almost the same number of laureates (10%). Germany follows the United States in all scientific prizes, but is outcompeted by France for Peace.
