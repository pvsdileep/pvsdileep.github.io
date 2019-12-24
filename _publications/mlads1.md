---
title: "Clustering labels through community detection on co-occurrence graphs."
collection: publications
permalink: /publication/mlads1
excerpt: 'Items are often characterized with sets of labes; for example, articles in a database might be tagged with several keywords per article. Here we illustrate a simple approach to clustering items based on counting occurrences of such tags. The approach can be generalized to a variety of applications; for example, web pages can be compared based on which other pages link to them, or we can find edges between items appearing together in market baskets. We discussed ways in which we are using this approach to cluster related items and discover functional relationships form a variety of loosely structred data sources.'
date: 06-09-2019
venue: 'Machine Learning, AI & Data Science Conference - Microsoft'
//paperurl: 'https://link.springer.com/article/10.1007/s13042-014-0309-2'
//citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---
Our demonstration example uses sets of tags extracted from StackOverflow posts. The tags are labels from a large defined vocabulary covering computer science topics like languages and frameworks, and each post has been tagged with a set of these labels. We start by arranging this data into a table with columns for post and tag. After filtering out rare tags, we generate a graph where the nodes are tag labels, and the edges show the fraction of article having the tag from the source node that also have the tag from the destination node. The edges are directed because weights depend on the direction of the connection; for example, 52% of posts tagged with 'tensorflow' are also tagged with 'python', but only a small fraction of all Python posts are tagged with tensorflow. Now that we have a graph, we can use community detection to put the nodes into clusters: here are the groups obtained by clustering the StackOverflow tags using the Louvain algorithm for maximum modularity.
