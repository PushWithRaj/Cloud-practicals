# Practical 3: Set Up a Virtual Private Cloud (VPC)

## Aim

To design and implement a custom Virtual Private Cloud (VPC) with isolated network tiers (Public and Private), enabling secure communication through Internet and NAT Gateways.

---

## Theory

Amazon VPC allows you to provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including selection of IP address range, creation of subnets, and configuration of route tables and network gateways.

**Public Subnet:**  
A subnet that has a direct route to an Internet Gateway (IGW). Resources here are reachable from the public internet.

**Private Subnet:**  
A subnet that does not have a route to the IGW. Resources are protected from the public internet but can access it via a NAT Gateway.

**NAT Gateway:**  
A Network Address Translation service that allows instances in a private subnet to connect to services outside your VPC (like software updates) but prevents external services from initiating a connection with those instances.

---

## VPC Architecture Table

| Component | CIDR / Configuration | Purpose |
|------------|----------------------|----------|
| VPC CIDR | 10.0.0.0/16 | The primary IP range for the entire network. |
| Public Subnet | 10.0.1.0/24 | Hosts the Web Server and NAT Gateway. |
| Private Subnet | 10.0.2.0/24 | Hosts the Database/App Server. |
| Internet Gateway | Attached to VPC | Provides internet access for the Public Subnet. |
| NAT Gateway | Placed in Public Subnet | Routes traffic from Private Subnet to Internet. |

---

## Operational Flowchart

```mermaid
graph TD
    A[Start: Create VPC] --> B[Create Public & Private Subnets]
    B --> C[Create & Attach Internet Gateway]
    C --> D[Create NAT Gateway in Public Subnet]
    D --> E[Configure Route Tables]
    E --> F[Route Public Subnet to IGW]
    F --> G[Route Private Subnet to NAT Gateway]
    G --> H[Launch EC2 Instances in both Subnets]
    H --> I[Test Connectivity]
    I --> J[End]
```

---

## Routing Table Configurations

### 1. Public Route Table

| Destination | Target |
|-------------|--------|
| 10.0.0.0/16 | Local |
| 0.0.0.0/0 | igw-xxxxxxxx (Internet Gateway) |

### 2. Private Route Table

| Destination | Target |
|-------------|--------|
| 10.0.0.0/16 | Local |
| 0.0.0.0/0 | nat-xxxxxxxx (NAT Gateway) |

---

## Code Section: Connectivity Test (Linux)

### Verify Public Subnet Instance Internet Access

```bash
# Run on Public Instance
ping google.com
```

### Verify Private Subnet Instance Internet Access (via NAT)

```bash
# Run on Private Instance
curl -I https://www.amazon.com

# Note: You must SSH into the Public instance first,
# then SSH into the Private instance using its internal IP.
```

---

## Conclusion

A multi-tier network architecture was successfully established. The Public Subnet was configured for external accessibility via an Internet Gateway, while the Private Subnet remained isolated, gaining secure outbound-only internet access through the NAT Gateway.
