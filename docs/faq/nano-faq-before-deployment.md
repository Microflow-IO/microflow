------

layout: default  

title: FAQ-Before Deployment  

parent: faq  

nav_order: 5  

------



<img src="https://github.com/Microflow-IO/microflow-nano/blob/main/docs/github_microflow_B.png" alt="logo" style="float:left; margin-right:10px;" />

  

<h1 style="font-size: 30px;">MicroFlow Nano</h1>  
<h2 style="font-size: 50px;">FAQ-Before Deployment</h2>

  


[TOC]

------



# 🏡Before Deployment



## What platforms or environments can Nano be deployed in?

Nano is a system-level user-mode program that can be adapted to almost all mainstream operating systems, as well as various architectures or environments.  This includes but is not limited to:

- All Linux distributions;  Windows versions;
- X86 platform, ARM platform;
- K8S (image);
- Public cloud, private cloud, hybrid cloud;  virtualization, hyper-converged;  hardware server.



## Do I need to restart or modify the host or business configuration?

No need to restart the host or service, nor to alter the host or service configuration.  Users simply need to establish the relevant network and security policies based on the address and routing of the data receiver.



## Do I need to increase computing power resources for Nano?

When deploying based on the host operating system, it is not necessary.  For details, please refer to "**Processing performance and resource overhead**".



## Which servers can receive the output data of the Nano?

Since the Nano uses open JSON over GELF UDP to send, there are a wide variety of servers.

please refer to “**Server integration**”



## What permissions are required during deployment?

- The Linux version requires root privileges;
- The Windows version requires Administrator privileges.
- K8S, please use DaemonSet to deploy Nano Image as a Pod.



## How does Nano upload data?

Nano has two methods for uploading data to the server or data middleware such as LogStash.

- Nano adopts an active PUSH method to upload JSON over GELF UDP to the server;
- For servers that do not support GELF UDP, Nano can first push the data to LogStash, and then have LogStash push it to the server;
- Nano can also locally cycle and write JSON data into JSON files, which are then uploaded to a third party log collection tool, such as Filebeat, Nxlog, Fluentd, Splunk Universal Forwarder......



## Can I use the log collection agent to collect Nano data

**SURE.**

Nano can locally cycle and write JSON data into JSON files, which are then uploaded to server by a log collection tool, such as Filebeat, Nxlog, Fluentd, Splunk Universal Forwarder......



## How is Nano managed?

Nano can be managed in two ways.  First, through configuration file management.

- Users can update the local configuration file of Nano by updating the configuration file in a specific path of a third-party tool and using Nano to periodically curl to retrieve it;
- Users can also proactively push new versions of configuration files to overwrite the local configuration files on Nano.  Secondly, RESTful management.
- We offer a customized Nano version specifically developed for Graylog. Graylog users can manage Nano through the SideCar interface;
- For commercial users of Nano, we can also offer similar customized services.



## Let's start a simple single host test

1. [**Linux**](https://github.com/Microflow-IO/microflow-nano/tree/main/linux)
2. [**Windows**](https://github.com/Microflow-IO/microflow-nano/tree/main/windows)
3. [**Image**](https://github.com/Microflow-IO/microflow-nano/tree/main/docker)



## How to make rapid large-scale deployment and management？

For the scale deployment and management of K8S, the difference between K8S and small-scale deployment is not significant, so it will not be repeated;

- **Large scale host deployment:** Nano is also very simple. The user only needs to execute the curl to download the Nano and execute the startup command through the automation tool; In this process, there is no need to consider running dependency, version compatibility, resource overhead and other issues;
- **Large scale Nano management:** Nano supports configuration file management. Users only need to specify the update path of the configuration file in the Nano configuration file, and Nano will go to the path every minute to verify whether the configuration file is updated. If there is an update, it will be downloaded to the local update probe configuration;

In addition, for large customers, we also support customized RESTful development to help users achieve Web UI based probe functions and online and offline management.



## Can Nano parse HTTPS?

- High version Nano can parse SSL/TLS plaintext without a CA certificate; But only limited to Linux-64; Windows does not support;
- Low version Nano does not support parsing encrypted traffic; However, in most cases, this does not affect Nano from achieving its intended value! Because the actual deployment location of Nano in production environments is usually before loading HTTPS or after unloading HTTPS; In other words, in most cases, where Nano is deployed, HTTPS is not the primary traffic, so there is no need to worry about the encryption and decryption issues of HTTPS.





------

**www.microflow.io**

**microflow.io@gmail.com**

**07/23/2023**





