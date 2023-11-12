# Movie Plots Analysis
![Clusters Formed](movie_clusters.png)

## Table of Contents

1. [Introduction](#introduction)
2. [Data Cleaning](#data-cleaning)
3. [Classification](#classification)
4. [Similar Movie Finder](#similar-movie-finder)
5. [Clustering](#clustering)
6. [Keyword Extraction](#keyword-extraction)
7. [Analyzing the Scripts Classified Plot-wise](#analyzing-the-scripts-classified-plot-wise)
8. [Analyzing the Scripts Decade-wise](#analyzing-the-scripts-decade-wise)
9. [Exploratory Data Analysis](#exploratory-data-analysis)
10. [References](#references)

## Introduction <a name="introduction"></a>

Movies have long been a captivating medium, weaving stories that resonate with audiences across generations. This project delves into the essence of cinematic narratives, aiming to identify the fundamental plots that have shaped our understanding of storytelling. By analyzing the scripts of the top 3 IMDb hits from the 1970s to the 2020s, we embark on a journey to uncover the underlying patterns that define these cinematic masterpieces.

## Data Cleaning <a name="data-cleaning"></a>

The data is sourced from a JSON file containing movie scripts. The following cleaning steps were performed:
- Lowercasing all text
- Removing symbols and line breaks
- Eliminating punctuation
- Removing stop words
- Lemmatizing the data for better contextual analysis

## Classification <a name="classification"></a>

A TF-IDF matrix of the movie scripts is created, and similarity distances are computed using cosine similarity. Hierarchical clustering is applied to identify basic plots, and the results are visualized using dendrograms.

## Similar Movie Finder <a name="similar-movie-finder"></a>

Cosine similarity is used to find similar movies based on the TF-IDF vectors of their scripts. A function, `find_similar`, is provided to identify the most similar movie for a given title.

## Clustering <a name="clustering"></a>

Clustering is the building block of this project helping us see if there exists a natural sectioning of movies from last 50 years to fall into constant plots/themes purely based on their script proving our initial hypothesis true. For this purpose, scripts are clustered based on their similarity using the KMeans algorithm. The optimal number of clusters is determined using the Elbow Method.

## Keyword Extraction <a name="keyword-extraction"></a>

Keywords act as the building blocks of narratives, encapsulating the essence of each story. Through the extraction of keywords using TF-IDF vectors, we gain a nuanced understanding of the pivotal elements that define these cinematic experiences. The top 10 keywords for each movie serve as beacons, illuminating the thematic landscape.

## Analyzing the Scripts Classified Plot-wise <a name="analyzing-the-scripts-classified-plot-wise"></a>

Plot-wise classification opens a portal to the diverse worlds crafted by filmmakers. The subsequent generation of word clouds for each cluster transforms textual data into visually engaging insights. By visually representing common themes, these word clouds offer a unique perspective on the shared narratives within each cluster.

## Analyzing the Scripts Decade-wise <a name="analyzing-the-scripts-decade-wise"></a>

Decades are chapters in the cinematic timeline, each marked by unique storytelling trends. By categorizing scripts based on their respective decades, we embark on a journey through the evolving landscape of movie genres. The resulting word clouds serve as time capsules, preserving the essence of storytelling trends across different eras.

## Exploratory Data Analysis <a name="exploratory-data-analysis"></a>

Beyond the narrative nuances, exploratory data analysis brings quantitative insights to the forefront. The conversion of running time to minutes and the subsequent visualization of movie durations over the years offer a comprehensive view of temporal trends. This analytical journey bridges the gap between storytelling and data, providing a holistic understanding of cinematic evolution.

## References <a name="references"></a>

My work was underlined by studies done in the research paper "The emotional arcs of stories are dominated by six basic shapes" by Andrew J. Reagan, Lewis Mitchell, Dilan Kiley, Christopher M. Danforth, and Peter Sheridan Dodds, published on July 8, 2016. The paper investigates emotional arcs in stories, which provides additional context and inspiration for the clustering approach used in this project.

---

*Note: This readme provides an overview and explanations of the code. For specific code details, refer to the source code file.*
