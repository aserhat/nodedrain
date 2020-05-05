# nodedrain
Bash implementation of the mechanics behind the kubectl drain command.

## Setup
A service account with the correct RBAC to access all pods in all namespaces as well as nodes.  For this demo, I am using the default service account in the default namespace.  You can adjust the service account and API server URL in the script variables.

## Usage
```
./nodedrain [nodename]
```
