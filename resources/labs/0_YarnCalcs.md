```
Adjustments made
1. Portion of memmorty set aside for OS is 10% of total RAM. It is too high as the worker node is memory optimized instance with 128GB of RAM.
 Hence adjusting it it for 5% that is factor of .05
```
```
workload factor
  Ideally the number of  mappers/reducers that can be configured for an application to run can be set based on the number of cores available on the cluster.
  Inferring that we are setting aside 1 core is the minimum needed for one slot. In practice we can schedule more than one mapper/reducer per core , in a way loading the node.
  workload factor explain how much manytimes we planned to load each node.
  worload factor 1 implies we planned to run 1 mappers/reduers on each node
  worload factor 2 implies we planned to run 2 mappers/reduers on each node
  worload factor 4 implies we planned to run 4 mappers/reduers on each node
```
	     
