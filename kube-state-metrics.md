# Metrics collected by kube-state-metrics

## ConfigMap Metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_configmap_info |Information about configmap | 映射配置信息 | 无
kube_configmap_created | Unix creation timestamp | Unix创建时间戳 | 无
kube_configmap_metadata_resource_version | Resource version representing a specific version of the configmap | 资源版本代表一个指定的映射配置版本 | 无

## CronJob Metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_cronjob_info | Info about cronjob |
kube_cronjob_labels | Kubernetes labels converted to Prometheus labels
kube_cronjob_created | Unix creation timestamp
kube_cronjob_status_active | Active holds pointers to currently running jobs
kube_cronjob_status_last_schedule_time | LastScheduleTime keeps information of when was the last time the job was successfully scheduled
kube_cronjob_spec_suspend | Suspend flag tells the controller to suspend subsequent executions
kube_cronjob_spec_starting_deadline_seconds | Deadline in seconds for starting the job if it misses scheduled time for any reason
kube_cronjob_next_schedule_time | Next time the cronjob should be scheduled. The time after lastScheduleTime, or after the cron job's creation time if it's never been scheduled. Use this to determine if the job is delayed

## DaemonSet Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_daemonset_created | Unix creation timestamp |
kube_daemonset_status_current_number_scheduled | The number of nodes running at least one daemon pod and are supposed to
kube_daemonset_status_desired_number_scheduled | The number of nodes that should be running the daemon pod
kube_daemonset_status_number_available | The number of nodes that should be running the daemon pod and have one or more of the daemon pod running and available
kube_daemonset_status_number_misscheduled | The number of nodes running a daemon pod but are not supposed to
kube_daemonset_status_number_ready | The number of nodes that should be running the daemon pod and have one or more of the daemon pod running and ready
kube_daemonset_status_number_unavailable | The number of nodes that should be running the daemon pod and have none of the daemon pod running and available
kube_daemonset_updated_number_scheduled | The total number of nodes that are running updated daemon pod
kube_daemonset_metadata_generation | Sequence number representing a specific generation of the desired state
kube_daemonset_labels | Kubernetes labels converted to Prometheus labels

## Deployment Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_deployment_created | Unix creation timestamp
kube_deployment_status_replicas | The number of replicas per deployment
kube_deployment_status_replicas_available | The number of available replicas per deployment
kube_deployment_status_replicas_unavailable | The number of unavailable replicas per deployment
kube_deployment_status_replicas_updated | The number of updated replicas per deployment
kube_deployment_status_observed_generation | The generation observed by the deployment controller
kube_deployment_spec_replicas | Number of desired pods for a deployment
kube_deployment_spec_paused | Whether the deployment is paused and will not be processed by the deployment controller
kube_deployment_spec_strategy_rollingupdate_max_unavailable | Maximum number of unavailable replicas during a rolling update of a deployment
kube_deployment_spec_strategy_rollingupdate_max_surge | Maximum number of replicas that can be scheduled above the desired number of replicas during a rolling update of a deployment
kube_deployment_metadata_generation | Sequence number representing a specific generation of the desired state
kube_deployment_labels | Kubernetes labels converted to Prometheus labels

## Endpoint Metrics 
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_endpoint_address_not_ready | Information about endpoint
kube_endpoint_created | Unix creation timestamp
kube_endpoint_labels | Kubernetes labels converted to Prometheus labels
kube_endpoint_address_available | Number of addresses available in endpoint
kube_endpoint_address_not_ready | Number of addresses not ready in endpoint

## Horizontal Pod Autoscaler Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_hpa_metadata_generation | The generation observed by the HorizontalPodAutoscaler controller
kube_hpa_spec_max_replicas | Upper limit for the number of pods that can be set by the autoscaler; cannot be smaller than MinReplicas
kube_hpa_spec_min_replicas | Lower limit for the number of pods that can be set by the autoscaler, default 1
kube_hpa_status_current_replicas | Current number of replicas of pods managed by this autoscaler
kube_hpa_status_desired_replicas | Desired number of replicas of pods managed by this autoscaler
kube_hpa_labels | Kubernetes labels converted to Prometheus labels
kube_hpa_status_condition | The condition of this autoscaler

## Job Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_job_info | Information about job
kube_job_labels | Kubernetes labels converted to Prometheus labels
kube_job_created | Unix creation timestamp
kube_job_spec_parallelism | The maximum desired number of pods the job should run at any given time
kube_job_spec_completions | The desired number of successfully finished pods the job should be run with
kube_job_spec_active_deadline_seconds | The duration in seconds relative to the startTime that the job may be active before the system tries to terminate it
kube_job_status_succeeded | The number of pods which reached Phase Succeeded
kube_job_status_failed | The number of pods which reached Phase Failed
kube_job_status_active | The number of actively running pods
kube_job_complete | The job has completed its execution
kube_job_failed | The job has failed its execution
kube_job_status_start_time | StartTime represents time when the job was acknowledged by the Job Manager
kube_job_status_completion_time | CompletionTime represents time when the job was completed

## LimitRange Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_limitrange | Information about limit range
kube_limitrange_created | Unix creation timestamp

## Namespace Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_namespace_created | Unix creation timestamp
kube_namespace_labels | Kubernetes labels converted to Prometheus labels
kube_namespace_annotations | Kubernetes annotations converted to Prometheus labels
kube_namespace_status_phase | kubernetes namespace status phase

## Node Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_node_info | Information about a cluster node
kube_node_created | Unix creation timestamp
kube_node_labels | Kubernetes labels converted to Prometheus labels
kube_node_spec_unschedulable | Whether a node can schedule new pods
kube_node_spec_taint | The taint of a cluster node
kube_node_status_condition | The condition of a cluster node
kube_node_status_phase | The phase the node is currently in
kube_node_status_capacity | The capacity for different resources of a node
kube_node_status_capacity_pods | The total pod resources of the node
kube_node_status_capacity_cpu_cores | The total CPU resources of the node
kube_node_status_capacity_memory_bytes | The total memory resources of the node
kube_node_status_allocatable | The allocatable for different resources of a node that are available for scheduling
kube_node_status_allocatable_pods | The pod resources of a node that are available for scheduling
kube_node_status_allocatable_cpu_cores | The CPU resources of a node that are available for scheduling
kube_node_status_allocatable_memory_bytes | The memory resources of a node that are available for scheduling

## PersistentVolume Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_persistentvolume_status_phase | The phase indicates if a volume is available, bound to a claim, or released by a claim
kube_persistentvolume_labels | Kubernetes labels converted to Prometheus labels
kube_persistentvolume_info | Information about persistentvolume

## PersistentVolumeClaim Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_persistentvolumeclaim_labels | Kubernetes labels converted to Prometheus labels
kube_persistentvolumeclaim_info | Information about persistent volume claim
kube_persistentvolumeclaim_status_phase | The phase the persistent volume claim is currently in
kube_persistentvolumeclaim_resource_requests_storage_bytes | The capacity of storage requested by the persistent volume claim

## Pod Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_pod_info | Information about pod
kube_pod_start_time | Start time in unix timestamp for a pod
kube_pod_completion_time | Completion time in unix timestamp for a pod
kube_pod_owner | Information about the Pod's owner
kube_pod_labels | Kubernetes labels converted to Prometheus labels
kube_pod_created | Unix creation timestamp
kube_pod_status_scheduled_time | Unix timestamp when pod moved into scheduled status
kube_pod_status_phase | The pods current phase
kube_pod_status_ready | Describes whether the pod is ready to serve requests
kube_pod_status_scheduled | Describes the status of the scheduling process for the pod
kube_pod_container_info | Information about a container in a pod
kube_pod_container_status_waiting | Describes whether the container is currently in waiting state
kube_pod_container_status_waiting_reason | Describes the reason the container is currently in waiting state
kube_pod_container_status_running | Describes whether the container is currently in running state
kube_pod_container_status_terminated | Describes whether the container is currently in terminated state
kube_pod_container_status_terminated_reason | Describes the reason the container is currently in terminated state
kube_pod_container_status_ready | Describes whether the containers readiness check succeeded
kube_pod_container_status_restarts_total | The number of container restarts per container
kube_pod_container_resource_requests | The number of requested request resource by a container
kube_pod_container_resource_limits | The number of requested limit resource by a container
kube_pod_container_resource_requests_cpu_cores | The number of requested cpu cores by a container
kube_pod_container_resource_requests_memory_bytes | The number of requested memory bytes by a container
kube_pod_container_resource_limits_cpu_cores | The limit on cpu cores to be used by a container
kube_pod_container_resource_limits_memory_bytes | The limit on memory to be used by a container in bytes
kube_pod_spec_volumes_persistentvolumeclaims_info | Information about persistentvolumeclaim volumes in a pod
kube_pod_spec_volumes_persistentvolumeclaims_readonly | Describes whether a persistentvolumeclaim is mounted read only

## ReplicaSet metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_replicaset_created | Unix creation timestamp
kube_replicaset_status_replicas | The number of replicas per ReplicaSet
kube_replicaset_status_fully_labeled_replicas | The number of fully labeled replicas per ReplicaSet
kube_replicaset_status_ready_replicas | The number of ready replicas per ReplicaSet
kube_replicaset_status_observed_generation | The generation observed by the ReplicaSet controller
kube_replicaset_spec_replicas | Number of desired pods for a ReplicaSet
kube_replicaset_metadata_generation | Sequence number representing a specific generation of the desired state

## ReplicationController metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_replicationcontroller_created | Unix creation timestamp
kube_replicationcontroller_status_replicas | The number of replicas per ReplicationController
kube_replicationcontroller_status_fully_labeled_replicas | The number of fully labeled replicas per ReplicationController
kube_replicationcontroller_status_ready_replicas | The number of ready replicas per ReplicationController
kube_replicationcontroller_status_available_replicas | The number of available replicas per ReplicationController
kube_replicationcontroller_status_observed_generation | The generation observed by the ReplicationController controller
kube_replicationcontroller_spec_replicas | Number of desired pods for a ReplicationController
kube_replicationcontroller_metadata_generation | Sequence number representing a specific generation of the desired state

## ResourceQuota Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_resourcequota_created | Unix creation timestamp
kube_resourcequota | Information about resource quota

## Secret Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_secret_info | Information about secret
kube_secret_type | Type about secret
kube_secret_labels | Kubernetes labels converted to Prometheus labels
kube_secret_created | Unix creation timestamp
kube_secret_metadata_resource_version | Resource version representing a specific version of secret

## Service Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_service_info | Information about service
kube_service_created | Unix creation timestamp
kube_service_spec_type | Type about service
kube_service_labels | Kubernetes labels converted to Prometheus labels

## Stateful Set Metrics
Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
kube_statefulset_created | Unix creation timestamp
kube_statefulset_status_replicas | The number of replicas per StatefulSet
kube_statefulset_status_replicas_current | The number of current replicas per StatefulSet
kube_statefulset_status_replicas_ready |The number of ready replicas per StatefulSet
kube_statefulset_status_replicas_updated  | The number of updated replicas per StatefulSet
kube_statefulset_status_observed_generation | The generation observed by the StatefulSet controller
kube_statefulset_replicas | Number of desired pods for a StatefulSet
kube_statefulset_metadata_generation | Sequence number representing a specific generation of the desired state for the StatefulSet
kube_statefulset_labels | Kubernetes labels converted to Prometheus labels