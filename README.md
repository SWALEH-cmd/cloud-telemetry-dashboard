# Cloud Infrastructure Telemetry & Performance Dashboard

##  Project Overview
An enterprise database logging and analytics script designed to aggregate hardware performance metrics across multi-region cloud server deployments.

---

##  The STAR Breakdown

###  Situation
A multi-cloud enterprise environment consisting of numerous running and stopped AWS/Azure instances was experiencing sporadic network bottlenecks. The core operations team lacked centralized dashboard visibility to quickly isolate which geographic regions were operating under critical compute strain and which specific nodes were driving high utilization costs.

###  Task
As a Cloud Support Associate, my task was to write an optimized relational database infrastructure query to analyze raw hardware utilization logs. The solution needed to automatically calculate regional load averages, filter out inactive nodes, isolate regions operating at over 75% load capacity, and pinpoint the exact top three resource-hogging virtual machines for immediate engineering remediation.

###  Action
* **Architecture Design:** Built and seeded a high-density structured relational schema inside an Ubuntu environment using SQLite to mimic production cloud platform telemetry logs.
* **Aggregated Load Filtering:** Implemented conditional multi-column grouping utilizing `GROUP BY` and the `HAVING` clause to mathematically compute and filter out stable regions, isolating only high-stress target clusters.
* **Top-N Performance Bottleneck Isolation:** Chained structural data ordering (`ORDER BY DESC`) with record threshold clipping (`LIMIT 3`) to eliminate background data noise and surface the exact machine IDs causing systemic performance decay.

###  Result
* Successfully isolated the specific high-strain deployment regions (`us-east-1` and `eu-west-1`) operating with an average compute strain exceeding the 75% critical threshold.
* Captured the top 3 absolute worst resource-offending server IDs out of thousands of mock records, reducing the time required to locate performance bottlenecks from hours to an instant script execution.

---

##  Tech Stack & Environment
* **OS:** Linux (Ubuntu)
* **Database Engine:** SQLite3



##  Terminal Verification & Output Proof

### 1. Workspace and Environment Setup
![Workspace Setup](screenshot1_setup.png)

### 2. Live Terminal Query Output Results
![Terminal Output](screenshot2_output.png)




---

#  Lab 2: Security Audit & Incident Response Ledger

##  Project Overview
A production-grade database security compliance script designed to analyze access logs, isolate brute-force vectors via pattern matching, and classify infrastructure threats dynamically.

---

##  The STAR Breakdown

###  Situation
An enterprise web application infrastructure was targets of brute-force validation attempts and credential-stuffing exploits. The security team lacked an active tracking layer to instantly gauge request clusters probing privilege-escalation routes (`/admin`) or evaluate risk severity levels across high-volume access attempts.

###  Task
As a Cloud Support Associate, my task was to build an isolation matrix to evaluate raw server access registries. The solution needed to identify administrative entry points, detect suspicious request velocity metrics, and automatically tag bad traffic with action-oriented risk classifications to accelerate incident mitigation.

###  Action
* **Log Architecture Design:** Implemented an incident audit trail schema (`access_logs`) tracking resource paths, validation variables, and endpoint hit counts.
* **Malicious Vector Identification:** Structured pattern evaluation constraints utilizing `LIKE '%/admin%'` to dynamically flag perimeter probing targeting administrative boundaries.
* **Conditional Logic Engine:** Formulated advanced multi-variable workflows (`CASE WHEN` with conditional `OR` mechanics) to categorize system alerts dynamically based on credentials states and high-volume hit spikes.

###  Result
* Successfully mapped raw system traffic into a structured alert dashboard, separating legitimate actions from perimeter threats instantly.
* Isolated brute-force points of origin, automatically applying critical isolation directives (`🚨 CRITICAL THREAT: ISOLATE IP`) to compromised nodes without manually reviewing raw logs.

---

##  Terminal Verification & Output Proof

### 1. Workspace and Environment Setup
![Workspace Setup](Lab2_Security_Audit/WorkspaceSetup.png)

### 2. Live Terminal Security Query Output Results
![Terminal Output](Lab2_Security_Audit/DatabaseOutput.png)
