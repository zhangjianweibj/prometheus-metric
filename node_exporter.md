# Metrics collected by node_exporter

## bcache metric

Name | Description | 中文描述 | 备注
---------|-------------|---------|-------------
bypassed_bytes_total | Amount of IO (both reads and writes) that has bypassed the cache
cache_hits_total | Hits counted per individual IO as bcache sees them
cache_misses_total | Misses counted per individual IO as bcache sees them
cache_bypass_hits_total | Hits for IO intended to skip the cache
cache_bypass_misses_total | Misses for IO intended to skip the cache
cache_miss_collisions_total | Instances where data insertion from cache miss raced with write (data already present)
cache_readaheads_total | Count of times readahead occurred

average_key_size_sectors | Average data per key in the btree (sectors) | | metrics in /sys/fs/bcache/<uuid>/
btree_cache_size_bytes | Amount of memory currently used by the btree cache || metrics in /sys/fs/bcache/<uuid>/
cache_available_percent | Percentage of cache device without dirty data, usable for writeback (may contain clean cached data)||metrics in /sys/fs/bcache/<uuid>/
congested | Congestion || metrics in /sys/fs/bcache/<uuid>/
root_usage_percent | Percentage of the root btree node in use (tree depth increases if too high)||metrics in /sys/fs/bcache/<uuid>/
tree_depth | Depth of the btree||metrics in /sys/fs/bcache/<uuid>/

active_journal_entries | Number of journal entries that are newer than the index || metrics in /sys/fs/bcache/<uuid>/internal/
btree_nodes | Total nodes in the btree || metrics in /sys/fs/bcache/<uuid>/internal/
btree_read_average_duration_seconds | Average btree read duration || metrics in /sys/fs/bcache/<uuid>/internal/
cache_read_races_total | Counts instances where while data was being read from the cache, the bucket was reused and invalidated - i.e. where the pointer was stale after the read completed || metrics in /sys/fs/bcache/<uuid>/internal/

dirty_data_bytes | Amount of dirty data for this backing device in the cache || metrics in /sys/fs/bcache/<uuid>/<bdev>/

io_errors | Number of errors that have occurred, decayed by io_error_halflife || metrics in /sys/fs/bcache/<uuid>/<cache>/
metadata_written_bytes_total | Sum of all non data writes (btree writes and all other metadata) ||metrics in /sys/fs/bcache/<uuid>/<cache>/
written_bytes_total | Sum of all data that has been written to the cache || metrics in /sys/fs/bcache/<uuid>/<cache>/
priority_stats_unused_percent | The percentage of the cache that doesn't contain any data || metrics in /sys/fs/bcache/<uuid>/<cache>/
priority_stats_metadata_percent | Bcache's metadata overhead || metrics in /sys/fs/bcache/<uuid>/<cache>/

##  cpu_linux metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|------------
guest_seconds_total | Seconds the cpus spent in guests (VMs) for each mode
frequency_hertz | Current cpu thread frequency in hertz
frequency_min_hertz | Minimum cpu thread frequency in hertz
frequency_max_hertz | Maximum cpu thread frequency in hertz
core_throttles_total | Number of times this cpu core has been throttled
package_throttles_total | Number of times this cpu package has been throttled

##  ipvs_linux metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|------------
connections_total | The total number of connections made
incoming_packets_total | The total number of incoming packets
outgoing_packets_total | The total number of outgoing packets
incoming_bytes_total | The total amount of incoming data
outgoing_bytes_total | The total amount of outgoing data
backend_connections_active | The current active connections by local and remote address
backend_connections_inactive | The current inactive connections by local and remote address
backend_weight | The current backend weight by local and remote address

##  wifi_linux metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|------------
interface_frequency_hertz | The current frequency a WiFi interface is operating at, in hertz
station_info | Labeled WiFi interface station information as provided by the operating system
station_connected_seconds_total | The total number of seconds a station has been connected to an access point
station_inactive_seconds | The number of seconds since any wireless activity has occurred on a station
station_receive_bits_per_second | The current WiFi receive bitrate of a station, in bits per second
station_transmit_bits_per_second | The current WiFi transmit bitrate of a station, in bits per second
station_signal_dbm | The current WiFi signal strength, in decibel-milliwatts (dBm)
station_transmit_retries_total | The total number of times a station has had to retry while sending a packet
station_transmit_failed_total | The total number of times a station has failed to send a packet
station_beacon_loss_total | The total number of times a station has detected a beacon loss

##  drbd_linux metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|------------
network_sent_bytes_total | Total number of bytes sent via the network
network_received_bytes_total | Total number of bytes received via the network
disk_written_bytes_total | Net data written on local hard disk; in bytes
disk_read_bytes_total | Net data read from local hard disk; in bytes
activitylog_writes_total | Number of updates of the activity log area of the meta data
bitmap_writes_total | Number of updates of the bitmap area of the meta data
local_pending | Number of open requests to the local I/O sub-system
remote_pending | Number of requests sent to the peer, but that have not yet been answered by the latter
remote_unacknowledged | Number of requests received by the peer via the network connection, but that have not yet been answered
application_pending | Number of block I/O requests forwarded to DRBD, but not yet answered by DRBD
epochs | Number of Epochs currently on the fly
out_of_sync_bytes | Amount of data known to be out of sync; in bytes
node_role_is_primary | Whether the role of the node is in the primary state
disk_state_is_up_to_date | Whether the disk of the node is up to date

##  systemd_linux metrics 

Name | Description | 中文描述 | 备注
---------|-------------|---------|------------
unit_state | Systemd unit
unit_start_time_seconds | Start time of the unit since unix epoch in seconds
system_running | Whether the system is operational (see 'systemctl is-system-running')
units | Summary of systemd unit states
service_restart_total | Service unit count of Restart triggers
timer_last_trigger_seconds | Seconds since epoch of last trigger
socket_accepted_connections_total | Total number of accepted socket connections
socket_current_connections | Current number of socket connections
socket_refused_connections_total | Total number of refused socket connections

##  infiniband_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
link_downed_total | Number of times the link failed to recover from an error state and went down | link_downed
link_error_recovery_total | Number of times the link successfully recovered from an error state | link_error_recovery
multicast_packets_received_total | Number of multicast packets received (including errors) | multicast_rcv_packets
multicast_packets_transmitted_total | Number of multicast packets transmitted (including errors) | multicast_xmit_packets
port_data_received_bytes_total | Number of data octets received on all links | port_rcv_data
port_data_transmitted_bytes_total | Number of data octets transmitted on all links | port_xmit_data
unicast_packets_received_total | Number of unicast packets received (including errors) | unicast_rcv_packets
unicast_packets_transmitted_total | Number of unicast packets transmitted (including errors) | unicast_xmit_packets
legacy_multicast_packets_received_total | Number of multicast packets received | port_multicast_rcv_packets |  Deprecated counters
legacy_multicast_packets_transmitted_total | Number of multicast packets transmitted | port_multicast_xmit_packets | Deprecated counters
legacy_data_received_bytes_total | Number of data octets received on all links | port_rcv_data_64 | Deprecated counters
legacy_packets_received_total | Number of data packets received on all links | port_rcv_packets_64 | Deprecated counters
legacy_unicast_packets_received_total | Number of unicast packets received | port_unicast_rcv_packets | Deprecated counters
legacy_unicast_packets_transmitted_total | Number of unicast packets transmitted | port_unicast_xmit_packets | Deprecated counters
legacy_data_transmitted_bytes_total | Number of data octets transmitted on all links | port_xmit_data_64 | Deprecated counters
legacy_packets_transmitted_total | Number of data packets received on all links | port_xmit_packets_64 | Deprecated counters

##  xfs_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
extent_allocation_extents_allocated_total | Number of extents allocated for a filesystem
extent_allocation_blocks_allocated_total | Number of blocks allocated for a filesystem
extent_allocation_extents_freed_total | Number of extents freed for a filesystem
extent_allocation_blocks_freed_total | Number of blocks freed for a filesystem
allocation_btree_lookups_total | Number of allocation B-tree lookups for a filesystem
allocation_btree_compares_total | Number of allocation B-tree compares for a filesystem
allocation_btree_records_inserted_total | Number of allocation B-tree records inserted for a filesystem
allocation_btree_records_deleted_total | Number of allocation B-tree records deleted for a filesystem
block_mapping_reads_total | Number of block map for read operations for a filesystem
block_mapping_writes_total | Number of block map for write operations for a filesystem
block_mapping_unmaps_total | Number of block unmaps (deletes) for a filesystem
block_mapping_extent_list_insertions_total | Number of extent list insertions for a filesystem
block_mapping_extent_list_deletions_total | Number of extent list deletions for a filesystem
block_mapping_extent_list_lookups_total | Number of extent list lookups for a filesystem
block_mapping_extent_list_compares_total | Number of extent list compares for a filesystem
block_map_btree_lookups_total | Number of block map B-tree lookups for a filesystem
block_map_btree_compares_total | Number of block map B-tree compares for a filesystem
block_map_btree_records_inserted_total | Number of block map B-tree records inserted for a filesystem
block_map_btree_records_deleted_total | Number of block map B-tree records deleted for a filesystem

##  nfs_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
packets_total | Total NFSd network packets (sent+received) by protocol type
connections_total | Total number of NFSd TCP connections
rpcs_total | Total number of RPCs performed
rpc_retransmissions_total | Number of RPC transmissions performed
rpc_authentication_refreshes_total | Number of RPC authentication refreshes performed
requests_total | Number of NFS procedures invoked

##  nfsd_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
requests_total | Total number NFSd Requests by method and protocol
reply_cache_hits_total | Total number of NFSd Reply Cache hits (client lost server response)
reply_cache_misses_total | Total number of NFSd Reply Cache an operation that requires caching (idempotent)
reply_cache_nocache_total | Total number of NFSd Reply Cache non-idempotent operations (rename/delete/…)
file_handles_stale_total | Total number of NFSd stale file handles
disk_bytes_read_total | Total NFSd bytes read
disk_bytes_written_total | Total NFSd bytes written
server_threads | Total number of NFSd kernel threads that are running
read_ahead_cache_size_blocks | How large the read ahead cache is in blocks
read_ahead_cache_not_found_total | Total number of NFSd read ahead cache not found
packets_total | Total NFSd network packets (sent+received) by protocol type
connections_total | Total number of NFSd TCP connections
rpc_errors_total | Total number of NFSd RPC errors by error type
server_rpcs_total | Total number of NFSd RPCs

##  mdadm_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
is_active | Indicator whether the md-device is active or not
disks_active | Number of active disks of device
disks | Total number of disks of device
blocks | Total number of blocks on device
blocks_synced | Number of blocks synced on device

##  hwmon_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
node_hwmon_chip_names | Annotation metric for human-readable chip names
node_hwmon_sensor_label | Label for given chip and sensor
node_hwmon_beep_enabled | Hardware beep enabled
node_hwmon_voltage_regulator_version | Hardware voltage regulator
node_hwmon_update_interval_seconds | Hardware monitor update interval

##  buddyinfo metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
buddyinfo_blocks | Count of free blocks according to size

##  logind_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
logind_sessions | Number of sessions registered in logind

##  textfile_linux metrics 

Name | Description | filenames | 备注
---------|-------------|---------|------------
node_textfile_mtime_seconds | Unixtime mtime of textfiles successfully read