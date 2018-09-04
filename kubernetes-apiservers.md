# Metrics collected by kubernetes-apiservers

## audit metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
event_total | Counter of audit events generated and sent to the audit backend
error_total | Counter of audit events that failed to be audited properly.Plugin identifies the plugin affected by the error
level_total | Counter of policy levels for audit events (1 per request)

## endpoints metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
apiserver_request_count | Counter of apiserver requests broken out for each verb, API resource, client, and HTTP response contentType and code
apiserver_longrunning_gauge | Gauge of all active long-running apiserver requests broken out by verb, API resource, and scope. Not all requests are tracked this way
apiserver_request_latencies | Response latency distribution in microseconds for each verb, resource and subresource
apiserver_request_latencies_summary | Response latency summary in microseconds for each verb, resource and subresource
apiserver_response_sizes | Response size distribution in bytes for each verb, resource, subresource and scope (namespace/cluster)
apiserver_dropped_requests | Number of requests dropped with 'Try again later' response
apiserver_registered_watchers | Number of currently registered watchers for a given resources
apiserver_current_inflight_requests | Maximal mumber of currently used inflight request limit of this apiserver per request kind in last second

## storage etcd metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
etcd_helper_cache_hit_count | Counter of etcd helper cache hits
etcd_helper_cache_miss_count | Counter of etcd helper cache miss
etcd_helper_cache_entry_count | Counter of etcd helper cache entries. This can be different from etcd_helper_cache_miss_count.because two concurrent threads can miss the cache and generate the same entry twice
etcd_request_cache_get_latencies_summary | Latency in microseconds of getting an object from etcd cache
etcd_request_cache_add_latencies_summary | Latency in microseconds of adding an object to etcd cache
etcd_request_latencies_summary | Etcd request latency summary in microseconds for each operation and object type
etcd_object_counts | Number of stored objects at the time of last check split by kind

## storage value metrics

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
transformation_latencies_microseconds | Latencies in microseconds of value transformation operations
transformation_failures_total | Total number of failed transformation operations 
envelope_transformation_cache_misses_total | Total number of cache misses while accessing key decryption key(KEK)
data_key_generation_latencies_microseconds | Latencies in microseconds of data encryption key(DEK) generation operations
data_key_generation_failures_total | Total number of failed data encryption key(DEK) generation operations


