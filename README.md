# Task 4 – Firewall Configuration and Testing (Windows)

## 📌 Objective
To configure and test basic firewall rules on **Windows Firewall** to allow or block specific network traffic, demonstrating firewall management and traffic filtering skills.

---

## 🛠 Tools Used
- **Windows Defender Firewall** (built-in tool)
- **Windows Command Prompt** (for testing)
- **Telnet Client** (installed via Windows Features)

---

## 🔹 Steps Performed

### 1️⃣ Viewed Existing Firewall Rules
- Opened **Windows Defender Firewall with Advanced Security** from the Control Panel.
- Navigated to **Inbound Rules** to check current configurations.
- 📸 *Screenshot 1:* Existing inbound firewall rules list.

### 2️⃣ Created a Rule to Block Port 23 (Telnet)
- Chose **Inbound Rules → New Rule → Port**.
- Selected **TCP** and specified **port 23**.
- Chose **Block the connection** and applied to **Domain, Private, Public** profiles.
- Named the rule **"Block Port 23 – Telnet"** and saved.
- 📸 *Screenshot 2:* New rule creation for blocking port 23.

### 3️⃣ Tested the Block Rule
- Enabled the **Telnet Client** feature:
  - Control Panel → Programs → Turn Windows features on/off → Check "Telnet Client".
- Tested by running:
  ```cmd
  telnet localhost 23
The connection failed, proving the rule works.

📸 Screenshot 3: Telnet test showing failed connection.

4️⃣ Removed the Test Rule
Returned to Inbound Rules.

Selected Block Port 23 – Telnet and deleted/disabled it.

📸 Screenshot 4: Rule removal step.

📷 Screenshots Included
step1_firewall_rules.png – Existing inbound rules list.

step2_block_port23.png – New rule creation wizard.

step3_telnet_fail.png – Failed Telnet connection test.

step4_remove_rule.png – Rule removal/disable step.

📚 Key Learnings
How to access and manage Windows Firewall with Advanced Security.

Understanding of inbound and outbound rules.

Why blocking insecure services like Telnet (Port 23) is important.

How to verify firewall rules using Telnet.

Restoring firewall configurations after testing to maintain normal network behavior.

❓ Interview Questions Practiced
What is a firewall?
A network security system that monitors and controls incoming and outgoing network traffic based on predetermined rules.

Difference between stateful and stateless firewalls?

Stateful: Tracks the state of active connections and makes decisions based on traffic context.

Stateless: Filters packets individually without tracking state.

What are inbound and outbound rules?

Inbound: Controls traffic coming into the system.

Outbound: Controls traffic going out of the system.

Why block port 23 (Telnet)?
Telnet transmits data unencrypted, making it insecure and vulnerable to interception.

Common firewall mistakes?

Leaving unnecessary ports open.

Not updating firewall rules.

Using overly permissive rules.

How does a firewall improve network security?
It acts as a barrier between trusted and untrusted networks, filtering unwanted traffic.

What is NAT in firewalls?
Network Address Translation allows multiple devices to share a single public IP while hiding internal IP addresses.

