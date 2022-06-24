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


### Redis® statefulset parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|redis|redis-port|redis-port|string|6379|
|redis.containerPorts.redis	|Redis® port	|integer|6379|
|redis.containerPorts.bus	|The busPort should be obtained adding 10000 to the redisPort. By default: 10000 + 6379 = 16379	|string|integer|16379|
|livenessProbe.initialDelaySeconds|Initial delay seconds for livenessProbe	|integer|5|
|livenessProbe.periodSeconds|Period seconds for livenessProbe	|integer|5|
|livenessProbe.timeoutSeconds|Timeout seconds for livenessProbe	|integer|5|
|livenessProbe.failureThreshold|Failure threshold for livenessProbe	|integer|5|
|livenessProbe.successThreshold|Success threshold for livenessProbe	|integer|1|
|readinessProbe.initialDelaySeconds|Initial delay seconds for readinessProbe	|integer|5|
|readinessProbe.periodSeconds|Period seconds for readinessProbe	|integer|5|
|readinessProbe.timeoutSeconds|Timeout seconds for readinessProbe	|integer|1|
|readinessProbe.failureThreshold|Failure threshold for readinessProbe	|integer|5|
|readinessProbe.successThreshold|Success threshold for readinessProbe	|integer|1|


### Cluster update job parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|updateJob.activeDeadlineSeconds	|Number of seconds the Job to create the cluster will be waiting for the Nodes to be ready.	|integer|600|
|updateJob.annotations	|Job annotations	|string|{}|
|updateJob.podAnnotations	|Job pod annotations	|string|{}|
|updateJob.podLabels	|Pod extra labels	|string|{}|
|updateJob.extraEnvVars	|An array to add extra environment variables	|string|[]|
|updateJob.extraEnvVarsSecret	|Secret containing extra environment variables	|string|""|
|updateJob.podAffinityPreset	|Update job pod affinity preset. Ignored if updateJob.affinity is set. Allowed values: soft or hard	|string|""|
|updateJob.podAntiAffinityPreset	|Update job pod anti-affinity preset. Ignored if updateJob.affinity is set. Allowed values: soft or hard	|string|soft|
|updateJob.nodeAffinityPreset.type	|Update job node affinity preset type. Ignored if updateJob.affinity is set. Allowed values: soft or hard	|string|""|
|updateJob.nodeAffinityPreset.key	|Update job node label key to match Ignored if updateJob.affinity is set.	|string|""|
|updateJob.affinity	|Affinity for update job pods assignment	|string|{}|
|updateJob.nodeSelector	|Node labels for update job pods assignment	|string|{}|
|updateJob.priorityClassName	|Priority class name	|string|""|
|updateJob.resources.limits	|The resources limits for the container	|string|{}|
|updateJob.resources.requests	|The requested resources for the container	|string|{}|

### Cluster management parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|cluster.init	|Enable the initialization of the Redis® Cluster	|string|true|
|cluster.nodes	|The number of master nodes should always be >= 3, otherwise cluster creation will fail	|integer|6|
|cluster.replicas	|Number of replicas for every master in the cluster	|integer|1|
|cluster.externalAccess.enabled	|Enable access to the Redis	|string|false|
|cluster.update.addNodes	|Boolean to specify if you want to add nodes after the upgrade	|string|false|
|cluster.update.currentNumberOfNodes	|Number of currently deployed Redis® nodes	|integer|6|
|cluster.update.currentNumberOfReplicas	|Number of currently deployed Redis® replicas	|integer|1|


### Metrics sidecar parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|metrics.enabled	|Start a side-car prometheus exporter	|string|false|
|metrics.image.registry	|Redis® exporter image registry	|string|docker.io|
|metrics.image.repository	|Redis® exporter image name	|string|bitnami/redis-exporter|
|metrics.image.tag	|Redis® exporter image tag	|string|1.37.0-debian-10-r62|
|metrics.image.pullPolicy	|Redis® exporter image pull policy	|string|IfNotPresent|
|metrics.resources	|Metrics exporter resource requests and limits	|string|{}|
|metrics.extraArgs	|Extra arguments for the binary; possible values [here](https://github.com/oliver006/redis_exporter	|string|{}|
|metrics.podAnnotations	|Additional annotations for Metrics exporter pod	|string|{}|
|metrics.podLabels	|Additional labels for Metrics exporter pod	|string|{}|
|metrics.serviceMonitor.enabled	|If true, creates a Prometheus Operator ServiceMonitor (also requires metrics.enabled to be true)	|string|false|
|metrics.serviceMonitor.namespace	|Optional namespace which Prometheus is running in	|string|""|
|metrics.serviceMonitor.interval	|How frequently to scrape metrics (use by default, falling back to Prometheus' default)	|string|""|
|metrics.serviceMonitor.scrapeTimeout	|Timeout after which the scrape is ended	|string|""|
|metrics.serviceMonitor.selector	|Prometheus instance selector labels	|string|{}|
|metrics.serviceMonitor.selector	|Prometheus instance selector labels	|string|{}|
|metrics.serviceMonitor.labels	|ServiceMonitor extra labels	|string|{}|
|metrics.serviceMonitor.annotations	|ServiceMonitor annotations	|string|{}|
|metrics.serviceMonitor.jobLabel	|The name of the label on the target service to use as the job name in prometheus.	|string|""|
|metrics.prometheusRule.enabled	|Set this to true to create prometheusRules for Prometheus operator	|string|false|
|metrics.prometheusRule.additionalLabels	|Additional labels that can be used so prometheusRules will be discovered by Prometheus	|string|{}|
|metrics.prometheusRule.namespace	|namespace where prometheusRules resource should be created	|string|""|
|metrics.priorityClassName	|Metrics exporter pod priorityClassName	|string|""|
|metrics.service.type	|Kubernetes Service type (redis metrics)	|string|ClusterIP|
|metrics.service.loadBalancerIP	|Use serviceLoadBalancerIP to request a specific static IP, otherwise leave blank	|string|""|
|metrics.service.annotations	|Annotations for the services to monitor.	|string|{}|
|metrics.service.labels	|Additional labels for the metrics service	|string|{}|
|metrics.service.clusterIP	|Service Cluster IP	|string|""|


### Sysctl Image parameters
|Parameter|Description|Type|Default|
|---------|-----------|----|-------|
|sysctlImagsysctlImage.repository	|sysctlImage Init container repository	|string|e.enabled	|Enable an init container to modify Kernel settings	|string|false|
|sysctlImage.registry	|sysctlImage Init container registry	|string|docker.io|
|sysctlImage.repository	|sysctlImage Init container repository	|string|bitnami/bitnami-shell|
|sysctlImage.tag	|sysctlImage Init container tag	|string|10-debian-10-r431|
