### 1. Preparation

(1-1) First prepare two Raspberry Pi  EVBs and two SD cards.

(1-2) Install the Raspbian operating system on the SD card. The version we have tested is 2018-11-13-raspbian-stretch.

(1-3) Unzip the compressed file "build-Redundant_system_UI_v2-Desktop-Release.zip".

(1-4) Enter the folder "build-Redundant_system_UI_v2-Desktop-Release" and click Redundant system_UI_v2 to execute.![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image004.jpg)



(1-5) You will see the following window.

![https://scontent-tpe1-1.xx.fbcdn.net/v/t1.15752-9/60687272_2055783791200727_2160335414215311360_n.png?_nc_cat=107&_nc_ht=scontent-tpe1-1.xx&oh=5281270a9ab62decc97d266350a93ef3&oe=5D5A1B72](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image006.png)

 

### 2. Installation of related software

(2-1) First click install to install GlusterFS, DMTCP, and Watchdog respectively. It will take some time to install DMTCP. The screenshot is shown in the figure below.

![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image008.jpg)

 

(2-2) Click configuration to set the environment: static IP and GlusterFS.

**![https://scontent-tpe1-1.xx.fbcdn.net/v/t1.15752-9/60439423_873404076339972_3098403297258635264_n.png?_nc_cat=111&_nc_ht=scontent-tpe1-1.xx&oh=65b81a81cc4ed74af4a13812ec871e2b&oe=5D605488](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image010.png)**



![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image012.jpg)

 

 

 

**![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)**



NOTE: Remember to reboot after setting.

![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image016.png)

After rebooting, check whether the IP has been changed successfully

**NOTE: Both Raspberry Pi EVBs must be installed software and set static IP.**

 

 

### 3. Configuration of GlusterFS

(3-1) Choose which Raspberry Pi to use as the primary system.

(3-2) Select the primary system in the "Host" field, and fill the primary system IP and redundant system IP, and then click configuration->GlusterFS. The operations are similar in the redundant system.

NOTE: You should set the primary system first and then set the redundant system.

![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image017.png)

![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image019.jpg)

 

Use the "sudo gluster volume info command" to check whether the gluster setting is successful.

|      |                                                              |
| ---- | ------------------------------------------------------------ |
|      | ![img](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image021.jpg) |

 



### 4. Mode selection

(4-1) According to program property, select Mode-1 or Mode-2 in the field "Program type".

(4-2) Fill target program path that is supposed to be executed.

(4-3) The "checkpoint time" field is the time interval to execute a checkpointing.

NOTE: For the redundant system In Mode-2, you do not need to fill the target program path and checkpoint time

![https://scontent-tpe1-1.xx.fbcdn.net/v/t1.15752-9/60562383_291663781753009_5863743760592011264_n.png?_nc_cat=106&_nc_ht=scontent-tpe1-1.xx&oh=a500d980934bd56e41df8ab8a75d50da&oe=5D9F5E11](file:///C:/Users/pschen/AppData/Local/Temp/msohtmlclip1/01/clip_image023.png)

(4-4) Finally, click start to start to build the system automatically.

 

 

### 5. Other reminders

The program and installation data are in the file, but the protected program is provided by the user.

Thank you for using this function. You can also refer to demo.mp4 to view the function usage.

 

 

 

 

 