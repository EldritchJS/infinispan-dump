# infinispan-dump 

Periodically dump contents of Infinispan cache

## Quickstart on cluster

### CheckCache test class

1. Start test
```
oc new-app --allow-missing-imagestream-tags \
	-l app=infinispan-dump \
	--image-stream=<PROJECT NAMESPACE>/redhat-openjdk18-openshift:1.2 \
	https://github.com/eldritchjs/infinispan-dump
```
2. Check pod log for output either via web console or the following, as data is published to equoid, the top-k entries should change accordingly:
```
oc logs <infinispan-dump pod ID> -n equoid
```

