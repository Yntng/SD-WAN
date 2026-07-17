````markdown
# IP Phone Configuration Guide

## Objective
This document describes the steps required to configure an IP phone using a DHCP-assigned IP address and register it with the Alcatel OXO Connect IP PBX.

---

## Prerequisites

- IP phone connected to the network.
- DHCP service is available.
- Access to the Alcatel OMC application.
- Valid SIP extension details.
- Default IP phone login credentials.

---

## Configuration Steps

### 1. Verify DHCP IP Assignment

1. Connect the IP phone to the network.
2. Ensure the phone successfully obtains an IP address from the DHCP server.
3. Note the assigned IP address from the phone display or DHCP server.

---

### 2. Access the IP Phone Web Interface

1. Open a web browser.
2. Enter the DHCP-assigned IP address of the phone.
3. Log in using the default credentials:

![Alt text](images/login%20page.png)

| Parameter | Value |
|-----------|-------|
| **Username** | `admin` |
| **Password** | `123456` |

---

### 3. Configure Network Settings

Since the network uses **DHCP**, a static IP address is **not required**.

- Verify that the network mode is set to **DHCP**.
- No additional network configuration is necessary.
- Proceed to the SIP account configuration.

---

### 4. Configure the SIP Account

Navigate to:

**Account Settings**

Enter the following information:

| Field | Description |
|-------|-------------|
| SIP Server IP | IP address of the Alcatel OXO Connect PBX |
| Extension Number | Assigned SIP extension |
| Server Port | SIP server port |
| Authentication Password | SIP password obtained from Alcatel OMC |

![Alt text](images/SIP%20Account.png)

Save the configuration after entering all required information.

---

### 5. Retrieve the SIP Authentication Password

1. Log in to the **Alcatel OMC** application.
2. Navigate to:

   ```
   Subscribers / Base Stations
       └── Subscribers List
   ```

3. Locate the required extension.
4. Double-click the extension entry.
5. Open the **IP/SIP** section.
6. Under **SIP Parameters**, locate the **SIP Password**.
7. Copy the SIP Password.
8. Return to the IP phone web interface.
9. Paste the password into the **Authentication Password** field.

![Alt text](images/IP%20phone%20password.png)

---

### 6. Verify SIP Registration

1. Save and apply the configuration.
2. Verify that the SIP account status changes to:

```
Registered
```

![Alt text](images/registered.png)

If the status is not **Registered**, verify:

- SIP Server IP
- Extension Number
- Server Port
- Authentication Password
- Network connectivity

---

### 7. Test the Configuration

Perform the following tests:

- Place a call to another extension.
- Receive a call from another extension.
- Verify two-way audio.
- Confirm successful call establishment.

---

## Configuration Checklist

| Item | Status |
|------|--------|
| Phone received DHCP IP | ☐ |
| Web interface accessible | ☐ |
| DHCP mode enabled | ☐ |
| SIP Server configured | ☐ |
| Extension configured | ☐ |
| SIP Password configured | ☐ |
| SIP Account Registered | ☐ |
| Outgoing calls tested | ☐ |
| Incoming calls tested | ☐ |
| Two-way audio verified | ☐ |

---

## Expected Result

- The IP phone successfully registers with the Alcatel OXO Connect PBX.
- The extension status displays **Registered**.
- Users can make and receive internal and external calls according to the configured dialing permissions.
````
