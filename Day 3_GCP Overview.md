## ☁️ 1. Google Cloud Platform (GCP) Overview:-
🔹 GCP (Google Cloud Platform)
A cloud service by Google to run apps, store data, and use computing power online.

Offers tools for computing, databases, AI, networking, and storage.

🔹 Project
A logical container for GCP resources (APIs, storage, compute, etc.).

All billing, IAM, and services are tied to a project.

🔹 Terraform
Open-source tool for automating cloud infrastructure.

Manages GCP resources using code (Infrastructure as Code).

## 🔐 2. Access Control in GCP:-
🔹 IAM (Identity and Access Management)
Manages who can access what in GCP.

Provides fine-grained access control to resources.

🔹 Roles

  🔹Primitive Role: Broad access roles (Viewer, Editor, Owner).

  🔹Predefined Role: Service-specific roles like "Storage Admin" or "BigQuery Viewer".

  🔹Custom Role: User-defined roles with tailored permissions.

| Role      | ✅ Permissions                          | 🚫 Restrictions                       | 🎯 Use When                                  |
| --------- | -------------------------------------- | ------------------------------------- | -------------------------------------------- |
| 📄 Viewer | Can view content                       | Cannot edit, comment, or share        | You want someone to read only                |
| ✏️ Editor | Can view, comment, and edit            | Cannot delete, share, or manage roles | Collaboration is needed but no admin access  |
| 👑 Owner  | Full control over content and settings | —                                     | You created the content or need admin rights |

🔹 Service Account

Special Google account used by apps or VMs to access GCP services securely.

## 📊 3. API Services and Usage:-
Billing Based on Usage: Charges apply per use (compute time, storage, queries).
Billing Account: Needed to activate and pay for GCP services.

| **API Name**       | **Simple Explanation**                                                      |
| ------------------ | --------------------------------------------------------------------------- |
| **Dialogflow API** | Used to build chatbots and voice assistants that understand human language. |
| **Cloud SQL API**  | Lets you manage cloud databases like MySQL and PostgreSQL.                  |
| **BigQuery API**   | Helps you run fast queries on huge amounts of data.                         |
| **Vertex AI API**  | Used to build and run machine learning models easily.                       |
| **Cloud Run API**  | Runs your container apps and handles scaling automatically.                 |
| **Connectors API** | Connects GCP with other systems like Salesforce or databases.               |

## 🌐 4. Networking:-
🔹 Virtual Networking
Virtual Private Cloud (VPC) enables secure communication between resources.

Uses components like subnets, firewalls, and IP addresses.

🔹 VPC
A private, isolated network inside GCP.

Works like an online version of your own data center with full control.

🔹 Firewall
Filters traffic in and out of your GCP network.

Protects resources by allowing or denying traffic based on rules.

## 5. GCP Storage options:
| **Storage Type**     | **Description**                                                                              | **Types of Files Stored**                                                                                                 |
| -------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| **Object Storage**   | Stores unstructured data as objects (file + metadata). Ideal for backups, images, and media. | - **Images:** JPG, PNG, GIF <br> - **Videos:** MP4, AVI, MOV <br> - **Backups:** ZIP, TAR <br> - **Logs:** TXT, JSON, CSV |
| **Block Storage**    | Stores data in fixed-size blocks like a hard drive. Used for VM disks and databases.         | - **VM Files:** VHD, VMDK <br> - **Database Files:** MySQL, PostgreSQL <br> - **Log Files:** TXT, LOG                     |
| **File Storage**     | Provides a traditional file system with folders and directories. Best for shared access.     | - **Documents:** DOCX, PDF, TXT <br> - **Spreadsheets:** XLSX, CSV <br> - **Configuration Files:** JSON, YAML, INI        |
| **Database Storage** | Stores data in structured tables for relational databases.                                   | - **SQL Files:** .sql, .db <br> - **BigQuery Export Files:** CSV, JSON, Avro, Parquet                                     |

## 6. Integration Storage types:
| **Integration Type**         | **Description**                                                                       | **Example**                                                        |
| ---------------------------- | ------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| **Inside Cloud (Internal)**  | Integration **within GCP** services, offering secure and fast connections.            | Cloud Storage ↔ BigQuery <br> Cloud Pub/Sub ↔ Cloud Functions      |
| **Outside Cloud (External)** | Integration with **external systems** like on-prem services or third-party platforms. | GCP ↔ Salesforce (via APIs) <br> GCP ↔ On-prem databases (via VPN) |

## 7. When integrating pipelines from outside the cloud:
| **Mechanism**                   | **Description**                                                                |
| ------------------------------- | ------------------------------------------------------------------------------ |
| **REST APIs**                   | Used to send or retrieve data between external systems and GCP services.       |
| **Cloud VPN / Interconnect**    | Provides secure, direct network connectivity from on-premises to GCP.          |
| **Pub/Sub**                     | Enables real-time event/data streaming from external systems to GCP pipelines. |
| **SFTP/FTP (Batch Transfer)**   | Transfers large files in batches from external environments to Cloud Storage.  |
| **Cloud Functions / Cloud Run** | Offers HTTP endpoints to trigger serverless workflows from external systems.   |
| **Apache Airflow / Talend**     | Orchestrates and automates multi-step data workflows across platforms.         |
| **Kafka / Dataflow**            | Streams real-time data from external sources into GCP for processing.          |

 ## When to Use What:-
Use REST APIs for communication between systems.

Use VPN/Interconnect for secure, frequent data exchange.

Use Pub/Sub/Kafka for real-time streaming.

Use SFTP for batch uploads.

Use Cloud Functions for event-driven tasks.

## 8. ✅ Pipeline Mechanisms for Inside GCP:
| **Mechanism**                  | **Description**                                                                     |
| ------------------------------ | ----------------------------------------------------------------------------------- |
| **Cloud Composer (Airflow)**   | Orchestrates complex data pipelines using a managed Apache Airflow service.         |
| **Dataflow**                   | Used for real-time or batch data processing and transformation (Apache Beam).       |
| **Cloud Functions**            | Event-driven, lightweight functions to trigger pipelines (e.g., after file upload). |
| **Cloud Run**                  | Container-based execution of pipeline components triggered via HTTP.                |
| **Pub/Sub**                    | Event/message streaming to trigger other GCP services or steps in a pipeline.       |
| **Workflows**                  | Connects and automates GCP services into serverless workflows.                      |
| **BigQuery Scheduled Queries** | Automates data transformation and reporting inside BigQuery.                        |

 ## 🔄Use Case Example
Cloud Storage upload → triggers Cloud Function → publishes message to Pub/Sub → starts Dataflow → loads data into BigQuery.

These tools help automate, scale, and simplify your pipelines without needing external infrastructure.


