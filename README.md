# Inter-VLAN-Routing-Project

---

  

### **1. Project Overview**

  

- The goal of this project was to explore inter-VLAN routing by building and configuring one mimicking a small office network. I used Packet tracer to build, configure and analyze this network, simulating potential real-world scenarios. This projects comes with screenshots detailing each steps I've taken.


---

  

### **2. Objectives**

  

- The objective was to identify and understand inter-VLAN routing by configuring VLANs and ports for the network, analyzing any mistakes done along the way and addressing them. I aimed to enhance my knowledge of Networking with this project and improve my ability to configure and build network.

  
---

  

### **3. Project Setup**

  

- The lab was set up using packet tracer running to simulate real-world network conditions. Specific configurations included network settings, IP configurations and CLI use to mirror practical scenarios.

  

---

  

### **4. Steps and Approach**

  
S1

1.       Create and name VLANs on the layer 2 switch (S1) according to the VLAN Table.
![[Pasted image 20250612122016.png]]
2.       Configure ports and assign to correct VLAN according to the Addressing Table.
![[Pasted image 20250612122022.png]]
![[Pasted image 20250612122038.png]]

3.       Configure the management interface VLAN 70 according to the Addressing Table.

![[Pasted image 20250612122046.png]]
![[Pasted image 20250612122057.png]]

4.       Configure trunk port G0/1.

![[Pasted image 20250612122110.png]]


MLS

     Note:  VLANs have been created on MLS according to the VLAN Table.

   5. Configure ports F0/1 and F0/2  and assign each to correct VLAN according to the Addressing Table.
   
![[Pasted image 20250612122120.png]]

   6. Configure and activate the SVI interfaces for VLANs 50, 60, 70, and 100 according to the Addressing Table.

![[Pasted image 20250612122131.png]]

   7. Configure Trunking on MLS.
  
![[Pasted image 20250612122140.png]]

   8. Enable routing.
   
![[Pasted image 20250612122219.png]]


   9. Configure PCs with correct IP address, subnet mask, and default gateway.
  
![[Pasted image 20250612122513.png]]  
![[Pasted image 20250612122553.png]]

  10. Verify end-to-end connectivity between all PCs.

![[Pasted image 20250612122605.png]]


  11. Change the host name on both switches.

![[Pasted image 20250612122618.png]]


---

  

### **5. Challenges and Solutions**

  
- Native VLAN Mismatch:
  A mismatch error occurred on trunk ports due to different native VLANs (1 vs. 50). This was resolved by explicitly configuring the native VLAN to match on both sides with: switchport trunk native vlan 50

- Routing Issues:
  Initial failure in routing was due to not enabling ip routing on the MLS. Once added, PCs across VLANs were able to communicate.

---

  

### **6. Key Learnings and Takeaways**

  

- Gained hands-on experience in setting up Inter-VLAN routing using SVI interfaces.

- Learned the importance of trunk configuration and native VLAN matching.

- Understood how to configure default gateways on PCs to ensure proper routing.

- Practiced identifying and resolving common Layer 2 and Layer 3 issues in network segmentation.
  

---

  

### **7. Future Improvements**

- Automate part of the configuration using CLI scripts to reduce setup time.

- Expand the lab to include router-on-a-stick setup for comparison.

- Add DHCP and DNS configurations to simulate a more complete enterprise environment.


---

  

### **8. Project Conclusion**

  
- This project successfully demonstrated how to configure a **multi-VLAN network with Layer 3 routing**.

- All PCs were able to communicate across VLANs after proper configuration, and native VLAN issues were resolved.

- The lab strengthened my understanding of VLANs, trunking, and SVI-based routing in a simulated enterprise network.
