# Hadoop Streaming Python

## Installation
- Docker pull: `docker pull sequenceiq/hadoop-docker`
- Docker run: `docker run -it sequenceiq/hadoop-docker /etc/bootstrap.sh -bash`
- Docker detach from container `ctrl-p + ctrl-q` and attach `docker attach <container-id>`

## Setup
- Copy files to $HADOOP_PREFIX from host to inside container: `docker cp <filename> <container-id>:<$HADOOP_PREFIX>`
- Download streaming jar for hadoop: `curl -O http://central.maven.org/maven2/org/apache/hadoop/hadoop-streaming/2.7.3/hadoop-streaming-2.7.3.jar`

## Run MapReduce
- Command: `bin/hadoop jar hadoop-streaming-2.6.0.jar -file /mapper.py -mapper /mapper.py -file /reducer.py -reducer /reducer.py -input input/ -output output`

## TODO
- Upgrade to use newer syntax in run mapreduce command

## References
- https://github.com/sequenceiq/hadoop-docker
- http://www.michael-noll.com/tutorials/writing-an-hadoop-mapreduce-program-in-python/
 
