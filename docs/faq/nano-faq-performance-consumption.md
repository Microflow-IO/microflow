------

layout: default  

title: FAQ-Performance and Consumption  

parent: faq  

nav_order: 4  

------



<img src="https://github.com/Microflow-IO/microflow-nano/blob/main/docs/github_microflow_B.png" alt="logo" style="float:left; margin-right:10px;" />

  

<h1 style="font-size: 30px;">MicroFlow Nano</h1>  
<h2 style="font-size: 50px;">FAQ-Performance and Consumption</h2>

  


[TOC]

------



# 💣Performance and Consumption



## Processing performance and resource consumption

Under 99% of the working conditions, Nano can operate solely with the remaining computing power resources of the host; the following parameters are for reference only;

- Nano parses 1Gbps network traffic in real-time and outputs TCP/UDP quadruples and KPIs, while only consuming 5% of  vCPU and 110MB of memory;
- Nano can parse 1000 concurrent HTTP sessions in real time, outputting HTTP/REQ/RSP/Header/Body, as well as KPIs, while only consuming 10% of vCPU and 110MB of memory;
- In extreme cases, when CPU usage exceeds 20% of one vCPU, Nano will initiate a throttling algorithm to reduce CPU overhead and avoid affecting the operation of other programs;
- Storage requirements?  If the user does not store JSON or PCAP files locally on the host, there is no need to consider the storage overhead of the program itself.



## What should we do if the data volume of traffic logs is too large?	

First of all, since Nano outputs a very simplified traffic log, which has removed background traffic, various communication overhead, and redundant bytes, and it does not output media class loads by default, the interference of the actual output data volume of the Nano to the bandwidth can be almost ignored; 

Of course, if users still need to further reduce the size of the Nano output traffic, we also provide three methods: 

- **Customized types of output data:** For example, in the application performance monitoring scenario, you can only choose to parse the HTTP header without outputting the HTTP body and TCP/UDP communication pairs;
- **Real time compression:** Turn on the compression function of Nano, usually 60% is compressed, which has no obvious impact on resource consumption and processing performance;
- **Sampling of communication pair aggregation and application layer session:** reduce the number of TCP/UDP communication pairs by enlarging the TCP/UDP aggregation time; By sampling application layer sessions (HTTP, SQL, etc.), you can reduce the number of application layer sessions;
- **Truncation of the load segment body:** In most functional scenarios, a complete load segment body is not required. Therefore, users can define the size of the body themselves to reduce the size of the traffic log.



## What is the difference between Nano and switch mirroring?

The (virtual) switch mirroring method, which is commonly used in traditional architectures, is no longer applicable in cloud environments.  However, traffic analysis through virtual switch mirroring is typically used in cloud security resource pool solutions for boundary security, and is not suitable for traffic collection within clouds and cloud-native environments.

Nano is a host-level packet parsing tool that can be flexibly deployed in almost all environments. It does not require any functionality of switches and can achieve fine-grained traffic logging services without blind spots;

In addition, even in environments where it is not convenient to implant probe programs, the issue can be resolved by deploying Nano to servers or virtual machines, and then performing switch mirroring.





------

**www.microflow.io**

**microflow.io@gmail.com**

**07/23/2023**





