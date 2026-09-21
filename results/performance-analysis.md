# Performance Analysis

## Type-1 Hypervisor – Proxmox VE

- Hypervisor: Proxmox VE
- Hypervisor Type: Type-1
- Guest OS: Ubuntu
- CPU Allocation: 2 vCPU
- Memory Allocation: 2 GB
- Disk Allocation: 20 GB

### Sysbench Result

- Total Execution Time: 10.0006 seconds
- Total Events: 16903
- Events per Second: 1689.43
- Average Latency: 0.59 ms

## Type-2 Hypervisor – VMware Workstation

- Hypervisor: VMware Workstation
- Hypervisor Type: Type-2
- Guest OS: Ubuntu
- CPU Allocation: 2 vCPU
- Memory Allocation: 2 GB
- Disk Allocation: 20 GB

### Sysbench Result

- Total Execution Time: 10.0007 seconds
- Total Events: 13497
- Events per Second: 1349.48
- Average Latency: 0.74 ms

## Comparison

| Performance Metric | Proxmox VE (Type-1) | VMware Workstation (Type-2) |
|---|---:|---:|
| Total Execution Time | 10.0006 s | 10.0007 s |
| Total Events | 16903 | 13497 |
| Events per Second | 1689.43 | 1349.48 |
| Average Latency | 0.59 ms | 0.74 ms |

### Performance Difference

The Proxmox VE VM recorded 1689.43 events per second, while the VMware Workstation VM recorded 1349.48 events per second.

The difference in events per second is:

- Difference: 339.95 events/second
- Percentage difference relative to VMware: approximately 25.19%

The average latency recorded was:

- Proxmox VE: 0.59 ms
- VMware Workstation: 0.74 ms

The measured execution times were nearly identical at approximately 10 seconds for both experiments.

## Conclusion

Both hypervisors were evaluated using Ubuntu virtual machines configured with 2 vCPU, 2 GB memory, and 20 GB disk. The Sysbench CPU benchmark was executed using:

```bash
sysbench cpu --cpu-max-prime=20000 run