# DHCP Configuration Notes

## Server Setup

1. **After installing DHCP**, click **"Complete DHCP configuration"**.
2. In the **DHCP Post-Install Wizard**:
   - Go to **Authorization**
   - Select **"Use the following user credentials"**
   - Example credentials:
     - **Username:** `BBLSA\Administrator`

## Accessing the DHCP Console

1. Open **Server Manager**
2. Navigate to **Tools → DHCP**
3. Expand the **DHCP Server** and then **IPv4**

## Creating a New Scope

1. Right-click **IPv4** → **New Scope**
2. Provide scope details:
   - **Name:** `BBLSA-scope`
3. Configure IP address range:
   - **Start IP:** `192.168.1.50`
   - **End IP:** `192.168.1.200`
   - **Subnet Mask Length:** `/24`
   - **Subnet Mask:** `255.255.255.0`
4. Keep the **lease duration** at:
   - **8 days**
5. Continue with configuration:
   - Select **"Yes, I want to configure these options now"**

Router or Firewall

- **Router (Default Gateway):** `192.168.1.1`
- **DNS Server:** `192.168.1.10`
- **Parent Domain:** `bblsa.com`

After entering the information:
- Select **"Yes, I want to activate this scope now"**.

---

## Client Verification

To verify DHCP is working on a client machine:

1. Open **Command Prompt**.
2. Run:
   - `ipconfig /release`
   - `ipconfig /renew`
3. Confirm the client receives:
   - An IP address in the correct range: `192.168.1.50 – 192.168.1.200`
   - The correct **Default Gateway:** `192.168.1.1`
   - The correct **DNS Server:** `192.168.1.10`
   - The correct **Domain Suffix:** `bblsa.com`

4. Optionally confirm with:
   - `ipconfig /all`
   - Check lease obtained/expiration times.

