# splunk-siem-universal-forwarder
Hands-on Splunk SIEM lab demonstrating the setup of Splunk Enterprise and deployment of Splunk Universal Forwarder for centralized Windows event log collection, monitoring, and analysis.

# Splunk SIEM Setup and Universal Forwarder Deployment

## Project Overview

This project focused on setting up a **Security Information and Event Management (SIEM) lab using Splunk Enterprise and the Splunk Universal Forwarder**. Splunk Enterprise was deployed on a Windows system to function as the central SIEM platform, while a separate **Windows 11 virtual machine running in VMware Workstation** was configured with the Splunk Universal Forwarder.

The Universal Forwarder was configured to collect Windows event logs, including **Application, Security, and System logs**, and forward them to the Splunk Enterprise server. The successful appearance of the Windows host and its associated event sources in Splunk Enterprise confirmed that the **log collection and forwarding process was functioning successfully**.
