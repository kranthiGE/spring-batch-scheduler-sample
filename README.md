# spring-batch-scheduler-sample
Sample batch with boot and scheduler

### how to register this job in SCDF (Spring cloud Data Flow)
- The SCDF web UI can be seen at http://localhost:9393/dashboard/index.html#/apps/apps
- Register the app
 ``app register --name spring-batch-scheduler-sample --type task --uri maven://com:spring-batch-scheduler-sample:jar:0.1.0``
- Create the task and point to above registered job
 ``task create testjob --definition spring-batch-scheduler-sample``
- Copy the spring-batch-scheduler-sample.jar into ~/.m2/Users/kirankranthi/.m2/repository/com/spring-batch-scheduler-sample so that the jar is added to your local maven repository
- You can use below command to verify the added tasks
 ``task list``
- You can start the job either through SCDF Web UI or via shell
``task launch testjob``

