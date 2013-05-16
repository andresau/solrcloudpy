solrcloudpy
===========

solrcloudpy is a python library for interacting with SolrCloud. This library aims to take advantage of the following features of Solr:

* Distributed indexing and searching and transparent failover
* Full JSON api
* Centralized index management
* Near-realtime search

The API is mean to be close to pymongo's API, where one can access collections and databases as simple attributes 

Usage
-------
Solr uses Zookeeper for distributed capabilities, so we will take advantage of that to:

* detect live nodes, 
* remove failing nodes
* find cluster health

Example usage:

     >>> zk = ZConnection("localhost:9983")
     >>> collection = collection.Collection(zk)
     >>> collection.create('test1')
     >>> print collection.test1.search(q='')
     ...

 
