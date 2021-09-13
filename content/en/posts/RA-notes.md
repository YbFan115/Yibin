---
title: "RA Notes"
date: 2021-08-30T15:31:09+08:00
draft: false
---

**Notes**: This post is written to keep the ideas alive and document what I learn from the research work with [Nate](https://teblunthuis.cc). Since Aug. 2021, I began to contribute to the project of Nate which is intended to find the connections between two online communities - [Fandom wiki](https://www.fandom.com/explore) (which was previously known as Wikia) and [Reddit](www.reddit.com). I make a role in the dataset construction.

### Week 1(Aug. 16 - Aug. 22)
	- **Wikidata and SPARQL language**: 
	- **Precision and recall**: 
### Week 2(Aug. 23 - Aug. 29)
	- **Linux**: To be more efficient to collaborate, I set the Linux and began to join the git of [Community Data Science Collective](https://wiki.communitydata.science/Main_Page), which is a research group focused on online communities. 
		- use `explorer.exe .` to find the Linux files in Windows
		- if `sudo apt install ...` fails, it can probably be solved by `sudo apt install -y ... --fix-missing`(see in [Help Docs](https://help.aliyun.com/knowledge_detail/41205.html?spm=a2c6h.13066369.0.0.21837b3ejhCgyA)) 
		- to find the ip for linux, use `ifconfig -a`
		- to open xrdp, use `sudo service xrdp restart`
	- **Wikidata**: According to the query outcome in Wikidata, it seems like dataset in Wikidata does not have a good coverage for the match between a fandom wiki and a subreddit, but include almost no error due to the properties for Wikipedia. Due to this property, 

### Week 3(Aug. 30 - Sept. 5)
	- **ML Classification**: To find out whether a subreddit and a fandom wiki is really similar or the mapping between them is correct, there can be some ideas from [machine learning classification](https://machinelearningmastery.com/types-of-classification-in-machine-learning/). 
	- **Rules for prediction**: Simpler than real ML classifier, if we give a set of rules to predict the correctnesss of mappings it would also make sense. An example rule Nate gave is:
	
	```
	The wiki is the top linked wiki from the subreddit AND
	(The subreddit and wiki are linked in wikidata OR
		The subreddit and wiki names are similar OR
		The subreddit-link zscore for the wiki is large
		)
	````

	Then we can say their names are similar even they have a low [edit distance](https://en.wikipedia.org/wiki/Edit_distance).
	- Validation Set
	- **More text features**: We expanded the rules to check the text match ratio besides edit distance by using [SequenceMatcher](https://towardsdatascience.com/sequencematcher-in-python-6b1e6f3915fc), to make a more complicated and accurate prediction. This is quite connected with [Natural Language Processing](https://en.wikipedia.org/wiki/Natural_language_processing).
	- I have labeled 200 more cases and done a logistical regression model for testing if the above rules of prediction work well for a larger set.
	

### Week 4（Sept. 6 - Sept. 12)

