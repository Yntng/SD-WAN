# How to Configure Omada L3 Switch and Adopt on Omada Controller

1. **Assign IP Address**  
   Assign an IP address in the range of `192.168.0.1` to your computer's network interface to access the Omada L3 switch.

   ![Alt text](images/Pc-Ip-assigning.png)

2. **Access the Switch**  
   Open a browser and enter the switch IP address: `http://192.168.0.1`.

   ![Alt text](images/Browser-ip.png)

3. **Login**  
   The login page will appear. Log in with the default credentials:
   - Username: `admin`
   - Password: `admin`

    ![Alt text](images/default-login.png)

4. **Change Default Password**  
   Change the default password to a new, secure password of your choice.

   ![alt text](images/Change-password.png)

5. **Navigate to L3 Settings**  
   Go to the **L3** feature, located at the top of the home page.

   ![alt text](images/L3.png)

6. **Interface Settings**  
   From the left menu, go to **Interface Settings** and select **IPv4** for further configuration.

    ![alt text](images/Interface.png)

7. **Assign Static IP**  
   Assign a static IPv4 address to the switch, as planned, by selecting **Static IP**.

    ![alt text](images/Static.png)

8. **Save Configuration**  
   Apply and save the configuration changes.

    ![alt text](images/Assign-ip.png)

9. **Connect to Omada-Core-Switch**  
   Connect the L3 switch to your **Omada-Core-Switch**, which should already be connected to the Omada Controller.


10. **Login to Omada Controller**  
    Log in to the Omada Controller.

11. **Check Device List**  
    In the device list, you will see the new device trying to connect to your network.

     ![alt text](images/Adopt-1.png)

12. **Adopt the Switch**  
    Adopt the correct switch by clicking **Adopt**. You may need to click **Adopt** twice to ensure it is adopted on the second attempt. On the second attempt, you will be prompted to enter the login credentials of the remote switch.

     ![alt text](images/Adopt-2.png)


13. **Successful Connection**  
    After entering the credentials, the Omada L3 switch will be successfully connected to the network and controlled by the Omada Controller.

     ![alt text](images/Connect.png)

14. **Rename Switch**  
    Change the switch name as desired and apply the changes.

     ![alt text](images/L3-config-rename.png)
      ![alt text](images/Apply.png)

15. **Configure Remote Switch**  
    Now, you can access and configure the remote Omada L3 switch through the Omada Controller.

     ![alt text](images/L3-switch.png)
