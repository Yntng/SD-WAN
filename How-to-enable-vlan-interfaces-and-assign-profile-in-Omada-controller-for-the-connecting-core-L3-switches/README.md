
# Omada Controller and Network Configuration Guide

Follow these steps to configure the Omada Controller, Core Switch, and Firewall-Router for network setup:

## 1. Log in to the Omada Controller
Open your browser and log in using the IP address of your Omada controller.
- Username: `admin`
- Password: `*****`

Once logged in, navigate to the **Your site** section in the dashboard.

![Alt text](images/Omada-devices.png)

## 2. Select "Devices" and Choose the Core Switch
In the **Devices** tab, locate and select the **Core Switch** you want to configure.

![Alt text](images/Core-switch.png)


## 3. Go to "Config" and Open "VLAN Interfaces"
In the Core Switch settings, click on the **Config** tab, then select **VLAN Interfaces**.
Choose the department you’re working on, and click **Edit** to modify the settings.

![Alt text](images/core-config-edit.png)


## 4. Assign Static IP and Enable DHCP
Set a **static IP address** for the local network and provide the subnet mask. Then, enable the **DHCP Server**.
Define the **DHCP range** and specify the DNS settings as required.

![Alt text](images/core-dhcp-switch.png)


## 5. Apply the Changes
After configuring the IP and DHCP settings, click **Apply** to save the changes.

![Alt text](images/core-dhcp-apply.png)

## 6. Return to "Devices" and Select the L3 Switch
Go back to the **Devices** tab and select the **L3 Switch** for the department you are configuring.

![Alt text](images/dept-switch.png)

## 7. Enable VLAN Profiles
Go to the **Configure** section, then open **VLAN** settings. Enable the following profiles: and apply changes
- **Default**
- **Hotspot**
- **[Department Name Profile]**

![Alt text](images/dept-switch-config.png)
![Alt text](images/dept-config2.png)

## 8. Configure Switch Ports
Go to the **Port** section, select the desired port, and click **Edit Selection**. Assign the correct profile to the remaining ports as needed.

![Alt text](images/swith-port-profile-enable.png)

## 9. Apply Port Configurations
After configuring the ports, click **Apply** to save the changes.

![Alt text](images/switch-port-profile2.png)
![Alt text](images/port-apply.png)

## 10. Computer Receives DHCP IP (No Internet)
Your connected computer will now receive an IP from the switch via DHCP but won’t have internet access yet.

![Alt text](images/DHCP.PNG)

## 11. Configure Routing on the Firewall Server
To enable internet access, you must configure routing on your **Firewall Server** to route traffic from the switch to the internet.


## 12. Using RB 450G as the Firewall Router
For this setup, we’re using the **RB 450G** as the **Sophos Firewall Router**, which acts as the firewall server.


## 13. Log in to RB 450G via Winbox
Open **Winbox** and log in to the **RB 450G** router.

![Alt text](images/Login-winbox.png)

## 14. Navigate to Routes in Winbox
Go to **IP** > **Routes** in the Winbox menu.

![Alt text](images/Ip-route.png)

## 15. Add a Routing Entry
Click the **Add** button in the top-left corner. Enter the **destination IP** and the gateway for routing traffic to the network. Then, click **Apply** and  **save**.

![Alt text](images/add-route.png)
![Alt text](images/route-ip-address.png)

## 16. Internet Access Available
After the route is added, you will now have internet access from your network through the configured switch and firewall.

![Alt text](images/ping%20response.png)