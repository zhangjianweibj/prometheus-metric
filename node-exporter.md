# Metrics collected by node exporter

## 2018/5/16 node exporter new version 0.16.0 released many metrics have been renamed.eg

<ul>
<li> node_cpu ->  node_cpu_seconds_total </li>
<li> node_memory_MemTotal -> node_memory_MemTotal_bytes </li>
<li> node_memory_MemFree -> node_memory_MemFree_bytes </li>
<li> node_filesystem_avail -> node_filesystem_avail_bytes </li>
<li> node_filesystem_size -> node_filesystem_size_bytes </li>
<li> node_disk_io_time_ms -> node_disk_io_time_seconds_total </li>
<li> node_disk_reads_completed -> node_disk_reads_completed_total </li>
<li> node_disk_sectors_written -> node_disk_written_bytes_total </li>
<li> node_time -> node_time_seconds </li>
<li> node_boot_time -> node_boot_time_seconds </li>
<li> node_intr -> node_intr_total </li>
</ul>

In addition to these changes,new feature visit this \([reference](https://github.com/prometheus/node_exporter/releases)\) to view.