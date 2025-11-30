# Web Server / IIS + DNS Configuration & Setup

## DNS Manager Setup

1. Open **Server Manager**.
2. Go to **Tools → DNS**.
3. In **DNS Manager**, expand the server:
   - **Server:** `DC01-BBLS`
4. Expand **Forward Lookup Zones**.
5. Select the domain:
   - **bblsa.com**

---

## Testing DNS Resolution

To verify the DNS zone is working:

1. Open **Command Prompt** on the server or a client.
2. Run an `nslookup` query for the domain:


