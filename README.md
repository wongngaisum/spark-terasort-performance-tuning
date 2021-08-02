# Spark Terasort Performance Tuning
Optimizing Spark TeraSort (20GB data) on a 12‐container kubernetes cluster.

## Cluster configurations
12 k8s containers each with 3 vcores and 5GB of memory, with 1 container as master and the remaining 11 containers as worker nodes. Hadoop YARN is used for resource management.

## Content
1. Shows the Spark configurations you have tested and the achieved sorting times in these experiments. 
2. Make use of Spark UI to analyze why better performace can be achieved when I changed the configuration parameters (e.g., number of executor cores, size of executor memory, number of instances, default parallelism). 
3. Sumarize which parameters (or their combinations) impact the sorting performance most significantly.

## Results
With non-optimized setup, the execution time is ~135s. But with my configutations, the cluster is able to perform TeraSort on 20GB data in 104s.
