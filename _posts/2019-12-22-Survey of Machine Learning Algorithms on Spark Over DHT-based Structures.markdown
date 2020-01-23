---
layout: post
title:  Publishing my first scientific paper
date: 2019-12-22 21:01:00
description: In this first blog post I will share the topic of the first and only (at the moment) paper I published along with some very distinguished and talented professors and colleagues.
---

### Background
<br/>
During my university years (<a href="http://di.ionio.gr/en/" target="blank">Ionian University - Department of Informatics</a>), I was always trying to get my hands dirty with as many parts of Computer Science as possible in order to identify what suits me best. This is the process of elimination and is always working for me. I started or participated in projects varying from computer networks to mobile applications and from cloud computing (my thesis) to big data. 
<br/><br/>
As you can imagine, I chose the winner. Big data always intrigued me and is something I never felt like work. Moreover, working with data is my way to please the curious version of myself and find answers to my questions.
<br/><br/>
All this time, I had the priviledge of meeting and working with very talented people, many of which I still call friends. With a couple of those, we founded a developers team (Ionian Developers Team) where we developed an Android Application (<a href="https://ionio.gr/gr/news/6265/" target="blank">Feedippides</a>) to keep our fellow students (and ourselves) up to date with our class announcements or updates. We were also lab members and researchers of the Information Systems and Databases (ISDLab) Lab of the department. As members of the lab, our professor (and one of my mentors on the field) <a href="https://www.ceid.upatras.gr/en/staff/faculty/sioutas-spyros" target="blank">Dr. Spyros Sioutas</a> proposed the idea of writing a survey and publish it on the 2nd International Workshop on Algorithmic Aspects of Cloud Computing (<a href="https://conferences.au.dk/algo16/algocloud/" target="blank">ALGOCLOUD 2016</a>). In this paper, we had to set up and configure a DHT-based database on a cluster and apply a couple of machine learning algorithms that can run in parallel. Below you can find the title and abstract of the paper and at the end of the post I will provide a link with the full text.

### Survey of Machine Learning Algorithms on Spark Over DHT-based Structures
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

#### Dataset
<br/>
After the installation and configuration of Cassandra in a cluster, and in order to demonstrate the application of popular machine learning algorithms we needed to have a dataset. After a little bit of research, we decided to proceed with Point-Of-Sales (POS) data as we found it very interesting and we could apply different algorithms for a variety of purposes. Below is a sample of the dataset used:
<br/>
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;border-color:black;}
.tg .tg-dvid{font-weight:bold;background-color:#efefef;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-wkkj{font-weight:bold;background-color:#efefef;border-color:inherit;text-align:left;vertical-align:top}
.tg .tg-0pky{border-color:inherit;text-align:left;vertical-align:top}
</style>
<table class="tg" style="width: 100% !important">
  <tr>
    <th class="tg-wkkj">Auto_Inc</th>
    <th class="tg-dvid">Basket_ID</th>
    <th class="tg-dvid">Date</th>
    <th class="tg-dvid">Barcode</th>
    <th class="tg-dvid">Sum_Units</th>
    <th class="tg-dvid">Sum_Value</th>
  </tr>
  <tr>
    <td class="tg-0pky">1</td>
    <td class="tg-0pky">959980460</td>
    <td class="tg-0pky">40938</td>
    <td class="tg-0pky">520121904010</td>
    <td class="tg-0pky">2</td>
    <td class="tg-0pky">12,15</td>
  </tr>
  <tr>
    <td class="tg-0pky">2</td>
    <td class="tg-0pky">959980460</td>
    <td class="tg-0pky">40938</td>
    <td class="tg-0pky">212735100000</td>
    <td class="tg-0pky">1</td>
    <td class="tg-0pky">5</td>
  </tr>
  <tr>
    <td class="tg-0pky">3</td>
    <td class="tg-0pky">959980461</td>
    <td class="tg-0pky">40938</td>
    <td class="tg-0pky">356007034249</td>
    <td class="tg-0pky">1</td>
    <td class="tg-0pky">1,34</td>
  </tr>
  <tr>
    <td class="tg-0pky">4</td>
    <td class="tg-0pky">959980461</td>
    <td class="tg-0pky">40938</td>
    <td class="tg-0pky">520100404062</td>
    <td class="tg-0pky">1</td>
    <td class="tg-0pky">9,50</td>
  </tr>
</table>
<br/>
The Point-Of-Sales data relates to the transactions that have been made in the cash register of a supermarket. Each Basket ID refers to a receipt. The Date ﬁeld represents the date that the transaction (as an integer) has been taken place. The Barcode ﬁeld refers to a unique product number, while Sum Units are the number of units of the given barcode purchased. Also, the Sum Value is the total value of those purchases. It is clear that the Auto Inc ﬁeld represents the record number in Cassandra and the primary key of the table.

#### Machine Learning Algorithms
<br/>
For the experimental case study, we used several Machine Learning Algorithms from Spark’s built-in library MLlib. <a href="https://spark.apache.org/" target="blank">Apache Spark</a> is a widely known open-source Application Programming Interface (API) for cluster computing which provides programmers with the ability to rapidly develop applications using languages like Scala (which is the native language that Spark is written), Java, Python or R in order to process very large datasets. The experiments conducted with some of the most inﬂuential algorithms that have been widely used in the machine learning community; these are Naive Bayes, SVM, K-Means, Expectation Maximization, Association Rules and Parallel FP-Growth. I won't get into details regarding the algorithms and the results as they are described in thoroughly in the paper.
<br/><br/>
If you would like to read the paper, you can follow <a href="https://www.researchgate.net/publication/311910023_Survey_of_machine_learning_algorithms_on_Spark_over_DHT-based_Structures" target="blank">this link</a> to ResearchGate and download the full-text PDF.
<br/><br/>
If you have any questions, feedback or comments, feel free to reach out via mail, LinkedIn or Twitter.