# oozie
I am talking here about oozie as a component running Cloudera Manager Cluster (CDH v6.6.)
Let us check a use case we need to apply:
    we have spark jobs that need to be run scheduled every hour on an hdfs cluster
    
This is normally done using spark-submit command on crontab but this hard to maintaing and monitor the execution of the crontab itself, so oozie here to provide such facilities. OOzie to achieve this it consists mainly of the following components:
1. WorkFlow: this a descriptive flow that defines the steps of execution of multiple tasks not just one task. So spark job here represent an action, so the workflow can execute multiple actions that flows from Step to another and an be conditioned like UML diagarams with conditions to go in this path or not. All those actions are controlled with controls like start, end and kill :). so the workflow represent a wider concept 
2. Coordinator 
