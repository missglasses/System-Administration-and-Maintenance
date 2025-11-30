# Print Server Configuration

## Install Print and Document Services Role

1. Open **Server Manager**.
2. Select **Add Roles and Features**.
3. In **Server Roles**, check:
   - **Print and Document Services**
4. When prompted, click **Add Features**.
5. In **Role Services**, check:
   - **Print Server**
6. Continue through the wizard and complete the **installation**.

---

## Configure Print Management

1. After installation, open:
   - **Tools → Print Management**
2. In the Print Management console:
   - Expand **Print Servers**
   - Select your server
   - Expand **Printers**
3. Right-click **Printers** → **Add Printer**

---

## Add a Printer (Wizard Steps)

1. Choose:
   - **Add a new printer using an existing port**
2. Select the port:
   - **LPT1:** (Printer Port)
3. Continue and choose:
   - **Install a new driver**
4. Set the **Printer Name:** `LabPrinter`
5. Check:
   - **Share this printer**
   - **Share name:** `LabPrinter`
6. Click **Finish**.

---

## Printer Properties

1. Right-click **LabPrinter** → **Printer Properties**
2. Go to the **Sharing** tab.
3. Confirm:
   - **Share this printer** is checked
   - **Share name:** `LabPrinter`
4. Apply and exit.

---

## Client Verification

1. On a client machine:
   - Press **Win + R**
   - Type:  
     ```
     \\dc01-bblsa
     ```
   - Press **Enter**
2. The shared printer **LabPrinter** should appear.
3. Open **Control Panel → View Devices and Printers**.
4. Locate **LabPrinter**.
5. Right-click → **Set as default printer**.
6. Open **Printer Properties** → Click **Print Test Page**.

---

## Manual Test Print

1. Open **Notepad**.
2. Type anything (e.g., “Test print from client”).
3. Go to **File → Print**.
4. Select **LabPrinter**.
5. Print the document.
6. In **LabPrinter’s print queue**, confirm the job appears:
   - If the Notepad print job is visible and completes, the test is successful.

---
