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

![s1-1](https://github.com/user-attachments/assets/a9645ba4-3e7f-40e2-b95b-4d9833c455b9)

2.       Configure ports and assign to correct VLAN according to the Addressing Table.

![s1-2](https://github.com/user-attachments/assets/724c3b4f-b82f-4540-8cf0-c6e85211121f)

![S1-2-2](https://github.com/user-attachments/assets/3a1b0118-2d72-4fb1-b7c4-50f8fd368e74)


3.       Configure the management interface VLAN 70 according to the Addressing Table.

![S1-3](https://github.com/user-attachments/assets/74ca1ae9-f23b-4243-8f97-463352891e46)
![S1-3-2](https://github.com/user-attachments/assets/1f337c3b-0e54-4a4e-958f-a263e446b4a6)


4.       Configure trunk port G0/1.

![S1-4](https://github.com/user-attachments/assets/ef7e1d2b-bf29-4cb8-aff5-d3aaa844c6d7)


MLS

     Note:  VLANs have been created on MLS according to the VLAN Table.

   5. Configure ports F0/1 and F0/2  and assign each to correct VLAN according to the Addressing Table.
   
![MLS-5](https://github.com/user-attachments/assets/a56e0d55-e4fd-4fff-bd3c-2e3df0364d78)


   6. Configure and activate the SVI interfaces for VLANs 50, 60, 70, and 100 according to the Addressing Table.

![MLS-6](https://github.com/user-attachments/assets/ad82e971-0402-4d88-9d56-efc3aa21ca75)

   7. Configure Trunking on MLS.
  
![MLS-7](https://github.com/user-attachments/assets/2ea89d32-d3e3-47a5-a93c-56bf04dd93b5)

   8. Enable routing.
   
![MLS-8](https://github.com/user-attachments/assets/78826d09-bbdd-4ca8-8e4e-4ec3255ded1f)


   9. Configure PCs with correct IP address, subnet mask, and default gateway.
  
![MLS-9](https://github.com/user-attachments/assets/16f92e64-470a-4f0c-8347-8ea517da7a2d)
![MLS-9-2](https://github.com/user-attachments/assets/209001f1-9f84-4d4e-b082-2cf615e5c338)

  10. Verify end-to-end connectivity between all PCs.

![MLS-10](https://github.com/user-attachments/assets/f8606932-a923-4f3c-a55c-0dd05109dbb5)


  11. Change the host name on both switches.

![MLS-11](https://github.com/user-attachments/assets/b4d7470f-e98d-472c-b97b-2e2eec89b676)


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

- Add DHCP and DNS configurations to simulate a more complete enterprise environment.


---

  

### **8. Project Conclusion**

  
- This project successfully demonstrated how to configure a **multi-VLAN network with Layer 3 routing**.

- All PCs were able to communicate across VLANs after proper configuration, and native VLAN issues were resolved.

- The lab strengthened my understanding of VLANs, trunking, and SVI-based routing in a simulated enterprise network.
