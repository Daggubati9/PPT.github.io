## ☁️ Google Cloud Platform (GCP) Overview:-

## 🔹 GCP (Google Cloud Platform):
A cloud service by Google that lets you run applications, store data, and use powerful computing resources online.

## 🔹 Google Cloud Platform:
Same as GCP — it includes tools for computing, databases, AI, and storage, all accessible through the internet.

## 🔹 Project:
A project in GCP is a logical container for resources (like APIs, storage, databases).

All billing, access control, and API usage are tied to a specific project.

## 🔹 Terraform:
An open-source tool used to automatically create and manage cloud resources (like GCP projects) using simple code.

## 🔐 Access Control in GCP

🔹 IAM (Identity and Access Management)

Manages who can do what on which resources. Access controls who can view, use, or manage resources in a Google Cloud project. It’s managed through IAM permissions.


## Roles:
## 🔹 Primitive Role:
Basic roles like Viewer, Editor, and Owner that apply broad access across all resources in a project.

## 🔹 Predefined Role:
Roles created by Google with specific permissions for a particular service (e.g., Storage Admin, Compute Viewer). Granular, service-specific roles (e.g., BigQuery Data Viewer, Dialogflow Admin).

## 🔹 Custom Role:
User-created roles that allow you to define a set of permissions tailored to your specific needs. You define specific permissions for custom needs.


## 🔑 Service Account:
A special Google account used by apps or virtual machines (VMs) to access GCP services.

Helps run services like Cloud Run or authenticate with APIs like Dialogflow.

## 📊 API Services and Usage:
    Billing Based on Usage:GCP charges based on actual usage (e.g., number of queries, storage used, compute time).       
    Billing Account:Your project must be linked to a Billing Account to use paid GCP services.

## API / Service	Purpose:
| **API Name**       | **Simple Explanation**                                                      |
| ------------------ | --------------------------------------------------------------------------- |
| **Dialogflow API** | Used to build chatbots and voice assistants that understand human language. |
| **Cloud SQL API**  | Lets you manage cloud databases like MySQL and PostgreSQL.                  |
| **BigQuery API**   | Helps you run fast queries on huge amounts of data.                         |
| **Vertex AI API**  | Used to build and run machine learning models easily.                       |
| **Cloud Run API**  | Runs your container apps and handles scaling automatically.                 |
| **Connectors API** | Connects GCP with other systems like Salesforce or databases.               |


## 🔹 Virtual Networking:
Virtual networking in cloud platforms like GCP allows resources (like VMs) to communicate securely using virtual networks.
It includes components like VPCs, subnets, firewalls, and IP addresses to manage traffic flow.

## CHAT GPT Versions:
GPT-4.5 is the latest version of ChatGPT, released by OpenAI on February 27, 2025 .
Older versions like GPT-3.5 and GPT-3 were slower and less advanced in understanding and answering questions.

## VPC:
🔹 VPC (Virtual Private Cloud) is like your own private network inside the cloud.

🔹 It helps connect and protect your cloud resources like virtual machines, databases, etc.

🔹 You can control:

🔹 Think of it as setting up your own mini data center, but online.

## Firewall:
🔹 A firewall is a security system that controls who can access your network and what traffic is allowed in and out.

🔹 It works like a gatekeeper:

It blocks unwanted traffic (like hackers trying to get in).

It allows trusted traffic (like your web browser accessing a website).

🔹 You can set rules to decide which types of data are safe or unsafe.

## GCP Storage options:
| **Storage Type**     | **Description**                                                                              | **Types of Files Stored**                                                                                                 |
| -------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Object Storage**   | Stores unstructured data as objects (file + metadata). Ideal for backups, images, and media. | - **Images:** JPG, PNG, GIF <br> - **Videos:** MP4, AVI, MOV <br> - **Backups:** ZIP, TAR <br> - **Logs:** TXT, JSON, CSV |
| **Block Storage**    | Stores data in fixed-size blocks like a hard drive. Used for VM disks and databases.         | - **VM Files:** VHD, VMDK <br> - **Database Files:** MySQL, PostgreSQL <br> - **Log Files:** TXT, LOG                     |
| **File Storage**     | Provides a traditional file system with folders and directories. Best for shared access.     | - **Documents:** DOCX, PDF, TXT <br> - **Spreadsheets:** XLSX, CSV <br> - **Configuration Files:** JSON, YAML, INI        |
| **Database Storage** | Stores data in structured tables for relational databases.                                   | - **SQL Files:** .sql, .db <br> - **BigQuery Export Files:** CSV, JSON, Avro, Parquet                                     |

## Integration Storage types:
| **Integration Type**         | **Description**                                                                       | **Example**                                                        |
| ---------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **Inside Cloud (Internal)**  | Integration **within GCP** services, offering secure and fast connections.            | Cloud Storage ↔ BigQuery <br> Cloud Pub/Sub ↔ Cloud Functions      |
| **Outside Cloud (External)** | Integration with **external systems** like on-prem services or third-party platforms. | GCP ↔ Salesforce (via APIs) <br> GCP ↔ On-prem databases (via VPN) |

## When integrating pipelines from outside the cloud:
| **Mechanism**                   | **Description**                                                                |
| ------------------------------- | ------------------------------------------------------------------------------ |
| **REST APIs**                   | Used to send or retrieve data between external systems and GCP services.       |
| **Cloud VPN / Interconnect**    | Provides secure, direct network connectivity from on-premises to GCP.          |
| **Pub/Sub**                     | Enables real-time event/data streaming from external systems to GCP pipelines. |
| **SFTP/FTP (Batch Transfer)**   | Transfers large files in batches from external environments to Cloud Storage.  |
| **Cloud Functions / Cloud Run** | Offers HTTP endpoints to trigger serverless workflows from external systems.   |
| **Apache Airflow / Talend**     | Orchestrates and automates multi-step data workflows across platforms.         |
| **Kafka / Dataflow**            | Streams real-time data from external sources into GCP for processing.          |
