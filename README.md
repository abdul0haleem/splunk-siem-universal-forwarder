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

## 🖥️ Lab Environment

| Component                   | Configuration                                  |
| --------------------------- | ---------------------------------------------- |
| **SIEM Platform**           | Splunk Enterprise                              |
| **Log Collection Agent**    | Splunk Universal Forwarder                     |
| **Virtualization Platform** | VMware Workstation                             |
| **SIEM Server**             | Windows system running Splunk Enterprise       |
| **Endpoint**                | Windows 11 virtual machine                     |
| **Log Sources**             | Windows Application, Security, and System logs |
| **Receiving Port**          | 9997                                           |
| **Deployment Server Port**  | 8089                                           |
| **Monitoring Interface**    | Splunk Web / Search & Reporting                |

## 🛠️ Tools Used

* **Splunk Enterprise** – Central SIEM platform used for receiving, indexing, searching, and monitoring security events.
* **Splunk Universal Forwarder** – Used to collect and forward Windows event logs to Splunk Enterprise.
* **VMware Workstation** – Used to host the Windows 11 virtual machine used as the log-generating endpoint.
* **Windows 11** – Endpoint operating system used for generating and collecting Windows event logs.
* **Windows Command Prompt (`ipconfig`)** – Used to identify the IPv4 address of the Splunk Enterprise server.
* **Splunk Web / Search & Reporting** – Used to verify hosts, sources, event counts, and received logs.

### 1. Downloading Splunk Enterprise

The first step in the SIEM lab setup was to obtain the **Splunk Enterprise** installation package from the official Splunk website.

#### Procedure

1. Navigate to the [official Splunk website](https://www.splunk.com/?utm_source=chatgpt.com).
2. Navigate to **Trials & Downloads** and select **Start Your Free Trial**.
3. Enter the required account information and complete the account registration process.
4. Verify the account using the verification code sent to the registered email address.
5. After completing the account creation process, navigate to the **Splunk Enterprise** download section.
6. Select **Windows** as the target operating system and choose the appropriate Splunk Enterprise installation package.
7. Download the installation package to the Windows system that will be used for the SIEM lab.

#### Purpose

This step provides the **Splunk Enterprise installation package** required to deploy the central SIEM platform. Splunk Enterprise will subsequently be configured to receive and analyze security logs forwarded from the Windows endpoint using the **Splunk Universal Forwarder**.

![Figure 1 - Splunk Enterprise download page](screenshots/01-splunk-enterprise-download.png)

*Figure 1: Splunk Enterprise download page showing the Windows installation package.*

### 2. Installing Splunk Enterprise

The downloaded Splunk Enterprise installation package was located in the **Downloads** folder and used to install Splunk Enterprise on the Windows system.

#### Procedure

1. Navigate to the **Downloads** folder and locate the downloaded Splunk Enterprise installer.
2. Open the installer to launch the **Splunk Enterprise Setup Wizard**.
3. Review the Splunk Enterprise license agreement and accept the terms to continue.
4. Select the installation location for Splunk Enterprise. The default installation directory was used.
5. Create the initial **Splunk administrator account** by entering a username and password.
6. Review the selected installation options and click **Install** to begin the installation.
7. Wait for the installation process to complete.
8. Once the installation is completed successfully, click **Finish** to close the Setup Wizard.

#### Purpose

This step installs **Splunk Enterprise** on the Windows system, establishing the central SIEM platform that will later be configured to **receive, index, search, and analyze security logs** from the Windows endpoint.

![Figure 2 - Splunk Enterprise installation](screenshots/02-splunk-enterprise-installation.png)

*Figure 2: Splunk Enterprise installation and configuration using the Setup Wizard.*

### 3. Configuring Splunk Receiving

After installing Splunk Enterprise, the application was launched and configured to receive data from the **Splunk Universal Forwarder**.

#### Procedure

1. Launch **Splunk Enterprise** from the Windows system.
2. The Splunk login screen will appear. Enter the **username and password** created during the installation process.
3. After successful authentication, the **Splunk Web interface** will be displayed.
4. Click **Settings** to open the settings menu.
5. Under the **Data** section, select **Forwarding and receiving**.

![Figure 3 - Forwarding and Receiving settings](screenshots/03-forwarding-receiving-settings.png)

*Figure 3: Accessing the Forwarding and Receiving configuration under Splunk Settings.*

6. In the **Receive Data** section, locate **Configure receiving** and click **Add new**.

![Figure 4 - Receive Data configuration](screenshots/04-receive-data.png)

*Figure 4: Receive Data section in the Splunk Forwarding and Receiving configuration.*

7. Specify the port number that Splunk Enterprise will use to receive forwarded data. The default Splunk receiving port **9997** was used.

![Figure 5 - Splunk receiving port](screenshots/05-receiving-port-9997.png)

*Figure 5: Configuring Splunk Enterprise to receive forwarded data on port 9997.*

8. Save the configuration to enable Splunk Enterprise to listen for incoming data from the Universal Forwarder.

#### Purpose

This step configures Splunk Enterprise to **receive log data from the Splunk Universal Forwarder**. Port **9997** is used as the receiving port through which forwarded event data is sent from the Windows endpoint to the Splunk Enterprise server.
