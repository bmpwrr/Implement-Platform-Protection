# Implement-Platform-Protection
Introduction
- 
asd

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

Exercise #2: Step by Step
- 
1) Create a Virtual Machine (VM) and deploy it.

![10 (9)](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/44804187-c81f-41b2-bc67-b2ef6241d571)


![image](https://github.com/bmpwrr/Implement-Platform-Protection/assets/144153997/e6c2027f-6466-4f67-8007-bd0ba6b01e04)


2) 
