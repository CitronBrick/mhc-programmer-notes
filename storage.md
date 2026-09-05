# Storage as a Service


## AWS Simple Storage Service S3

* object storage service
* scalability
* availability
* security
* performance
* read-write consistency post PUT/DELETE

### Access management & security

* default public access blocked
* IAM
* Bucket policies
* S3 access points
* ACLs


### Logging

* Automated
	* CloudWatch
	* CloudTrail
* Manual
	* Server access logging
	* AWS Trusted Advisor

### S3 Storage classes

#### Frequent

* **S3 Standard** (default)
* **S3 Express One Zone** 
	* fastest (< 10ms)
	* 1 AZ
* **Reduced Redudancy** (not recommended)

#### Unknown frequency (Automatic tiering)

* **S3 Intelligent Tiering** : Frequent, Infrequent, Archive Instant, Archive, Deep Archive tiers

#### Infrequent

* **S3 Standard IA**
* **S3 One Zone IA** : supplement with AWS Local Zone, Cross Region Replication

#### Rarely accessed

* **S3 Glacier Instant Retrieval (GLACIER_IR)** : ms retrieval
* **S3 Glacier Flexible Retrieval (GLACIER)** : min retrieval, **no real time access**
* **S3 Glacier Deep Archive (DEEP_ARCHIVE)** : **no real time access**

## Google Cloud Storage (GCS)

* encrypted at rest

### GCS Storage Classes

1. **RAPID** (1 TiB limit)
2. **STANDARD**
3. **NEARLINE** (>= 30 days, needs payment)
4. **COLDLINE** (>= 90 days, needs payment)
5. **ARCHIVE**  (>= 180 days, needs payment)
6. **Autoclass** (intelligent)

## Azure Storage

* encrypted at rest

* **Azure Blobs** : text & binary data. Support for *data analytics* via **Data Lake Storage**
* **Azure Files** : Managed File Shares for On-Prem deployments
* **Azure Elastic SAN** : *fully integrated* solution to deploy; scale; manage **Storage Area Network** (SAN)
* **Azure Queues** : message store for reliable messaging between app components
* **Azure Tables** : NoSQL store for **schemaless** storage of structured data
* **Azure Managed Disks** : Block level storage volumes for Azure VMs
* **Azure Container Storage** : *native* volume management, deployment & orchestration service for containers
* **Azure NetApp Files** : Enterprise file storage (powered by NetApp) to migrate/run complex file based apps with no code change
* **Azure Managed Lustre** : **Distributed Parallel File System** ideal for HPC workloads (high throughput, low latency)

### Azure Access Tiers

1. **Hot** 
2. **Cool** (>= 30 days)
3. **Cold** (>= 90 days)
4. **Archive** (>= 180 days)
5. **Smart** (intelligent)

### Azure Blob Storage

* for unstructured data
* 3 components
	1. Storage accounts
		* unique namespace
		* every object has address including unique namespace
		* default: `http://<namespace>.blob.core.windows.net`
		* types:
			* **General-purpose v2** : fileshares, blobs, queues, tables
			* **Block blob** : premium storage account type for Block blobs and Append Blobs
			* **Page blob** : premium storage account type for Page blobs only

#### Blob types

* Block Blob 
	* text & binary data
	* managed individually
	* < 190.7 TiB (**TiB = Tebibyte = 2^40 bytes**)
* Append Blob 
	* like block blobs
	* optimized for append
	* ideal for VM logging
* Page blob
	* Virtual Hard Drive (VHD) files serving as disks for Azure VM
	* random files <= 8 TiB