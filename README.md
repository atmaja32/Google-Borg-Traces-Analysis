# Google-Borg-Traces-Analysis

A Google cluster is a set of machines, packed into physical enclosures, and
connected by a high-bandwidth cluster network. A cell is a set of machines, typically
all in a single cluster, that share a common cluster-management system that
allocates work to machines.A single usage trace describes several days of the workload on a single
Borg cell. A trace is made up of several tables, each indexed by a primary key that
typically includes a timestamp. The data in the tables is derived from information
provided by the cell's management system and the individual machines in the cell. 

Analyzing the Google cluster manager Borg dataset helps us understand about the
resource usage and requirements of a trace. Analyses of job duration, duration for
each event/state transition, distribution of jobs, resource requests in terms of CPU
and memory usage, type of resource request: job or alloc_set, job loads at each
cluster etc. will lead to some very helpful insights. These insights can help us draw
useful conclusions about machines, jobs, tasks and resource usage and in turn would
aid in better allocation and management of resources.

Our objective is to analyze Borg Cluster data to observe:

1. Distribution of jobs across clusters
2. Time taken to transition states.
3. Frequency of jobs failing/succeeding at the end of their life cycles.
4. Memory consumption of jobs across clusters
5. Predict request success or failure and event or state of trace using applicable
features.
