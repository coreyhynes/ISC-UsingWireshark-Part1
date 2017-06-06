
<!---
Version: 1.0 
-->
# Install Wireshark
## INTRODUCTION MESSAGE
In this exercise, you will install Wireshark using an executable file previously downloaded from [https://www.wireshark.org](https://www.wireshark.org).
## COMPLETION MESSAGE
Congratulations, you have just installed Wireshark.
### Log on to WIN10
If necessary, log on to WIN10 using **Student** as the username and **Passw0rd!** as the password.





### Open downloads folder
From the taskbar, open **File** **Explorer,** and then navigate to the **Downloads** folder.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775087.PNG





### Launch Wireshark installler
In the Downloads folder, double-click **Wireshark-win64-2.2.6.exe**. In the User Account Control dialog box, click **Yes**.

#### :bulb: KNOWLEDGE
**NOTE:** To save time in the lab, this file was downloaded from [https://www.wireshark.org](https://www.wireshark.org). In a production envrionment, you should generally use the most recent version. Both 64-bit and 32-bit versions are available as well as versions that run on Linux distributions.





### Advance through setup wizard
On the Welcome to Wireshark 2.2.6 \)64-bit) Setup page, click **Next**. On the License agreement page, click **I Agree**. On the Choose Components page, accept the default settings, and click **Next**. On the Select Additional Tasks page, accept the defaults, and click **Next**. On the Choose Install Location page, accept default location and click **Next**. On the Install WinPcap page, accept default setting, and click **Next**. On the Install USBPcap, click **Install**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775129.PNG





### Advance through WinPcap 4.1.3 wizard
On the Welcome to the WinPcap 4.1.3 Setup Wizard page, click **Next**. On the License Agreement page, click **I Agree**.  Click **Install**. On the **Completing the WinPcap 4.1.3 Setup Wizard**, click **Finish**.  
  


#### :bulb: KNOWLEDGE
NOTE: To capture network traffic, WinPcap needs to be installed.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775130.PNG





### Complete Wireshark setup
On the Completing Wireshark 2.2.6 \)64-bit) Setup page, click check **Run Wireshark 2.2.6 \)64 bit)**, and click **Finish**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775206.PNG





### Leave Wireshark open
Leave Wireshark open for next exercise.






# Capture network traffic
## INTRODUCTION MESSAGE
In this exercise, you will learn how to capture network traffic.
## COMPLETION MESSAGE
Congratulations, you have just captured network traffic using Wireshark.
### Ensure Wireshark is open
Ensure Wireshark is running. If you closed it accidentally, click the **Action** icon \)lightning bolt) to the right of this instruction to launch the application.



#### :calling: COMMAND
```Shell
"C:\program files\wireshark\wireshark.exe"
```


### Select adapter
On the Welcome to Wireshark page, select **Ethernet**, as shown in the attached screen shot.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775256.PNG





### Open command prompt
Click the**Action** icon \)lightning bolt) to the right of this instruction to open the command prompt. Alternatively, right-click **Start**, and then **Command Prompt**.



#### :calling: COMMAND
```ShellWithUi
cmd.exe
```


### Start capture
Switch to the Wireshark application. On the top menu, click **Capture**, and then click **Start**.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775722.PNG





### Generate network traffic
At the command prompt, type **ping wirehsark.org**, and then press **ENTER**.





### Open Google Chrome
On the desktop, double-click the **Google Chrome** shortcut. Alternatively, click the **Action** icon to the right of this instruction.



#### :calling: COMMAND
```Shell
"C:\Program Files (x86)\Google\Chrome\Application\Chrome.exe"
```


### Stop capture
Switch to Wireshark. On the menu, click **Stop**, as shown in the attached screen shot.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/775867.PNG





### Leave Wireshark open for next task
Ensure you leave Wireshark open for the next exercise.






# Examine network traffic
## INTRODUCTION MESSAGE
In this exercise, you will examine the captured network traffic data. You will learn the elements of the Wireshark main windows and learn some basic techniques for locating and viewing captured data.
## COMPLETION MESSAGE

### Understand the main window
Review the attached screenshot and click the Knowledge icon \)head with lightbulb) to learn about the elements that comprise the main window.

#### :bulb: KNOWLEDGE
Wireshark's windows consists of the following parts:   

1. The **menu**. Used to start actions.
2. The**main toolbar**. Provides quick access to a subset of frequently used actions.
3. The **filter toolbar**. Used to filter the view to locate packets according to desired criteria.
4. The **packet list pane**. Displays summary of each packet that is captured.
5. the **packet details pane**. Displays data from packet selected in the list pane above.
6. The **packet bytes pane**. Displays data from the packet selected in the packet details pane above.



#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/776301.PNG
>* ShowAutomatically = Always





### Locate DNS traffic
In the packet list pane, locate and select the first instance of a packet that displays **DNS** in the protocol field.  DNS traffic occurs before the ping traffic because the host has to determine the IP address for **wireshark.org**. 

#### :bulb: KNOWLEDGE
**NOTE:** The attached screen shot may show slightly different data from the data you captured.  
  
Also note that  protocols are color-coded in the UI to make the data easier to view and interpret.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/776161.PNG
>* ShowAutomatically = No





### Locate ping traffic
In the packet list pane, locate and select the first instance of a packet that displays**ICMP** in the protocol field. Note the arrows on the left of the packet and the ICMP packet immediately following the first ICMP packet to indicate a query and response pair.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/776308.PNG





### Locate Google traffic
In the filter toolbar, type **udp contains google**, and press **ENTER**. Scroll through the results and examine the various application layer protocols that are displayed. These application layer protocols include DNS and others.

#### :bulb: KNOWLEDGE
**NOTE:** This filter expression locates all packets that use the  User Datagram Protocol \)UDP) at the transport layer, and contain the text string "google" in the data.   
  
Also note that the backbround of the filter changes color as you are typing to indicate valid or invalid filter expressions.

#### :camera: SCREENSHOT
>LODSProperties
>* Uri = screens/776309.PNG





### Locate QUIC traffic
In the filter toolbar, type **QUIC**, and press **ENTER**. Click the Knowledge icon to learn more about QUIC.

#### :bulb: KNOWLEDGE
Quick UDP Internet Connection \)QUIC) is an experimental protocol developed by Google to provide security and protection equivalent to TLS/SSL while improving performance. For more information, please see the [ QUIC Geek FAQ](https://docs.google.com/document/d/1lmL9EF6qKrk7gbazY8bIdvq3Pno2Xj_l_YShP40GLQE/edit).





### End lab
Click **Done** to finalize and close the lab.






