 #Cyber Security Internship – Task 4: Firewall Setup and Testing (Windows)
# Objective
The main goal of this task was to learn how to set up and test firewall rules using Windows Defender Firewall. Specifically, the task focused on blocking traffic through Telnet (port 23) and checking whether the block was successfully applied.

🖥#System Used
Here’s the setup used for this task:

Operating System: Windows 10

Firewall Tool: Windows Defender Firewall with Advanced Security

Testing Tools: Command Prompt and Telnet Client

#Steps Taken
Step 1: Enabling the Telnet Client
To begin with, I needed to enable the Telnet client since it’s not active by default in Windows. Here’s how I did it:

Opened the Control Panel

Navigated to Programs → Turn Windows features on or off

Checked the Telnet Client option and clicked OK

This allowed me to test traffic on port 23 using the command line.

Step 2: Creating a Firewall Rule to Block Port 23
Next, I set up a firewall rule to block any traffic coming in through port 23 (which Telnet uses):

Opened Windows Defender Firewall with Advanced Security

Went to Inbound Rules → New Rule

Chose the following options:

Rule Type: Port

Protocol: TCP

Port Number: 23

Action: Block the connection

Applied the rule to Domain, Private, and Public profiles

Named the rule: Telnet block

Step 3: Testing the Firewall Rule
To confirm the rule was working, I tested it by running this command in Command Prompt:
telnet localhost 23
Since the firewall rule was in place, the connection attempt failed — just as expected. This confirmed that traffic on port 23 was successfully blocked.
