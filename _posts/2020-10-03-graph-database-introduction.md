---
layout: post
title:  "Introduction to Graph Database"
author: Pahul Preet Singh Kohli
categories: [Graph Database, Data Management, Triple Stores, RDF, Resource Description Framework, Property Graph, Hypergraph] 
image: assets/images/graphdatabase.jpeg
description: "Graph Database are increasingly being adopted in various industries, such as healthcare, retail, financial services, given their ability to represent data from the real world and help to analyse various data relationships. Graph Database is a NoSQL database which uses nodes to store data entities, and edges to store relationships between the entities."
comments: false
---


Graph Database are increasingly being adopted in various industries, such as healthcare, retail, financial services, given their ability to represent data from the real world and help to analyse various data relationships.

**Graph Database** is a NoSQL database which uses nodes to store data entities, and edges to store relationships between the entities.

  

## Types of Graph Databases

  

### True Graph Database / Property Graphs
    

-   Support property graphs in which the properties may be assigned to either entities or their relationships, or both.
    
-   They support index free adjacency, we can traverse a graph without needing an index.
    

![](https://lh5.googleusercontent.com/rN1n3-Zj_pDKrzOzFuWMwUrP3NgaGqvE_tNJWb0Hz3yIXW2TRhuVOKIM1605nwBPZYQyqMiAB0zzyNZOfJzYBbrtr1vh2NbQhOUE2Wp3d9b62rzThifn3AAUBVVU5ZUT6xQPfyXD)


-   In property graphs
    
	
	-   **Nodes**
	    
	
		-   Represents entities / objects in the graph.
		    
		-   Can contain properties (i.e., key-value pairs) and be labeled with one or more labels.
		    

	-   **Relationships**
	    
	
		-   Represents the named relationships between different entities.
		    
		-   Can contain properties (i.e., key-value pairs) and are directional (definite start and end node).
	    

  

-   True Graph Database / Property Graphs based database services:
    
	
	-   [Neo4j](https://neo4j.com/)
	    
	-   [AWS Neptune](https://aws.amazon.com/neptune/)
	    

  
  

### Triple Stores / RDF (Resource Description Framework) database
    

-   Stores data in a format known as a triple of subject-predicate-object data structure.
    
-   Data is logically linked in Triple Stores.
    

  

![](https://lh5.googleusercontent.com/m4ymdIyFModi1-oO_ixqfgTo4nS5wLElzFs9bLlGqDIurcjGoxNgNQpg6--ZJ4Gl6q5X7N3aSMAjb8TQZNd2JjI7EO-VKi_dVMXNGUogpF2L6Gc0VxEPLuM_KeGrU2tY6GplkBsd)

-   They don’t support index free adjacency.
    
-   Triple Stores / RDF (Resource Description Framework) based database services:
    
	
	-   [AllegroGraph](https://franz.com/agraph/allegrograph/)
	    
	-   [GraphDB](http://graphdb.ontotext.com/graphdb/)
	    

  
### Hypergraph Database
    

-   Useful for modelling many to many relationships.
    
-   In this type of graph based database, the relationship is called as Hyperedge which allows any number of nodes at either end of a relationship.
    

![](https://lh3.googleusercontent.com/mGTY3hCzvxC6q41Xwm_L0d15aGnPVWOK0TyFyj9wWKcjWacZmkOr8bGycgZirspjoW0pSAE-JHy7BHgvwKlW-Y1B4CdjckhIzoGeddf9obud7eKmlWhyaFkTB_VUDxvhr1vO4Rm6)

-   Hypergraphs are more generalizable and are multidimensional.
    
-   Property Graph and Hypergraph Graph are isomorphic, that is Property Graph can be represented by Hypergraph but the reverse isn’t possible.
    
-   Hypergraphs based database services:
	    

	-   [HyperGraphDB](http://www.hypergraphdb.org/)
	    

  

### Advantages of Graph Databases

-   The query speed for graph databases depends only on the number of concrete relationships and not on the total amount of data in the database.
    
-   The graph databases are easily able to represent real world data relationships and hierarchies.
    
-   The graph database representation is flexible and follows agile structures. The data entities definitions and the relationship definitions can be altered dynamically.
    

  

### Disadvantages of Graph Databases

-   Each graph database provider has specified a specific syntax or language for updates and queries. Therefore, there is no standard query language that works for every graph database.
    
-   Difficult to scale,as graph database are designed as a single-tier architecture.
    

  

### References

-   [https://www.itworldcanada.com/blog/a-quick-primer-on-graph-databases/434215](https://www.itworldcanada.com/blog/a-quick-primer-on-graph-databases/434215)
    
-   [https://www.bloorresearch.com/technology/graph-databases/](https://www.bloorresearch.com/technology/graph-databases/)
    
-   [https://www.eweek.com/database/why-experts-see-graph-databases-headed-to-mainstream-use](https://www.eweek.com/database/why-experts-see-graph-databases-headed-to-mainstream-use)
    
-   [https://whatis.techtarget.com/definition/graph-database](https://whatis.techtarget.com/definition/graph-database)
    
-   [https://neo4j.com/blog/other-graph-database-technologies/](https://neo4j.com/blog/other-graph-database-technologies/)
    
-   [https://towardsdatascience.com/graph-databases-whats-the-big-deal-ec310b1bc0ed](https://towardsdatascience.com/graph-databases-whats-the-big-deal-ec310b1bc0ed)
    
-   [https://simplea.com/Articles/what-is-a-graph-database](https://simplea.com/Articles/what-is-a-graph-database)
    
-   [https://neo4j.com/use-cases/](https://neo4j.com/use-cases/)
