# Awesome Data Structures in Open Source [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A list of data structures used in Open Source projects in various languages and projects around the web. This list is primarily intended for students/developers who want to see real-world usage of various data structures, being used in production code. It is also intended for experienced developers and contributers whose deep knowledge of OSS projects would help students and beginning developers around the world get a feel for raw code, and how theory translates into practice.

All languages, frameworks, and libraries are included, as long as the link demonstrates usage/declaration of a data structure in an open source project.

## Contributing To This List

Please ensure your pull request adheres to the following guidelines:

- Make an individual pull request for each suggestion.
- Add some description of the data structure used in the context of the project.
- New categories or improvements to the existing categorization are welcome!

Thank you for sharing your hard-earned knowledge!


## Hash Tables

- [Wget](http://www.gnu.org/software/wget/)
	- Used for [cookie storage](http://bzr.savannah.gnu.org/lh/wget/trunk/annotate/head:/src/cookies.c#L61). See the [header file here](http://bzr.savannah.gnu.org/lh/wget/trunk/annotate/head:/src/hash.h)
	
- [PostgreSQL](http://www.postgresql.org/)
	- PostgreSQL uses [dynamic hashing tables](https://github.com/postgres/postgres/blob/master/src/backend/utils/hash/dynahash.c). Read [all about them here](https://github.com/postgres/postgres/blob/master/src/backend/access/hash/README).

- [Git](https://git-scm.com/)
	- The version control system Git uses hashmaps and hashtables internally ([Documentation](https://github.com/git/git/blob/master/Documentation/technical/api-hashmap.txt)) ([header](https://github.com/git/git/blob/master/hashmap.h) and [main](https://github.com/git/git/blob/master/hashmap.h)). Hashmaps are used in [caches](https://github.com/git/git/blob/master/cache.h#L116), [file name hashes](https://github.com/git/git/blob/master/name-hash.c) etc.

- [MySQL](http://www.mysql.com/)
	- MySQL uses hash structure to store records - see the [header](https://github.com/mysql/mysql-server/blob/a2757a60a7527407d08115e44e889a25f22c96c6/include/hash.h#L62).

- [Recutils](https://www.gnu.org/software/recutils/)
	- [Base memory table](https://github.com/sidthekidder/recutils/blob/master/src/rec.h#L49) for storing any element. 

## Trees

- [PostgreSQL](http://www.postgresql.org/)
	- Red Black trees are used for fast storage of data in the core database engine. See the [header file](https://github.com/postgres/postgres/blob/master/src/include/lib/rbtree.h) and [main file](https://github.com/postgres/postgres/blob/master/src/backend/lib/rbtree.c).

- [RethinkDB](http://rethinkdb.com/)
	- Every RethinkDB table is represented as a B-tree. An [internal node](https://github.com/rethinkdb/rethinkdb/blob/next/src/btree/node.hpp#L45)/[leaf node](https://github.com/rethinkdb/rethinkdb/blob/next/src/btree/leaf_node.hpp#L42) are the basic structures used (page caches are used to store the blocks of the B-tree) where each node can have multiple children represented by offsets.

- [Git](https://git-scm.com/)
	- Git has many uses for [trees](https://github.com/git/git/blob/master/tree.h) - [cache trees](https://github.com/git/git/blob/master/cache-tree.h) etc

- [MySQL](http://www.mysql.com/)
	- Red Black trees are used in its InnoDB storage engine, for indexing primary tables. See the [header](https://github.com/mysql/mysql-server/blob/09ddec8757b57893ccd2f2c2482b3eec5ca811e5/storage/innobase/include/ut0rbt.h#L58) and [implementation](https://github.com/mysql/mysql-server/blob/09ddec8757b57893ccd2f2c2482b3eec5ca811e5/storage/innobase/ut/ut0rbt.cc#L31)

- [Apache Spark](http://spark.apache.org/)
	- Apache Spark uses decision trees for classification and regression. Grok the [readme here](http://spark.apache.org/docs/latest/mllib-decision-tree.html) and see the [actual implementation here](https://github.com/apache/spark/blob/master/mllib/src/main/scala/org/apache/spark/ml/tree/Node.scala#L108).

- [D3.js](http://d3js.org/)
	- This popular visualization library for javascript uses red-black trees for Voronoi geometry. [See its implementation here](https://github.com/mbostock/d3/blob/master/src/geom/voronoi/red-black.js).

- [vamonos](https://github.com/rosulek/vamonos)
	- This visualization library [uses binary trees in Coffeescript](https://github.com/rosulek/vamonos/blob/master/src/data-structure/binarytree.coffee) for visualization of algorithms. 

## Heaps

- [PostgreSQL](http://www.postgresql.org/)
	- PostgreSQL uses [Binary Heaps](https://en.wikipedia.org/wiki/Binary_heap) [ see [header](https://github.com/postgres/postgres/blob/master/src/include/lib/binaryheap.h) and [main](https://github.com/postgres/postgres/blob/master/src/backend/lib/binaryheap.c) ] and [Pairing-Heaps](https://en.wikipedia.org/wiki/Pairing_heap) [ see [header](https://github.com/postgres/postgres/blob/master/src/include/lib/pairingheap.h) and [main](https://github.com/postgres/postgres/blob/master/src/backend/lib/pairingheap.c) ]. 

## Queues

- [MySQL](http://www.mysql.com/)
	- A [priority-queue](https://github.com/mysql/mysql-server/blob/09ddec8757b57893ccd2f2c2482b3eec5ca811e5/include/priority_queue.h#L35) is used by MySQL, the [base queue implementation](https://github.com/mysql/mysql-server/blob/09ddec8757b57893ccd2f2c2482b3eec5ca811e5/include/queues.h#L19) of which is straight from the textbook - [implementation](https://github.com/mysql/mysql-server/blob/a2757a60a7527407d08115e44e889a25f22c96c6/mysys/queues.c#L16).
	


### License

[![Creative Commons License](http://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
