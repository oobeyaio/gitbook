---
description: >-
  This guide explains how to view resource utilization in real time and how to
  gather data over a specific period using monitoring tools.
---

# How to Retrieve Resource Utilization Data

### **Real-Time Resource Utilization Monitoring**

You can use the following commands to check the resource usage of your system or containers in real time. These commands will provide information about CPU, memory, disk, and container resource usage.

#### **1. Memory Usage**

Use the `free -m` command to view the system’s memory usage in megabytes (MB).

```bash
free -m
```

* **Total**: The total amount of memory.
* **Used**: The memory currently in use.
* **Free**: Memory that is available.

#### **2. Disk Usage**

Use the `df -h` command to check disk space usage.

```bash
df -h
```

* This will display disk usage in a human-readable format (GB or MB), showing the used and available space for each mounted filesystem.

#### **3. Docker Containers Resource Usage**

To monitor the resource usage of running Docker containers, use the `docker stats` command.

```bash
docker stats
```

* This will show real-time CPU, memory, network, and disk metrics for each container.

#### **4. CPU and Memory Usage of Processes**

To monitor the CPU and memory usage of processes running on your system, use the `top` command.

```bash
top
```

* This provides real-time information about which processes are consuming the most resources on your system.

***

### **Resource Utilization Over A Specific Period**

If you're looking to track resource usage over a specific period (e.g., a week or month), we recommend setting up a monitoring system. If you’re already using a monitoring tool (such as Azure Monitor, Elastic APM, or Prometheus), we’d be happy to assist you in configuring it to gather the necessary data.



***

### **Need Further Assistance?**

If you need more help setting up or configuring your monitoring system, feel free to reach out to our support team. We're here to assist you with any questions or technical details.
