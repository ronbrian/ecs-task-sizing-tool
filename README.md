# 🐳 ECS Task Right-Sizer

A lightweight, static web tool to help AWS engineers and developers determine the optimal vCPU and Memory allocations for Amazon ECS and AWS Fargate tasks. 

Similar to *ec2instances.info*, but specifically designed for containerized workloads on AWS.

## 🚀 Why this exists
Estimating task sizes in ECS can be tricky. Over-provisioning wastes money, while under-provisioning causes out-of-memory (OOM) kills and CPU throttling. Furthermore, randomly sizing tasks can lead to "bin-packing" fragmentation on your underlying EC2 container instances. 

This tool takes the guesswork out of ECS task sizing by mapping your requirements directly to **valid AWS Fargate configurations** and providing architectural best practices.

## ✨ Features
* **Runtime Profiling:** Accounts for the baseline resource footprint of different languages (e.g., JVM overhead vs. lightweight Go/Rust binaries).
* **Workload Adjustments:** Adjusts recommendations based on whether your app is an I/O-bound API, a CPU-bound worker, or a data-processing job.
* **Fargate Alignment:** Strict mapping to valid AWS Fargate vCPU/Memory increments to prevent resource fragmentation.
* **Anti-Pattern Detection:** Warns you about language-specific pitfalls (e.g., assigning multiple vCPUs to a single-threaded Node.js app without clustering).
* **Scaling Advice:** Suggests horizontal scaling (task counts) and load balancer setups for High Availability workloads.

## 🛠️ Built With
* HTML5
* Vanilla JavaScript
* Tailwind CSS
* Hosted on GitHub Pages

## 🌐 Live Demo
Check out the live tool here: **[Link to your GitHub Pages URL]**
