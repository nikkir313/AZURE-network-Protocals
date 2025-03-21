# AZURE-network-Protocals<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>
**Step 1: Create and Configure Azure Virtual Machines**  
- Deploy two **Azure Virtual Machines (VMs)** within the same **Virtual Network (VNet)**.  
- Verify that both VMs can communicate **before applying NSG rules**.  

![Azure VM Setup](placeholder-image-link-1.jpg)  

### **Step 2: Create and Associate a Network Security Group (NSG)**  
- Create an **NSG** from the **Azure Portal** or **Azure CLI**.  
- Associate the NSG with either:  
  - The **Subnet** (affecting all VMs in the subnet).  
  - The **Network Interface (NIC)** (affecting only a specific VM).  

![NSG Association](placeholder-image-link-2.jpg)  

### **Step 3: Configure Inbound and Outbound Rules**  
- Define **custom security rules** to allow or deny traffic.  
- Example configurations:  
  - Allow **RDP (3389) or SSH (22)** access.  
  - Deny specific ports (e.g., block all HTTP traffic).  

![NSG Rule Configuration](placeholder-image-link-3.jpg)  

### **Step 4: Inspect and Monitor Traffic Flow**  
- Use **Azure Network Watcher → NSG Flow Logs** to monitor traffic.  
- Test connectivity with `ping`, `telnet`, or `curl` commands to validate rule enforcement.  
- Identify dropped packets and troubleshoot connectivity issues.  

![Traffic Monitoring](placeholder-image-link-4.jpg)  

## **Conclusion**  
Network Security Groups (NSGs) provide granular control over **inbound and outbound traffic** between Azure VMs. Using **Azure Network Watcher**, administrators can inspect traffic flow, optimize security rules, and troubleshoot connectivity issues.  

---

### **Code Snippet for Images**  
Replace `placeholder-image-link-X.jpg` with the actual image URLs or paths.  

---
