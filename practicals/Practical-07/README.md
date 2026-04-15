# 🧪 Practical 7: Install OpenStack (Local Environment)

## 🎯 Aim
To install and configure a local OpenStack environment using DevStack to understand Infrastructure as a Service (IaaS) components and management.

---

## 📖 Theory
OpenStack is a free, open-source cloud computing platform that provides Infrastructure as a Service (IaaS). It helps manage compute, storage, and networking resources through a dashboard or APIs.

### 🔑 Key Components
- **Keystone (Identity):** Authentication and authorization  
- **Nova (Compute):** Virtual machine management  
- **Neutron (Networking):** Network services (IP, routers, subnets)  
- **Glance (Image):** Stores VM images  
- **Horizon (Dashboard):** Web interface  
- **Cinder (Block Storage):** Persistent storage  

---

## 💻 System Requirements

| Resource   | Minimum Requirement | Recommended |
|------------|-------------------|------------|
| OS         | Ubuntu 22.04 LTS  | Ubuntu 24.04 LTS |
| Processor  | 2 Cores           | 4 Cores |
| RAM        | 8 GB              | 16 GB |
| Storage    | 20 GB             | 40 GB+ |
| Network    | Internet Access   | Static IP |

---

## 🔄 Operational Flowchart

```mermaid
graph TD
A[Start] --> B[Install Ubuntu Linux]
B --> C[Create 'stack' User with Sudo Privileges]
C --> D[Clone DevStack Repository]
D --> E[Create local.conf File]
E --> F[Run stack.sh Script]
F --> G{Installation Success?}
G -->|No| H[Troubleshoot]
H --> F
G -->|Yes| I[Access Horizon Dashboard]
I --> J[End]
