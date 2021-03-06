---
layout: post  
title: Knowledge Graph
categories: [Knowledge Graph ]  
tags: [Knowledge_graph]  
description: 「介绍knowledge graph」   
---

本文介绍什么是知识图谱

## [维基百科（译）](https://en.wikipedia.org/wiki/Knowledge_Graph)

知识图谱是谷歌用来增强其搜索结果而使用的一个知识库。谷歌于2012年开始将知识图谱加入到它的搜索引擎中。知识图谱可以为某一主题提供详细的、结构化的信息，而不仅仅是提供一系列的链接。这样用户就可以直接获得所查询的信息，而不再需要自己通过点击各个链接来获取所需的信息。知识图谱提供的简短摘要常常被谷歌用作Google Now的回复。

## 知识图谱的组织形式
知识图谱通常被表现为网络的形式，其中节点表示实体，边表示实体间的关系。

实体（entity）是指现实世界中的事物。比如篮球运动员“姚明”，比如“运动员”，比如“桌子”等等。

关系（relation）就是指两个实体之间存在的关联。比如“姚明”和“运动员”之间的关系是“职业”。知识图谱中的关系都是二元关系，也就是两个实体之间的关系。

通常来说，两个实体和关系之间是存在方向的，比如我们可以说“姚明”和“运动员”之间的关系是“职业”，但是不能说“运动员”和“姚明”之间的关系是“职业”。所以我们也把前面的那个实体称为头实体，后面的那个实体称为尾实体。

## 知识图谱的存储形式
对于数据的存储我们有很多种方法。我们可以以文本的形式存储，比如本文; 我们也可以用表格的形式存储，比如excel表和很多数据库。那么我们如何来存储知识图谱呢？

前面我们说了，知识图谱常常表示为网络的形式，我们能否以网络的形式保存呢？理论上是可以的，但是这样需要专门设计网络（图）的存储算法，比较麻烦。

现在流行的存储知识图谱的方法是将知识图谱表示为三元组的形式。所谓三元组就是（头实体，关系，尾实体）这样的形式。我们可以把一个任意大小的知识图谱切割成若干个三元组，然后按照每行一个三元组的约定（也可以按照别的约定），有多少个三元组就写多少行，这样就可以把一个知识库存储在一个普通的文件中了。

现实生活中，常常会存在不同的事物叫同一个名字的情况。因为在现实生活中这些名字的出现常常会伴随着上下文，通过这些上下文我们可以很容易区分具体指的是什么，所以不容易产生歧义。但是在知识图谱中，每一条三元组表示了一个确定的事实，如果同一个名字表示不同的实体，必然会产生歧义。因此在实际构建知识图谱时，并不是直接用“姚明”这样的名字来表示一个实体，而是对每一个实体分配一个唯一的ID，这样就能解决歧义的问题了。下面是某个知识图谱的文本形式的一部分。
<center>
	<p><img src="https://raw.githubusercontent.com/xiangrongzeng/xiangrongzeng.github.io/master/_posts/graph/sample_of_knowledge_graph.jpg" align="center"></p>
</center>

## 常用的知识图谱
> [Freebase](https://developers.google.com/freebase/) 通过社区成员协作，从许多源抽取而来。

> [Depedia](http://wiki.dbpedia.org/) 从维基百科的结构化信息中抽取而来。

> [Yago](https://datahub.io/dataset/yago) 从维基百科和其它资源中自动抽取而来。