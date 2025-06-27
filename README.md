# windows-firewall-configuration-testing


Steps Performed
**1. Open Firewall Configuration Tool**
Press Windows + R, type wf.msc, press Enter.

**2. List Current Firewall Rules**
Open Inbound Rules and Outbound Rules from the left pane.

**3. Add a Rule to Block Inbound Traffic on Port 23 (Telnet)**
Go to Inbound Rules → New Rule.
Select Port, click Next.
Choose TCP, specify port 23.
Select Block the connection.
Apply to desired profiles.
Name the rule Block Telnet Port 23.

**4. Test the Rule**
Install Telnet Client: dism /online /Enable-Feature /FeatureName:TelnetClient

Test with: telnet localhost 23
Expected Result: Connection fails if block rule is active.

**5. Add Rule to Allow SSH (Port 22)**
Follow same steps as above but: 
Port: 22
Action: Allow the connection
Name the rule Allow SSH Port 22

**6. Remove Test Block Rule**
Locate Block Telnet Port 23 under Inbound Rules.
Right-click and Delete.

**7. Summary: How Firewall Filters Traffic**
The Windows Firewall filters network traffic based on:
1. Port numbers
2. Protocols
3. Applications
4. IP addresses

**It blocks unauthorized access while permitting trusted communication, enhancing system security.**

**Screenshots**

![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/1.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/2.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/3.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/4.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/5.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/6.png)
![image alt](https://github.com/Amanranjan455/windows-firewall-configuration-testing/blob/2a0930e6519fe67e6e664a19d875836f3e8cebae/7.png)


