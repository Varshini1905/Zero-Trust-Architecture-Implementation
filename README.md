# 🔐 Zero Trust Architecture Implementation  

## 📖 Overview  
This project demonstrates a **Zero Trust Architecture (ZTA)** using Cisco Packet Tracer and Python for access control simulation.  
The goal is to showcase **micro-segmentation, least privilege access, and automated policy enforcement** to secure an enterprise network.  

The implementation aligns with the **Zero Trust principles**:  
- Never trust, always verify  
- Enforce least privilege  
- Assume breach  

---

## 🏗️ Architecture Design  

### Key Components
- **Cisco Packet Tracer Network Topology**  
  - Segmented VLANs (HR, Finance, Engineering, Guest)  
  - Internal and external firewalls  
  - DMZ with public-facing services  

- **Access Control Policies**  
  - Role-based network segmentation  
  - Policy enforcement on critical servers  

- **Python-based Access Control Simulation**  
  - Script validates user/device access requests  
  - Deny by default unless explicit policy allows  

- **Identity & Authentication**  
  - Basic lab authentication with username/password  
  - Can be extended to MFA/SSO  

---

## ⚙️ Implementation Steps  

1. **Network Segmentation in Cisco Packet Tracer**  
   - VLANs created for each department  
   - Inter-VLAN routing restricted via firewalls  
   - Lateral movement between VLANs prevented  

2. **Firewall & ACL Rules**  
   - Access Control Lists defined for each VLAN  
   - Default deny, only required traffic permitted  
   - ACLs applied to router/firewall interfaces  

3. **Python Access Control Simulation**  
   - Custom script simulates role-based access  
   - Example: Only HR users can access HR server  
   - All other access attempts denied and logged   

4. **Micro-Segmentation Policies**  
   - East-west traffic restricted between VLANs  
   - Finance VLAN cannot access Engineering VLAN  
   - Guest network fully isolated from internal assets  

5. **Testing & Results**  
   - Verified VLAN isolation  
   - ACL rules tested for allowed vs denied flows  
   - Python script logged access attempts correctly  

---

## 📊 Demo Workflow  

1. User initiates access from endpoint  
2. Packet passes through firewall & ACL check  
3. Python script validates role and requested resource  
4. If match → access granted  
5. Otherwise → access denied and logged  

---

## 🚀 Future Enhancements  

- 🔑 Add **MFA (Multi-Factor Authentication)**  
- ☁️ Extend Zero Trust to **cloud workloads**  
- 🤖 Automate enforcement with **SOAR playbooks**  
- 📈 Build **SOC dashboards** for monitoring  

---

