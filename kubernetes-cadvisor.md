# Metrics collected by cadvisor

## CpuUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_cpu_user_seconds_total | Cumulative user cpu time consumed in seconds
container_cpu_system_seconds_total | Cumulative system cpu time consumed in seconds
container_cpu_usage_seconds_total | Cumulative cpu time consumed in seconds
container_cpu_cfs_periods_total | Number of elapsed enforcement period intervals
container_cpu_cfs_throttled_periods_total | Number of throttled period intervals
container_cpu_cfs_throttled_seconds_total | Total time duration the container has been throttled

## ProcessSchedulerMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_cpu_schedstat_run_seconds_total | Time duration the processes of the container have run on the CPU
container_cpu_schedstat_runqueue_seconds_total | Time duration processes of the container have been waiting on a runqueue
container_cpu_schedstat_run_periods_total | Number of times processes of the cgroup have run on the cpu

## CpuLoadMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_cpu_load_average_10s | Value of container cpu load average over the last 10 seconds
container_tasks_state | Number of tasks in given state

## MemoryUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_memory_cache | Number of bytes of page cache memory
container_memory_rss | Size of RSS in bytes
container_memory_swap | Container swap usage in bytes
container_memory_failcnt | Number of memory usage hits limits
container_memory_usage_bytes | Current memory usage in bytes, including all memory regardless of when it was accessed
container_memory_max_usage_bytes | Maximum memory usage recorded in bytes
container_memory_working_set_bytes | Current working set in bytes
container_memory_failures_total | Cumulative count of memory allocation failures

## AcceleratorUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_accelerator_memory_total_bytes | Total accelerator memory
container_accelerator_memory_used_bytes | Total accelerator memory allocated
container_accelerator_duty_cycle | Percent of time over the past sample period during which the accelerator was actively processing

## DiskUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_fs_inodes_free | Number of available Inodes
container_fs_inodes_total | Number of Inodes
container_fs_limit_bytes | Number of bytes that can be consumed by the container on this filesystem
container_fs_usage_bytes | Number of bytes that are consumed by the container on this filesystem

## DiskIOMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_fs_reads_bytes_total | Cumulative count of bytes read
container_fs_reads_total | Cumulative count of reads completed
container_fs_sector_reads_total | Cumulative count of sector reads completed
container_fs_reads_merged_total | Cumulative count of reads merged
container_fs_read_seconds_total | Cumulative count of seconds spent reading
container_fs_writes_bytes_total | Cumulative count of bytes written
container_fs_writes_total | Cumulative count of writes completed
container_fs_sector_writes_total | Cumulative count of sector writes completed
container_fs_writes_merged_total | Cumulative count of writes merged
container_fs_write_seconds_total | Cumulative count of seconds spent writing
container_fs_io_current | Number of I/Os currently in progress
container_fs_io_time_seconds_total | Cumulative count of seconds spent doing I/Os
container_fs_io_time_weighted_seconds_total | Cumulative weighted I/O time in seconds

## NetworkUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_network_receive_bytes_total | Cumulative count of bytes received
container_network_receive_packets_total | Cumulative count of packets received
container_network_receive_packets_dropped_total | Cumulative count of packets dropped while receiving
container_network_receive_errors_total | Cumulative count of errors encountered while receiving
container_network_transmit_bytes_total | Cumulative count of bytes transmitted
container_network_transmit_packets_total | Cumulative count of packets transmitted
container_network_transmit_packets_dropped_total | Cumulative count of packets dropped while transmitting
container_network_transmit_errors_total | Cumulative count of errors encountered while transmitting

## NetworkTcpUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_network_tcp_usage_total | tcp connection usage statistic for container

## NetworkUdpUsageMetrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_network_udp_usage_total | udp connection usage statistic for container

## Container spec Metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
container_start_time_seconds | Start time of the container since unix epoch in seconds
container_spec_cpu_period | CPU period of the container
container_spec_cpu_quota | CPU quota of the container
container_spec_cpu_shares | CPU share of the container
container_spec_memory_limit_bytes | Memory limit for the container
container_spec_memory_swap_limit_bytes | Memory swap limit for the container
container_spec_memory_reservation_limit_bytes | Memory reservation limit for the container
