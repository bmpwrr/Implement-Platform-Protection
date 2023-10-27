# Implement-Platform-Protection
Introduction & Objective
- 
![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/606f7de3-ee8c-4a01-a327-d8bf652c3e2b)

Creating a robust virtual networking infrastructure is a fundamental step in modern IT environments, providing the agility and scalability needed to support the dynamic demands of today's applications and services. Within this virtual ecosystem, deploying virtual machines (VMs) plays a pivotal role, enabling organizations to harness the power of cloud computing and efficiently manage resources. However, the true measure of a well-designed network lies in its ability to secure and control the flow of data. Network filters, akin to sentinels of digital security, hold the key to fortifying these virtual networks. In this exploration, we embark on a journey to understand the intricacies of constructing a virtual networking infrastructure, setting up virtual machines within it, and rigorously testing the efficacy of network filters. This voyage is crucial not only for optimizing performance but also for ensuring the safety and integrity of the networked environment.

In this lab, our initial goal is to establish the virtual networking infrastructure. This endeavor involves a series of four essential tasks that we will systematically undertake: 

**Task 1:** Create a virtual network with one subnet.

**Task 2:** Create two application security groups.

**Task 3:** Create a network security group and associate it with the virtual network subnet.

**Task 4:** Create inbound NSG security rules to all traffic to web servers and RDP to the management servers.

Our second objective in this lab is to deploy virtual machines and rigorously test the network filters. To accomplish this, we will guide you through a sequence of four distinct tasks:

**Task 1:** Create a virtual machine to use as a web server.

**Task 2:** Create a virtual machine to use as a management server.

**Task 3:** Associate each virtual machines network interface to it’s application security group.

**Task 4:** Test the network traffic filtering.

Technologies, Azure Components, and Regulations Employed
- 
- Remote Desktop Protocol (RDP)
- PowerShell (in the Cloud)
- Virtual Machine (VM)
- Azure Network Security Guard (NSG)
- Azure Application Security Guard (ASG)
- Virtual Network (VNet)
- Engineered the Network's Infrastructure
- Test Network Filters

Exercise #1: Step by Step
-
1) Create a "Virtual Network" and name it "myVirtualNetwork".

![1](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/16a6de1e-e8d4-412f-ab20-4d390c447fbc)


2) Head over to "Application Security Group" and create 2 application security groups, one named "myAsgWebServers" and the other "MyAsgMgmtServers".

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/1f292f17-04b8-4f2e-bc01-804894d867b8)


![3](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/0ec6c0cf-37c2-4947-80fc-8f30c98c82b5)


![4](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/c13bb508-b566-471f-826a-cba3689bd025)


3) Once completed, head over to "Network Security Groups" and create a network security group, and name it "myNsg".

![5 (NETWORK, not application)](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/107ab6ca-65b6-45f5-af65-05c9651d9faf)


4) Once your "myNsg" is deployed, go to "Settings" >> "Subnets". Add an "Associate" subnet.

![6 (add NSG to myVirtualNetwork)](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/181376fd-434d-4f60-8e4a-22b70550da8e)


5) Now, we are going to create inbound NSG security rules to all traffic to web servers and RDP to the management servers.

![7](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/5ba09c13-7519-448d-8be3-c32fdb0d601e)

![8](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/84a8a15b-0b9f-411c-9ba0-af6f0d230898)

6) Now this is what you should have as your last step of exercise #1.

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/a934ac10-5194-4f65-bc8e-b0e39336e793)


Exercise #2: Step by Step
- 
1) Create a Virtual Machine (VM) as a web server and deploy it.

![10 (9)](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/44804187-c81f-41b2-bc67-b2ef6241d571)


![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/e6c2027f-6466-4f67-8007-bd0ba6b01e04)


2) Create a Virtual Machine (VM) as a management server and deploy it.

![11](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/b898062b-761a-468c-a15b-f6e0fde5141d)


![12](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/5771f2ae-ad7a-426d-9ad2-676459b00f0e)


3)  For the next task, we will associate each virtual machine's network interface to it's application security group. We will connect "myVmWeb" to "myAsgWebServers"

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/a3199c50-86da-4ae4-a25f-5a9ce9abd457)


![14](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/188db620-b70c-4326-a4fd-3cb9bf291bae)


4) Similar to step 3, we will associate "myVMMgmt" to "myAsgMgmtServers"

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/0db6c509-054b-426e-9764-8d9188f1926e)


![16](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/e9f0ddde-f21b-466f-8d57-00e79ed2dadc)


5) Now that we are finished with associating the virtual machine's to its proper application security group, we will now run these virtual machines to test the network filtering. For "myVMMgmt" we will RDP access it.

![17](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/f246b386-ae25-417d-bf53-2d41d4323df3)

Now, download the RDP file:

![18](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/b9711df6-2ab5-450f-b492-e2a24a21a716)


Once you download the RDP file and open it, you will need to enter the virtual machine's credentials. 

![19](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/76e7d6c1-7c4a-4d03-9787-2e9be651043c)

RDP (remote desktop protocol) connection was successful; at this point we have confirmed that we can connect via RDP to myVMMgmt


6) Now, we are to test if myVmWeb's network is online, via Bash.

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/4fc1b233-8414-499b-81fa-6895b089fac9)

Once you click "RunPowerShellScript", enter this code into the console:

![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/05fe92f2-eb54-4af7-ba88-66227f8b64ff)


This is how it should look completed:

![21](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/f7d17126-0abf-41b0-8df1-1b94e1b1f268)

We have successfully verify that we can access myVMWeb through HTTP/HTTPS.

7) Now that we have successfully proved that we can access this through HTTP/HTTPS, let's copy the IP address into our web browser. If all the steps are done correctly, this should be on your screen:

![22](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/b218a10e-2b65-470a-8001-6a11c8977b15)

Conclusion
- 
In contemporary IT environments, building a strong virtual networking infrastructure is a fundamental requirement. This infrastructure is crucial for meeting the dynamic needs of today's applications and services, providing the necessary agility and scalability. In this digital ecosystem, the deployment of virtual machines (VMs) is of paramount importance, as it enables organizations to make the most of cloud computing and resource management. However, the true test of a well-designed network lies in its ability to secure and manage data flow. Network filters, which act as digital security guardians, play a vital role in enhancing the security of virtual networks. Our journey in this exploration involves understanding the complexities of constructing a virtual networking infrastructure, setting up virtual machines, and rigorously testing network filters. This journey is not only essential for optimizing network performance but also for ensuring the safety and integrity of the interconnected digital environment.

In this lab, our primary objective is to establish the virtual networking infrastructure. This involves a series of four key tasks that we will systematically complete:

**Task 1:** Create a virtual network with a single subnet.

**Task 2:** Create two application security groups.

**Task 3:** Create a network security group and associate it with the virtual network subnet.

**Task 4:** Establish inbound Network Security Group (NSG) security rules to control traffic to web servers and Remote Desktop Protocol (RDP) access to management servers.

Our secondary objective in this lab is to deploy virtual machines and thoroughly test the network filters. To achieve this, we will guide you through a series of four specific tasks:

**Task 1:** Create a virtual machine for use as a web server.

**Task 2:** Create a virtual machine to serve as a management server.

**Task 3:** Associate the network interfaces of each virtual machine with their respective application security groups.

**Task 4:** Conduct a comprehensive assessment of network traffic filtering.




