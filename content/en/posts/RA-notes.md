---
title: "RA Notes"
date: 2021-08-30T15:31:09+08:00
draft: false
---

**Notes**: This post is written to document the ideas and what I learn from the research assistant work with [Nate](https://teblunthuis.cc). Since the middle of Aug., I began to contribute to the project of Nate which is intended to find the connections between two online communities - [Fandom wiki](https://www.fandom.com/explore) and [Reddit](www.reddit.com). I make a role in the dataset construction.

- Week 1(Aug. 16 - Aug. 22)
	- **Wikidata and SPARQL language**: 
	- **Precision and recall**
- Week 2(Aug. 23 - Aug. 29)
	- **Linux**: 
	- 
- Week 3(Aug. 30 - Sept. 5)
	- **ML Classication**: To find out whether a subreddit and a fandom wiki is really similar or the mapping between them is correct, there can be some ideas from [machine learning classification](https://machinelearningmastery.com/types-of-classification-in-machine-learning/). 
	- **Rules for prediction**: Simpler than real ML classifier, if we give a set of rules to predict the correctnesss of mappings it would also make sense. An example rule Nate gave is:
	````
	The wiki is the top linked wiki from the subreddit AND
	(The subreddit and wiki are linked in wikidata OR
		The subreddit and wiki names are similar OR
		The subreddit-link zscore for the wiki is large
		)
	
	````
	Then we can say their names are similar even they have a low [edit distance](https://en.wikipedia.org/wiki/Edit_distance).
	- Validation Set
