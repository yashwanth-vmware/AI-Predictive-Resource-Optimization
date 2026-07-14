# Data Dictionary

| Variable | Description | Planned role |
|---|---|---|
| `timestamp_ms` | Unix epoch timestamp in milliseconds | Time index |
| `cpu_cores` | Provisioned virtual CPU cores | Capacity predictor |
| `cpu_capacity_mhz` | Provisioned CPU capacity in MHz | Capacity predictor |
| `cpu_usage_mhz` | Observed CPU use in MHz | Predictor / secondary target |
| `cpu_usage_pct` | Observed CPU utilization percentage | Primary CPU target |
| `memory_provisioned_kb` | Provisioned VM memory in KB | Capacity predictor |
| `memory_usage_kb` | Active memory use in KB | Primary memory target |
| `disk_read_kbps` | Disk read throughput in KB/s | I/O predictor |
| `disk_write_kbps` | Disk write throughput in KB/s | I/O predictor |
| `network_received_kbps` | Inbound network throughput | Network predictor |
| `network_transmitted_kbps` | Outbound network throughput | Network predictor |
| `vm_id` | Identifier derived from source file | Grouping variable |
| `timestamp` | UTC datetime derived from `timestamp_ms` | Chronological analysis |
| `memory_usage_pct` | Derived memory-utilization percentage | Normalized target |
