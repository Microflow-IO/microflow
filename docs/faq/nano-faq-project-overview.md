---
layout: default  

title: FAQ-Project Overview  

parent: faq  

nav_order: 1  

------



<img src="https://github.com/Microflow-IO/microflow-nano/blob/main/docs/github_microflow_B.png" alt="logo" style="float:left; margin-right:10px;" />

  

<h1 style="font-size: 30px;">MicroFlow Nano</h1>  
<h2 style="font-size: 50px;">FAQ-Project Overview</h2>

  


[TOC]

------




# 🎏Project Overview



## What is Microflow Nano?

- Nano is a cross-architecture host traffic log microprobe with extensive deployment experience. It can provide high-quality, fine-grained traffic log data for various data analysis platforms, enabling rich functionality and value.
- Nano is designed according to commercial product standards and meets 7 * 24 * 365 and large-scale deployment requirements in terms of processing performance, resource overhead, configuration management, compatibility, and security.
- By utilizing log analysis tools, SOC, Modsecurity for Anylog(MSA)[^1], and STIX Spark[^2] in conjunction, a wide range of security and operation scenarios can be achieved.
- In addition, Nano's high-quality, fine-grained traffic log data serves as essential training data for the AISEC project, significantly reducing training time.

[^1]: Based on Modsecurity, it is specially designed to analyze risks in various HTTP logs and can be used in Docker in conjunction with log platforms.
[^2]: STIX Spark is a high-performance program for real-time matching of STIX libraries, which can be used in conjunction with log analysis platforms in Docker.



## What problem does Nano solve?

- **Demand:** Fine-grained traffic logs serve as the foundational data for various tasks such as "risk detection, performance monitoring, and traffic analysis";  however, in cloud/cloud native environments, especially where various Linux and Windows versions coexist, obtaining them is more challenging;
- **Puzzlement:** On one hand, in the context of cloud and cloud-native architectures, dynamic workloads, and the widespread adoption of HTTPS, the switch image method has become ineffective. On the other hand, within the host, real-time analysis of host traffic demands additional resources, and eBPF is not compatible with Windows and older versions of Linux;



## What application scenarios can be realized by adopting Nano?

By integrating with various log analysis platforms, observability solutions, and risk detection SOC solutions, Nano's high-quality, fine-grained traffic log data can quickly realize a wide range of application scenarios, including important needs that have not yet been addressed or have achieved suboptimal results in cloud and cloud-native environments at this stage.

1.	**Attack Context for SOC / XDR / AISEC**
2.	**East-West Lateral Movement Detection**
3.	**API Attack Detection & Performance Monitoring**
4.	**Cloud Network Traffic Analysis (Cloud-NTA)**
5.	**Granular Cloud Traffic Observability**
6.	**Compromised Host Identification**
7.	**Cloud Sensitive Data Behavior Monitoring**
8.	**Sensitive data leakage prevention DDR**
9.	**Prospective application layer Micro-Isolation**
10.	**PCAP Export for Sandbox Analysis**
11.	**Non-Intrusive DB/SQL Performance Monitoring**
12.	**Hybrid Performance Management XPM**



## Technical highlights of Nano

- **Cross-platform:** compatible with Linux, Windows, ARM/X86, K8S, and container environments; as well as various cloud environments. compatible with the present and future;
- **Ultra-lightweight:** a standalone Linux tool weighing only 500KB, yet boasting incredibly powerful functionality;
- **Ultra-low resource consumption:** fixed memory usage of 110MB, capable of processing massive amounts of data in real time without requiring additional CPU resources;
- **Ultra-fine granularity:** Real-time parsing of HTTP/API/header/body, SQL, DNS, Redis, MQ, TCP/UDP...... as well as host metrics;
- **Super safe:** The deployment of Nano does not require restarting or altering the host and user services; it does not involve any kernel risks; and it does not introduce third-party runtime dependencies.



## What data and KPIs can Nano output?

Please refer to another .md document, "**[Nano Output List](https://github.com/Microflow-IO/microflow-nano/blob/main/docs/Nano_Output_List.md)**".



## Is there an online demo

https://demo.microlfow.io

login: guest

password: mfnano@2024



## Is Nano an open-source program?

Nano is not a program open to the public;  

However, for security reasons, Nano is open sourced to major commercial clients.  Other projects of Microflow.io are open to the public.



## Is Nano free?

Nano is permanently free for individuals and small-to-medium-sized users.

For commercial key accounts, Nano will charge an appropriate cost, but it will be significantly lower than the cost of developing Nano by the users themselves.



## How can I obtain technical support?

For the free version, users can communicate through GitHub issues;  we will respond as promptly as possible;

For the commercial version, users can contact us via email (microflow.io@gmail.com). Typically, we will respond within a maximum of four hours and provide an estimated time for addressing potential program bugs.





------

**www.microflow.io**

**microflow.io@gmail.com**

**07/23/2023**

