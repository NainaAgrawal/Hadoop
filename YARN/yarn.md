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
