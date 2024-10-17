# Network Analysis of Nobel Prize Laureates

The webpage of the project: [The Nobel Prize Laureates Network](https://fontaluc.github.io/Nobel/)

All the code is gathered in one self explanatory [here](https://github.com/MiladMt11/Network-Analysis-of-Nobel-Prize-Laureates/blob/c18a26a4d2cb6aa19f4e12842c7f118bcaaa8386/Notebook_files/Nobel_Prize_Laureates_Network_Final.ipynb) or via [Nbviewr](https://nbviewer.org/github/fontaluc/Nobel/blob/734c8e35bd1131ff46eaa7f08c07c4325299d601/Notebook_files/Nobel_Prize_Laureates_Network_Final.ipynb)

## Intro & The Network:
This project builds a network of Nobel Prize laureates based on data from Wikipedia. The nodes in this network represent individual laureates, and an edge exists between two laureates if one laureate's Wikipedia page contains a link to the other laureate's page. 
The final network consists of 969 nodes and 3220 edges.

We enriched the network with additional attributes for each laureate, including:
* Year of the award
* Prize category
* Age at the time of the award
* Country of birth
* Gender

These attributes were also sourced from the laureates’ Wikipedia pages.

## Objectives:
The primary goal of this project is to explore and analyze the network to gain insights into the Nobel laureates and the prizes themselves. Specifically, we aim to:

* Understand the characteristics of Nobel laureates, focusing on age, gender, and nationality.
* Investigate the connections between laureates to identify patterns in how they are linked to one another.
* Discover communities within the laureates’ network and analyze how they form.
* Perform sentiment analysis on Nobel lectures, which were extracted from nobelprize.org, to observe how sentiments expressed in these lectures evolve over time.

## Project Components & Methodology:
1. **Web Scraping:** Automated extraction of data on Nobel laureates from various sources, including Wikipedia for biographical details and NobelPrize.org for Nobel lecture content.
2. **Network Creation & Visualization:** Construction of a network graph where each node represents a Nobel laureate, and an edge is drawn between two laureates if one laureate's Wikipedia page links to another's. This includes enriching nodes with attributes like prize category, year, age, gender, and country of birth.
3. **Statistical Analysis:** Applying statistical techniques to explore relationships and trends in laureates' demographics and prize categories, including correlation analysis, hypothesis testing, and identifying significant variations over time or across different groups.
4. **Exploratory Data Analysis (EDA):** Exploring the dataset of laureates to uncover patterns and insights related to their demographics, such as distributions of age, gender, country of birth, and prize categories. This stage includes data visualization to understand the overall structure and characteristics of the laureates.
5. [**Community Detection:**](https://en.wikipedia.org/wiki/Community_structure) Applying community detection algorithms (e.g., Louvain, Girvan-Newman) to the laureate network to identify groups or clusters of laureates who are more interconnected. These communities can provide insights into collaborations or thematic groupings of prize winners.
6. [**TF-IDF (Term Frequency-Inverse Document Frequency) Analysis:**](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)
7. **Sentiment and Textual Analysis:** Performing sentiment analysis on Nobel lectures to evaluate the emotional tone over time. Creating word clouds to visually represent the most frequently used words and recurring themes in laureates' speeches. This combined analysis uncovers both the topics and sentiments shaping their thoughts across different periods.

## Data:
* Wikipedia: Used for the list of Nobel laureates and their biographical details (year, prize, age, country of birth, and gender).
* Nobelprize.org: Source for the Nobel lectures used in sentiment analysis.

## Packages & Frameworks:
* [NLTK](https://www.nltk.org/)
* [beautifulSoup](https://beautiful-soup-4.readthedocs.io/en/latest/)
* [WordCloud](https://pypi.org/project/wordcloud/)
* [RegEx](https://docs.python.org/3/library/re.html)
* [ForceAtlas](https://pypi.org/project/ForceAtlas2/)

## Installation:
If you want to run the notebookremember to Install the required Python packages using `pip`:

    ```bash
    pip install -r requirements.txt
    ```

  
## References
[^1] https://www.nobelprize.org/

[^2] Project 2 Charidimos Vradis, Lucie Fontaine, Milad Taghikhani

[^3] VADER: A Parsimonious Rule-based Model for Sentiment Analysis of Social Media Text C.J. Hutto Eric Gilbert

[^4] https://en.wikipedia.org/wiki/Modularity_(networks)

[^5] https://en.wikipedia.org/wiki/Tf%E2%80%93idf

[^6] Thelwall, Mike. (2017). Gender Bias in Sentiment Analysis. Online Information Review. 42. 00-00. 10.1108/OIR-05-2017-0139.

## License
This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## Contact
We're open to any feedback, suggestions, or questions regarding the projects or the repository. Don't hesitate to contact via email at milad.mtkh@gmail.com.
