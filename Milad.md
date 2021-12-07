## Connectivity
In this section we would like to show how connected our network is. As part of measuring the network's connectivity, we have created three different plots, each representing a different piece of information about the network.

### Most Influential Laureates
First, let's take a look at who are the most influential laureates in our network. In order to accomplish this, we plotted the top 10 laureates with the highest degree in the network.

<p align="center">
  <img src="/images/Top10 Influential.png">
</p>

As it can be seen in the plot, almost all of the laureates shown in the plot, have won the award in one of the scientific categories. "United Nations" is also on the top ten list which is most likely because many laureates in the peace category are somehow related to this organization due to their activities, thus the number of connectios of this node is relatively high. Additionally, an organization such as United Nations could potentially have links to laureates in other categories as well.

### Connectivity Through Time
The goal of this part is to discuss the connectivity of the network for each year. The following plots are provided in this regard.

The first plot below represents the average degree for each year. Based on the plot, it's clear that four periods of time have the highest average degrees. In the first period, the prize was only awarded in two categories, Physics and Chemistry, which clarifies the noticable high average degree in the year 1918. Additionally, The laureates in these categories were "Max Planck" and "Fritz Haber" who are both located in our network with a great amount of connectivity. The other three periods were 1962, 1954 and 1944. In each of these years, there was a laureate who is also listed among our top 10 most influential laureates with the highest degree, people like "Otto Hahn", "Linus Pauling" and "Max Born". Therefore, the average degree in the mentioned years is almost higher than the other years.

<p align="center">
  <img src="/images/Average Connectivity Through Time.png">
</p>

Using the second plot, we attempted to represent the maximum degree over time. There is a noticeable difference in the maximum degree for each year before 1965 compared to years after 1965. The reason behind this might be that as we move forward in time, references (links) to laureates who won the award in the past increase. This may caused by the citations or references made by recent laureates to previous laureates work. consequently, the average degree in the years before 1965 is higher than in recent years.

<p align="center">
  <img src="/images/Max Connectivity Through Time.png">
</p>

### Connectivity for Each Category
We can also examine connectivity from another aspect by investigating the maximum degree of connection among the winners of each category.
According to the following plot, clearly, the Physics category is the one with the highest connectivity.Why is this so?
This can be explained by the fact that laureates in the Physics category tend to have more collaboration in their research fields and other scientific areas, also it may be possible that they have shared the prize with one or to other laureates. As well as that, It is possible to consider references and citations in this regard. On the other hand, the lowest maximum degree belongs to the literature category. Perhaps this is because literature laureates may not collaborate as much as other categories. Moreover, there is no significant relation between laureates in literarture and laureates in other categories.

<p align="center">
  <img src="/images/Max Connectivity Each Category.png">
</p>

## Word Clouds
What words appeared the most in laureates pages?
How does the word or words relate to the category in which the laureate was awarded?
In this section we used word clouds to show the most frequent words in each of the prize categories as well as in each community (which we obtained by implementing [Louvain Method](https://en.wikipedia.org/wiki/Louvain_method)).

### Category Word Cloud
Below you can find the word clouds for each category.

<p align="center">
  <img src=>
</p>

As it can be seen in the picture, words like "Particle", "Neutrino", "Gravitational", "Supernova" and etc. have appeared the most in the Physics category. This represents, most of the content of laureates Wikipedia pages is about the main concepts of physics like gravity, subatomic particles, astronomy and etc. It is interesting to note that the word "Protein" appeared in both Chemistry and Physiology or Medicine categories. As was expected, there is a lot of economy-related phrases shown in the Economics category word cloud. Words like "poem", "poetry", "screenplay" and "playwright" are the most frequent ones in the Literature category which refer to different contexts of literature. Most of the words appeard in the word cloud of Peace category are abberivations for peace related or political organizations.

### Communities Word Cloud

