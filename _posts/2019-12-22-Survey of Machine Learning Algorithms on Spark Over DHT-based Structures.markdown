---
layout: post
title:  Survey of Machine Learning Algorithms on Spark Over DHT-based Structures
date: 2019-12-22 21:01:00
description: In this first blog post I will share the topic of the first and only (at the moment) paper I published along with some very distinguished and talented professors and colleagues.
---

### Background
<br/>
During my university years (<a href="http://di.ionio.gr/en/" target="blank">Ionian University - Department of Informatics</a>), I was always trying to get my hands dirty with as many parts of Computer Science as possible in order to identify what suits me best. This is the process of elimination and is always working for me. I started or participated in projects varying from computer networks to mobile applications and from cloud computing (my thesis) to big data. 
<br/><br/>
As you can imagine, I chose the winner. Big data always intrigued me and is something I never felt like work. Moreover, working with data is my way to please the curious version of myself and find answers to my questions.
<br/><br/>
All this time, I had the priviledge of meeting and working with very talented people, many of which I still call friends. With a couple of those, we founded a developers team (Ionian Developers Team) where we developed an Android Application (<a href="https://ionio.gr/gr/news/6265/" target="blank">Feedippides</a>) to keep our fellow students (and ourselves) up to date with our class announcements or updates. We were also lab members and researchers of the Information Systems and Databases (ISDLab) Lab of the department. As members of the lab, our professor (and one of my mentors on the field) <a href="https://www.ceid.upatras.gr/en/staff/faculty/sioutas-spyros" target="blank">Dr. Spyros Sioutas</a> proposed the idea of writing a survey and publish it on the 2nd International Workshop on Algorithmic Aspects of Cloud Computing (<a href="https://conferences.au.dk/algo16/algocloud/" target="blank">ALGOCLOUD 2016</a>). In this paper, we had to set up and configure a DHT-based database on a cluster and apply a couple of machine learning algorithms that can run in parallel. Below you can find the abstract of the paper and at the end of the post I will provide a link with the full text of the paper.

### Abstract
<br/>
Several solutions have been proposed over the past few years on data storage, data management as well as data retrieval systems. These solutions can process massive amount of data stored in relational or distributed database management systems. In addition, decision making analytics and predictive computational statistics are some of the most common and well studied fields in computer science. In this paper, we demonstrate the implementation of machine learning algorithms over an open-source distributed database management system that can run in parallel on a cluster. In order to accomplish that, a system architecture scheme (e.g. Apache Spark) over Apache Cassandra is proposed. This paper also presents a survey of the most common machine learning algorithms and the results of the experiments performed over a Point-Of-Sales (POS) data set.

### What is a DHT-based structure and why we chose it?
<br/>
Instead of trying to explain what is a DHT-based structure, I will first provide a very well written description from <a href="https://en.wikipedia.org/wiki/Distributed_hash_table" target="blank">Wikipedia</a>.
<br/>
<blockquote>
A distributed hash table (DHT) is a distributed system that provides a lookup service similar to a hash table: (key, value) pairs are stored in a DHT, and any participating node can efficiently retrieve the value associated with a given key. The main advantage of a DHT is that nodes can be added/removed with minimum work around re-distributing keys. Keys are unique identifiers which map to particular values, which in turn can be anything from addresses, to documents, to arbitrary data. Responsibility for maintaining the mapping from keys to values is distributed among the nodes, in such a way that a change in the set of participants causes a minimal amount of disruption. This allows a DHT to scale to extremely large numbers of nodes and to handle continual node arrivals, departures, and failures.
</blockquote>

<div class="img_row">
	<img class="col three" src="/img/post_1/DHT.svg">
</div>
<br/>
DHT structures are mainly motivated from peer-to-peer systems (e.g. BitTorrent, Napster etc.) because of its decentralized nature and scalability capabilities and today, one of the most popular implementations of a DHT-based database system is <a href="http://cassandra.apache.org/" target="blank">Apache Cassandra</a>. Cassandra initially developed at Facebook by Avinash Lakshman, one of the authors of Amazon's Dynamo, and Prashant Malik to power the Facebook inbox search feature.
<br/><br/>
Besides Cassandra's applicability for our project, its popularity and proven performance, we also chose to use it because of its very well written documentation and the community behind it as this made the installation and configuration more simple. 

### Machine Learning Algorithms and experimental results

<br/>

<br/>

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/img/post_1/9.jpg">
</div>
<div class="col three caption">
	A simple, elegant caption looks good between image rows, after each row, or doesn't have to be there at all. 
</div>
<div class="img_row">
	<img class="col two" src="/img/post_1/8.jpg">
	<img class="col one" src="/img/post_1/10.jpg">
</div>

Slow-carb four dollar toast Helvetica pop-up. Kale chips next level literally trust fund Pitchfork. Jean shorts Pinterest beard, farm-to-table irony craft beer swag tofu 8-bit Banksy. Quinoa forage fanny pack, pug hashtag Echo Park heirloom Schlitz tote bag artisan Neutra mumblecore 90's shabby chic raw denim.


<div class="img_row">
	<img class="col one" src="/img/post_1/11.jpg">
	<img class="col one" src="/img/post_1/12.jpg">
	<img class="col one" src="/img/post_1/7.jpg">
</div>
