# API Calls

## cordon a node
```
curl -s --request PATCH -H 'Content-type: application/strategic-merge-patch+json' -H "Authorization: Bearer $TOKEN" https://api-server-url:6443/api/v1/nodes/nodename -d @post-data/node-cordon.json
```

## get all pods on node
```
curl -s -H 'Content-type: application/json' -H "Authorization: Bearer $TOKEN" https://api-server-url:6443/api/v1/pods?fieldSelector=spec.nodeName%3Dnodename
```

## post an eviction to a pod
```
curl -s -H 'Content-type: application/json' -H "Authorization: Bearer $TOKEN" https://api-server-url:6443/api/v1/namespaces/namespacename/pods/podname/eviction -d @post-data/eviction.json
```

## get pods
```
curl -s -H 'Content-type: application/json' -H "Authorization: Bearer $TOKEN" https://api-server-url:6443/api/v1/pods
```

## get nodes
```
curl -s -H 'Content-type: application/json' -H "Authorization: Bearer $TOKEN" https://api-server-url:6443/api/v1/nodes
```