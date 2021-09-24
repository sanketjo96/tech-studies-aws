# AWS

#### EC2 Basics

1. EC2 Types
   1. General purpose
       - Balance between compute, networking and memory
       - Ideal for code repo or web servers
       - Example T family
   2. Compute optimize
       - Used for compute intensive workloads like
         - Media transcoding
         - High perf web servers
         - Scientific data modeling 
         - Gaming 
         - Example C family
   3. Memory optimized
       - Useful for processing large data in memory
         - High perf relational/non relational DBs
         - In mem DBs for BI
         - Real time processing apps
         - Example R family
   4. Storage optimized
       - Use cases where there are high sequential read and writes to local storage
         - High frequency online transactions
         - Relational and NOSQL DBs
         - Cache for in mem databases like redis
         - Distributed file system
         - Example I, D or H1 family

2. EC 2 Launch Types
   1. On demand
   2. Reserved (From 1 to 3 yrs)
       - Standard
       - Scheduled
       - Convertible (can change EC2 types)
   3. Spot instances  (less cost)
       - Batch processing
       - Image processing
       - One time JOBS 
       - JOBS with flexible start and end time
   4. Dedicated host
       - Full dedicated machine
       - Can give you full complice
       - Dedicated H/W with full access
       - Control over softwares
       - Higher cost
   5. Dedicated instance
       - Dedicated machine
       - But no access to h/w
       - Useful in cases where high level compliance needs are in place i.e. not sharing h/w with any other aws account

3. IPs
   1. Private
   2. Public
   3. Elastic (charchable and used mostly for redirecting traffic to required instance on failure)

4. Placement groups
   1. Controls placements for EC2
   2. Startegies
       - Cluster - grouped with Low latency h/w, within single AZ
       - Spread - Spread across different H/w, spread across different AZ (critical apps)
       - Partitions - Similar to spread but spread across partitions - racks. They are still separated rack wise, so low latencies.

---

#### Security Groups
1. Classic Ports
    - SHH - 22
    - FTP - 21
    - SFTP - 22
    - HTTP - 80
    - HTTPS - 443
    - RDP - 3389
