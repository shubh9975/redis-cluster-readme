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
