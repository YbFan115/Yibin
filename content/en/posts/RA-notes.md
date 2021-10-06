---
title: "RA Notes"
date: 2021-08-30T15:31:09+08:00
draft: false
---

**Notes**: This post is written to keep the ideas alive and document what I learn from the research work with [Nate](https://teblunthuis.cc). Since Aug. 2021, I began to contribute to the project of Nate which is intended to find the connections between two online communities - [Fandom wiki](https://www.fandom.com/explore) (which was previously known as Wikia) and [Reddit](www.reddit.com). I make a role in the dataset construction.

- **Wikidata and SPARQL language**: Wikidata is an open source knowledge graph that has structured data about relationships between different entities. Here is an example: [One Piece](https://www.wikidata.org/wiki/Q673). Wikidata provides a query service which can run by SPARQL language, to find the qualified entities and properties in the dataset. I have learned the rules for SPARQL, and pulled the entities that have both a fandom wiki and a subreddit ID. 
- **Precision and recall**: How good the mapping in Wikidata is to be checked. Precision and recall rate can be used to examine it. 

- **Linux**: To be more efficient to collaborate, I set the Linux and began to join the git of [Community Data Science Collective](https://wiki.communitydata.science/Main_Page), which is a research group focused on online communities. 
	- use `explorer.exe .` to find the Linux files in Windows
	- if `sudo apt install ...` fails, it can probably be solved by `sudo apt install -y ... --fix-missing`(see in [Help Docs](https://help.aliyun.com/knowledge_detail/41205.html?spm=a2c6h.13066369.0.0.21837b3ejhCgyA)) 
	- to find the ip for linux, use `ifconfig -a`
	- to open xrdp, use `sudo service xrdp restart`

- **Wikidata**: According to the query outcome in Wikidata, it seems like dataset in Wikidata does not have a good coverage for the match between a fandom wiki and a subreddit, but include almost no error due to the properties for Wikipedia. We are going to deal with more data to get back at the dataset in Wikidata.

- **Machine Learning Classification**: To find out whether a subreddit and a fandom wiki is really similar or the mapping between them is correct, there can be some ideas from [machine learning classification](https://machinelearningmastery.com/types-of-classification-in-machine-learning/).

- **Machine Learning for Social Sciences**: Machine learning models used in social sciences has triggered a heated discussion: whether it is "garbage in, garbage out" ([Geiger et al., 2019](https://doi.org/10.1145/3351095.3372862)) or "theory in, theory out" ([Radford & Joseph, 2020](https://doi.org/10.3389/fdata.2020.00018))?

- **Rules for prediction**: Simpler than real ML classifier, if we give a set of rules to predict the correctnesss of mappings it would also make sense. An example rule Nate gave is:
	
	```
	The wiki is the top linked wiki from the subreddit AND
	(The subreddit and wiki are linked in wikidata OR
		The subreddit and wiki names are similar OR
		The subreddit-link zscore for the wiki is large
		)
	````
- **Validation Set**

- **More text features**: We expanded the rules to check the text match ratio besides edit distance by using [SequenceMatcher](https://towardsdatascience.com/sequencematcher-in-python-6b1e6f3915fc), to make a more complicated and accurate prediction. This is quite connected with [Natural Language Processing](https://en.wikipedia.org/wiki/Natural_language_processing).
- I have labeled 200 more cases and done a logistical regression model for testing if the above rules of prediction work well for a larger set.
	
- **MapReduce**: MapReduce is a programming model. It is composed of a **map** procedure, which conducts filtering and sorting, and a **reduce** method, which conducts a summary operation. 

- Simulation: Reality is recursive. The macro outcome can be often surprising even if we have known the micro behavior well. Simulation methods, especially **agent-based models**, can be used to study the emergence in the complex systems, such as how individual behavior bias can accumulate to the group size difference ([Foote et al., 2020](https://arxiv.org/abs/2006.03119v1)). Simulation can be a promising field and method to address the micro-macro link in social scientific research.

- Hyak: High performance computer cluster at UW. It can be used to conduct large amount of computing.

