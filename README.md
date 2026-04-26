# azure-public-blob-storage-project
This project demonstrates the deployment of a public Azure Blob Storage solution using the Microsoft Azure Portal. It simulates a real-world DevOps scenario where data is migrated to cloud storage and exposed via controlled public access.
The implementation includes:
Storage account creation
Public Blob container configuration
Anonymous access enablement
Validation of public file access

Architecture

```mermaid
flowchart TD
    A[User / Internet] --> B[Public URL Access]
    B --> C[Azure Storage Account: nautilusst24014]
    C --> D[Blob Container: nautilus-blob-8431]
    D --> E[Stored Objects / Files]

 Implementation Steps

Storage Account Creation

* Name: `nautilusst24014`
* Tier: Standard
* Redundancy: LRS

---
2. Security Configuration

* Enabled: **Allow anonymous access on individual containers**
* HTTPS enforced (secure transfer enabled)
* Default settings retained for lab environment

---
 3. Blob Container Setup

* Container name: `nautilus-blob-8431`
* Access level:

  *Container (anonymous read access for containers and blobs)*

---

4. Validation

* Uploaded test file
* Accessed file via public URL
* Confirmed anonymous browser access

---

Security Notes

While this configuration enables public access, it should NOT be used for sensitive workloads.

Risks:

* No authentication required
* Public data exposure risk

 Best Practices:

* Use private containers in production
* Implement SAS tokens for controlled sharing
* Enable RBAC for access control
* Use private endpoints for secure architectures

---

 Real-World Use Cases

* Hosting static assets (images, files)
* Public datasets distribution
* Temporary file sharing
* Web application asset storage

---

Skills Demonstrated

* Azure Storage Account provisioning
* Blob Storage configuration
* Public access management
* Cloud security configuration
* DevOps lab execution

---

 Outcome

Successfully deployed a public cloud storage solution with verified anonymous access, demonstrating practical Azure storage and security configuration skills.


