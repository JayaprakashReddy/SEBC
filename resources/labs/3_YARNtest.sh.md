```
#!/bin/sh
# Confirm the path values given below correspond to your installation
#HADOOP_MR=/opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce
#HADOOP_PATH=/opt/cloudera/parcels/CDH/bin
HADOOP_MR=/opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/lib/hadoop-mapreduce
HADOOP_PATH=/opt/cloudera/parcels/CDH-5.8.3-1.cdh5.8.3.p0.2/bin

# Mark start of the loop
echo Testing loop started on `date`
maps=$1
echo "mappers=$maps"
reds=$2
echo "reducers=$reds"
mem=$3
echo "memory=$mem"
# Mapper containers
for i in $maps    
do
   # Reducer containers
   for j in $reds 
   do                 
      # Container memory
      for k in $mem 
      do                         
         # Set mapper JVM heap 
         MAP_MB=`echo "($k*0.8)/1" | bc` 

         # Set reducer JVM heap 
         RED_MB=`echo "($k*0.8)/1" | bc` 

        $HADOOP_PATH/hadoop jar $HADOOP_MR/hadoop-mapreduce-examples-*.jar teragen \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     100000 /results/tg-10MB-${i}-${j}-${k} 1>tera_${i}_${j}_${k}.out 2>tera_${i}_${j}_${k}.err                       

       $HADOOP_PATH/hadoop jar $HADOOP_MR/hadoop-mapreduce-examples-*.jar terasort \
                     -Dmapreduce.job.maps=$i \
                     -Dmapreduce.job.reduces=$j \
                     -Dmapreduce.map.memory.mb=$k \
                     -Dmapreduce.map.java.opts.max.heap=$MAP_MB \
                     -Dmapreduce.reduce.memory.mb=$k \
                     -Dmapreduce.reduce.java.opts.max.heap=$RED_MB \
	             /results/tg-10MB-${i}-${j}-${k}  \
                     /results/ts-10MB-${i}-${j}-${k} 1>>tera_${i}_${j}_${k}.out 2>>tera_${i}_${j}_${k}.err                         

        $HADOOP_PATH/hadoop fs -rm -r -skipTrash /results/tg-10MB-${i}-${j}-${k}                         
        $HADOOP_PATH/hadoop fs -rm -r -skipTrash /results/ts-10MB-${i}-${j}-${k}                 
      done
   done
done

echo Testing loop ended on `date`
```