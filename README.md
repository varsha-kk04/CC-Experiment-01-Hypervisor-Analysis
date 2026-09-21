# CC Experiment 01 - Hypervisor Analysis

## Objective

To analyze and compare the performance of Type-1 and Type-2 hypervisors using virtual machines with similar configurations and CPU benchmarking.

## Hypervisors

### Type-1
- Proxmox VE

### Type-2
- VMware Workstation

## VM Configuration

- Operating System: Ubuntu
- CPU: 2 vCPU
- Memory: 2 GB
- Disk: 20 GB

## Benchmark

Sysbench CPU benchmark:

```bash
sysbench cpu --cpu-max-prime=20000 run
```

## Repository Structure

```text
screenshots/
├── type1-proxmox/
├── type2-vmware/
└── comparison/

results/
└── performance-analysis.md
```

## Results

The experimental results and comparison are documented in the `results` directory.