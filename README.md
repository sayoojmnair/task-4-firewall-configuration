Task 4 - Firewall Configuration and Rule Testing
🎯 Objective
To configure and test firewall rules in Windows Defender Firewall with Advanced Security to block Telnet (Port 23) and allow SSH (Port 22), ensuring proper network access control.

🧰 Tools Used
Windows 11 (Target System)

Windows Defender Firewall with Advanced Security

Command Prompt (for Telnet testing)

🔍 Steps Performed
1. Created Inbound Rule to Block Telnet
Opened Windows Defender Firewall with Advanced Security.

Selected Inbound Rules → New Rule.

Chose Port as the rule type.

Protocol: TCP, Local Port: 23.

Selected Block the connection.

Applied to Domain, Private, and Public profiles.

Named the rule Block Telnet.

2. Verified the Rule Properties
Confirmed that protocol type was TCP and Local Port set to 23.

3. Tested Telnet Connection
Ran:

cmd
Copy
Edit
telnet 127.0.0.1 23
Connection failed as expected, confirming the block rule worked.

4. Created Inbound Rule to Allow SSH (Optional)
Selected New Rule → Port.

Protocol: TCP, Local Port: 22.

Chose Allow the connection.

Applied to All Profiles.

Named the rule Allow SSH.

5. Removed the Telnet Rule
Located Block Telnet in Inbound Rules.

Right-clicked and chose Delete.

Confirmed removal.

📷 Screenshots
Screenshots of:

Creating the Block Telnet rule.

Rule properties showing TCP port 23.

Telnet connection failure in Command Prompt.

Creating the Allow SSH rule.

Deleting the Block Telnet rule.

📄 Files in this Repository
README.md — Documentation of the process.

/screenshots/ — Folder containing all screenshots.

firewall-task4.pdf — Exported PDF report (if required).

✅ Conclusion
The firewall successfully blocked Telnet access and allowed SSH traffic as configured. Testing confirmed that the block rule was effective, and rule management was verified by removing the Telnet rule after testing.
