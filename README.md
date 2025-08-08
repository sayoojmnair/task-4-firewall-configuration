# Task 4 - Firewall Configuration and Rule Testing

## 🎯 Objective
To configure and test firewall rules in Windows Defender Firewall with Advanced Security to block Telnet (Port 23) and allow SSH (Port 22), ensuring proper network access control.

---

## 🧰 Tools Used
- **Windows 11** (Target System)
- **Windows Defender Firewall with Advanced Security**
- **Command Prompt** (for Telnet testing)

---

## 🔍 Steps Performed

### 1. Created Inbound Rule to Block Telnet
- Opened *Windows Defender Firewall with Advanced Security*.
- Selected **Inbound Rules → New Rule**.
- Chose **Port** as the rule type.
- Protocol: **TCP**, Local Port: **23**.
- Selected **Block the connection**.
- Applied to **Domain, Private, and Public** profiles.
- Named the rule **Block Telnet**.

### 2. Verified the Rule Properties
- Confirmed that protocol type was **TCP** and Local Port set to **23**.

### 3. Tested Telnet Connection
- Enabled Telnet Client from **Windows Features**.
- Ran:
  ```cmd
  telnet 127.0.0.1 23

The connection failed as expected, confirming that the block rule worked.

### 4. Created Inbound Rule to Allow SSH (Optional)
- Selected **New Rule → Port**.
- Protocol: **TCP**, Local Port: **22**.
- Chose **Allow the connection**.
- Applied to **All Profiles**.
- Named the rule **Allow SSH**.

### 5. Removed the Telnet Rule
- Located **Block Telnet** in Inbound Rules.
- Right-clicked and chose **Delete**.
- Confirmed removal.
- Verified in the inbound rules list that **Block Telnet** no longer appeared.

---

## 📷 Screenshots
Screenshots included in `/screenshots/`:

1-firewall-inbound-rules.png – Inbound rules list showing Block Telnet.

2-block-telnet-properties.png – Block Telnet properties showing TCP port 23.

3-block-telnet-name.png – Wizard “Name” step for Block Telnet rule.

4-telnet-connection-failed.png – Telnet connection failure in Command Prompt.

5-allow-ssh-name.png – Wizard “Name” step for Allow SSH rule.

6-allow-ssh-properties.png – Allow SSH properties showing TCP port 22.

7-delete-block-telnet.png – Confirmation dialog for deleting Block Telnet rule.

---

## 📄 Files in this Repository
- `README.md` — Documentation of the process.
- `/screenshots/` — Folder containing all screenshots.

---

## ✅ Conclusion
The firewall was successfully configured to block Telnet access and allow SSH traffic. Testing confirmed that the block rule was effective, preventing connections on port 23. The optional SSH rule allowed secure remote access. Finally, the Telnet block rule was removed to demonstrate rule management. These configurations help in securing the system by controlling access to specific ports and protocols.
