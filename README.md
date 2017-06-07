
/*

Author : Logothetis Fragkoulis
ECE
Electrical and Computer Engineer
*/



During the last decades, data management and storage have become increasingly distributed. Advanced query operators, such as 
skyline queries, have become, not just useful, but indispensable, in order to help users handle the huge amount of available
data by identifying a set of interesting data objects. Space partition techniques, such as recursive division of the data space,
have been used for skyline query processing in centralized, parallel and distributed settings. Unfortunately, such grid-based 
partitioning is not suitable in the case of a parallel skyline query, where all partitions are examined simultaneously,
since many data partitions do not contribute to the overall skyline set, resulting in a lot of redundant processing.
This thesis focuses on studying the design, development and comparison of two algorithms to parallel skyline query computation. 
The presented implementation is based on the Map-Reduce model and its open-source implementation, Hadoop, using space partitioning 
techniques that were introduced earlier in a parallelizable way over the MapReduce model of computation, in one step. 
A set of experiments will be demonstrated that will show that these techniques are suitable for skyline query processing in
parallel architectures. A comparative performance analysis for the two algorithms used, will also be provided. As it will be 
demonstrated by experimental studies, these techniques are an eﬃcient and scalable solution for skyline query processing in 
parallel environments.


Even before the introduction of skyline queries into database research, 
the problem of making interesting decisions was known as the maximum vector problem
or the Pareto [1] optimum. In recent years, skyline query processing has become an important issue 
in database research. The popularity of the skyline operator is mainly due to its applicability on decision
making applications. In such applications, the database tuples are represented as a set of multidimensional 
data points and the skyline set contains those particular points which present the best trade-oﬀs between the 
diﬀerent dimensions. For example, consider a database that contains information about recreational establishments, such as hotels. 
Each tuple of the database is represented as a point in a data space consisting of numerous dimensions. In the presented example,
the y-dimension represents the price of a room, whereas the x-dimension captures the distance of the hotel to a certain point of 
interest such as a particular beach. According to the dominance deﬁnition, a hotel will dominate another hotel because it will be
cheaper and closer to the beach. Thus, the skyline points are the best possible trade-oﬀs between price and distance from the beach.
