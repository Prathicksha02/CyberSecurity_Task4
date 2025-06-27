# Task 4

## Objective:

Configure and test basic firewall rules to allow or block network traffic using **UFW (Uncomplicated Firewall)** in **Kali Linux**.

---

## Tools Used:

* **Kali Linux Terminal**
* **UFW - Uncomplicated Firewall**
* **Telnet for testing port blocking**

---

## Steps Followed:

### 1️⃣ Enable UFW Firewall:

sudo ufw enable

* Activates the firewall and sets it to start on system boot.

---

### 2️⃣ Check Current Firewall Rules:

sudo ufw status numbered

* Lists active rules with numbers for easy management.

---

### 3️⃣ Add Rule to Block Inbound Traffic on Port 23 (Telnet):

sudo ufw deny 23

* Blocks all inbound traffic to port 23, which is commonly used for Telnet connections.

---

### 4️⃣ Verify Rules:

sudo ufw status numbered

* Confirms that port 23 is blocked along with existing rules.

---

### 5️⃣ Test the Rule using Telnet:

telnet localhost 23

* **Expected Result:**
  `Connection refused` confirms that the firewall is blocking port 23 successfully.

---

### 6️⃣ Remove the Block Rule (Restore Original State):

sudo ufw delete deny 23

* Deletes the block rule for port 23 (IPv4 and IPv6 both).

---

### 7️⃣ Final Verification:

sudo ufw status numbered

* Ensures the block rule is removed and the firewall is back to its original state.

---

## Screenshots:
 Screenshot included here: Screenshots_task4.pdf

---

## Conclusion:

* Successfully blocked inbound traffic on port 23 using UFW.
* Verified blocking using Telnet test.
* Allowed SSH (port 22) remains enabled.
* Removed test rule to restore default firewall settings.

---

## How Firewall Filters Traffic:

A firewall acts as a security barrier that filters network traffic based on defined rules.

* It can **Allow** or **Deny** traffic based on ports, IP addresses, or protocols.
* Helps prevent unauthorized access to system services and enhances overall security.

---

