# splunk-siem-universal-forwarder
Hands-on Splunk SIEM lab demonstrating the setup of Splunk Enterprise and deployment of Splunk Universal Forwarder for centralized Windows event log collection, monitoring, and analysis.

# Splunk SIEM Setup and Universal Forwarder Deployment

## 📖 Project Overview

This project focused on setting up a **Security Information and Event Management (SIEM) lab using Splunk Enterprise and the Splunk Universal Forwarder**. Splunk Enterprise was deployed on a Windows system to function as the central SIEM platform, while a separate **Windows 11 virtual machine running in VMware Workstation** was configured with the Splunk Universal Forwarder.

The Universal Forwarder was configured to collect Windows event logs, including **Application, Security, and System logs**, and forward them to the Splunk Enterprise server. The successful appearance of the Windows host and its associated event sources in Splunk Enterprise confirmed that the **log collection and forwarding process was functioning successfully**.

## 🎯 Objectives

The main objectives of the project were:

* To understand the basic architecture and functionality of a **SIEM platform**.
* To install and configure **Splunk Enterprise** as a centralized log management and monitoring platform.
* To install and configure the **Splunk Universal Forwarder** on a Windows 11 endpoint.
* To configure Splunk Enterprise to receive forwarded log data.
* To establish communication between the **Universal Forwarder and Splunk Enterprise**.
* To collect and monitor **Windows Application, Security, and System event logs**.
* To verify successful log forwarding and analyze the received events using **Splunk Search & Reporting**.

