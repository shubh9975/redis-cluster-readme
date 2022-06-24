# redis-cluster package

redis-cluster is an open source object-relational database known for reliability and data integrity. ACID-compliant, it supports foreign keys, joins, views, triggers and stored procedures.

## Configuration Reference
You can configure the following:

## Redis® Cluster Common parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|image.registry|Redis® cluster image registry|string|docker.io|
|image.repository|Redis® cluster image repository|string|bitnami/redis-cluster|
|image.tag|Redis® cluster image tag (immutable tags are recommended)|string|6.2.7-debian-10-r22|
|image.pullPolicy|Redis® cluster image pull policy|string|IfNotPresent|
|image.debug|Enable image debug mode|string|false|
|networkPolicy.enabled|	Enable NetworkPolicy|string|false|
|networkPolicy.allowExternal|The Policy model to apply. Don't require client label for connections|string|true|
|networkPolicy.ingressNSMatchLabels|Allow connections from other namespacess. Just set label for namespace and set label for pods (optional).|string|{}|
|networkPolicy.ingressNSPodMatchLabels|	For other namespaces match by pod labels and namespace labels|tring|{}|
|serviceAccount.create|Specifies whether a ServiceAccount should be created|string|false|
|serviceAccount.create|Specifies whether a ServiceAccount should be created|string|false|
|serviceAccount.name|	The name of the ServiceAccount to create|string|""|
|serviceAccount.annotations|Annotations for Cassandra Service Account|string|{}|
|serviceAccount.automountServiceAccountToken|Automount API credentials for a service account.|string|false|
|rbac.create|Specifies whether RBAC resources should be created|string|false|
|podSecurityContext.enabled|Enable Redis® pod Security Context|string|true|
|podSecurityContext.fsGroup|Group ID for the pods|integer|1001|
|podSecurityContext.runAsUser|User ID for the pods|integer|1001|
|podSecurityContext.runAsNonRoot|"podSecurityContext runAsNonRoot"|string|true|
|podDisruptionBudget|Limits the number of pods of the replicated application that are down simultaneously from voluntary disruptions|string|{}|
|minAvailable|Min number of pods that must still be available after the eviction|string|""|
|maxUnavailable|Max number of pods that can be unavailable after the eviction	|string|""|
|containerSecurityContext.enabled|Enable Containers' Security Context	|string|true|
|containerSecurityContext.runAsUser	|User ID for the containers.|integer|1001|
|containerSecurityContext.runAsNonRoot|Run container as non root|string|true|
|usePassword|Use password authentication|string|true|
|password|Redis® password (ignored if existingSecret set)	|string|""|
|existingSecret	|Name of existing secret object (for password authentication)	|string|""|
|existingSecretPasswordKey|Name of key containing password to be retrieved from the existing secret	|string|""|
|usePasswordFile|Mount passwords as files instead of environment variables	|string|false|
|tls.enabled|Enable TLS support for replication traffic	|string|false|
|tls.authClients| Require clients to authenticate or not	| string |true|
|tls.autoGenerated	|Generate automatically self-signed TLS certificates	|string|false|
|tls.existingSecret	|The name of the existing secret that contains the TLS certificates	|string|""|
|tls.certificatesSecret	|DEPRECATED. Use tls.existingSecret instead	|string|""|
|tls.certFilename	|Certificate filename	|string|""|
|tls.certKeyFilename	|Certificate key filename	|string|""|
|tls.certCAFil|ename	|CA Certificate filename	|string|""|
|tls.dhParamsFilename	|File containing DH params (in order to support DH based ciphers)	|string|""|
|service.ports.redis	|Kubernetes Redis service port|integer|6379|
|service.nodePorts.redis	|Node port for Redis	|string|""|
|service.annotations|Provide any additional annotations which may be required.|string|{}|
|service.labels|Additional labels for redis service|string|string|{}|
|service.type| Service type for default redis service	|string|ClusterIP|
|service.clusterIP	|Service Cluster IP	|string|""|
|service.loadBalancerIP	|Load balancer IP if service.type is LoadBalancer	|string|""|
|service.externalTrafficPolicy	|Service external traffic policy	|string|Cluster|
|service.sessionAffinity	|Session Affinity for Kubernetes service, can be "None" or "ClientIP"	|string|None|
|service.sessionAffinityConfig	|Additional settings for the sessionAffinity	|string|{}|
|persistence.path	|Path to mount the volume at, to use other images Redis® images.	|string|/bitnami/redis/data|
|persistence.subPath	|The subdirectory of the volume to mount to, useful in dev environments and one PV for multiple services	|string|""|
|persistence.storageClass	|Storage class of backing PVC	|string|""|
|persistence.annotations	|Persistent Volume Claim annotations	|string|{}|
|persistence.accessModes	|Persistent Volume Access Modes	|string|["ReadWriteOnce"]|
|persistence.size	|Size of data volume	|string|8Gi|
|persistence.matchLabels	|Persistent Volume selectors	|string|{}|
|persistence.matchExpressions	|matchExpressions Persistent Volume selectors	|string|{}|
|volumePermissions.enabled	|Enable init container that changes volume permissions in the registry (for cases where the default k8s runAsUser and fsUser values do not work)	|string|false|
|volumePermissions.image.registry	|Init container volume-permissions image registry	|string|docker.io|
|volumePermissions.image.repository	|Init container volume-permissions image repository	|string|bitnami/bitnami-shell|
|volumePermissions.image.tag	|Init container volume-permissions image tag	|string|10-debian-10-r431|
|volumePermissions.resources.limits	|The resources limits for the container	|string|{}|
|volumePermissions.resources.requests	|The requested resources for the container	|string|{}|
|podSecurityPolicy.create	|Whether to create a PodSecurityPolicy. WARNING: PodSecurityPolicy is deprecated in Kubernetes v1.21 or later, unavailable in v1.25 or later	|string|false|

