# Service Level Agreements and Objectives (SLAs/SLOs)

## Purpose

The purpose of this section is to outline the service level agreements (SLAs) and service level objectives (SLOs) that are expected to be met by the target-state solution including any test results from availability and performance testing that verify the system's availability and performance.  The primary audience for this section is architects, lead engineers, and site reliability engineers, however, engineering leaders may also use this section to determine if the system's performance profile will meet business objectives.  The artifacts in this section are at the `sea` level of abstraction.

## Electivity

This section is considered:  **Mandatory**

## Service Level Objectives

### High-Availability/Disaster Recovery Approach

* Availability Strategy
  * Active/Passive Multi-Region with Failover
  * Active/Active Multi-Region with Load Balancing
* Availability Test Results
* Diasaster Recovery Strategy
  * Backup and Restore
  * Pilot Light
  * Warm Standby
  * Multi-Site Active/Active
* Disaster Recovery Test Results

### Performance Objectives

* Performance Expectations
  * Maximum Throughput: 1000 transactions per second
  * Average Latency: 100ms
  * TP99: 1000ms
  * Error Rate: 0.1%
* Performance Testing Results
  * Maximum Throughput Results
  * Average Latency Results
  * TP99 Results
  * Error Rate Results
* Previous Peak Season Performance Results
  * Maximum Throughput Results
  * Average Latency Results
  * TP99 Results
  * Error Rate Results

### Service Level Agreements

* SLAs
  * Availability: 99.9% uptime
  * Recovery Time Objective (RTO): 4 hours
  * Recovery Point Objective (RPO): 1 hour
* Actual Service Levels
  * Availability: 99.1% uptime
  * Recovery Time Objective (RTO): 8 hours
  * Recovery Point Objective (RPO): 1.5 hours
