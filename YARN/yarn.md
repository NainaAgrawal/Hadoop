**Yarn**: Yet Another Resource Negotiator.

In MR 2 yarn was introduced. It is the cluster resource mgt layer of hadoop. Even Mr has to communicated with yarn to get any tasks done.

Two daemons were introduced in this phase:
1. **Resource Manager** : It is the Master daemon it runs on master machine.
  -- To which all the jobs are submitted from the client.
  -- It is one which allocates all cluster level resources for executing a job.
  -- It has two components a scheduler and an application Manager.
 
2. **Node Manager** : It is daemon that works on data/slave node with data node proceses.
  --It monitors resources of a particular data node.
  
**Processes**
  
-**Job History Server**: ddd
It is someone who keeps the track of all the jobs that have been submitted or executed over the cluster.
It also keeps track of the status.
It also keeps the log files of every execution happened over the hadoop cluster.

-**Application Master**
It is a process that is executed on node machine/slave machine created by a resource manager to execute and manage a job.
It is the one which negotiates the resources from the resource manager and finally coordinates with the node manager to execute the job.

-**Container**
It is created by the node manager itself which has been allocted by resource manager, within the container all the jobs are executed.

• Viewing running applications: yarn application –list

• To view all applications independently on their current state we
  can use:
  yarn application -list -appStates ALL
  In place of “ALL” you can use: NEW, NEW_SAVING, SUBMITTED, ACCEPTED, RUNNING,
  FINISHED, FAILED, KILLED

• To view the info of a specific app: yarn application -status <App ID>

• To forcibly terminate an application you can use:
  yarn application -kill <AppID>
  
• You can also view the log file for an application:
  yarn logs -applicationId <AppID>
  yarn logs -applicationId <AppID> | less (scrollable list)
