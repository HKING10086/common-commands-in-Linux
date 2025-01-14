# Experiment 1st: common commands in Linux
group 6
## Purpose of the experiment
+ Be familiar with the use of VirtualBox virtual machines.

+ Be familiar with the Ubuntu operating system。

+ Master the commonly used Linux commands.
## Experimental equipment
+ Hardware:PC machine

+ Software:VietualBox virtual machine and Ubuntu operating system
## Experiment pre-study requirements
+ Read Section 1.3 about the installation and use of Linux.

+ Read Section 1.5 Linux Common Operation Commands.
## Experimental content
+ The use of virtual machine-based Linux operating system.

+ The use of commands related to files and directories.

+ Use of disk management and maintenance commands.

+ The use of system management and setting commands.
   
+ The use of network-related commands.

+ The use of compressed backup commands.
## Experimental Procedure
+ ### Use of the Linux operating system based on virtual machines
1.
+ ### Use of commands related to files and directories
1.
+ ### Use of commands related to Disk Management and maintenance
1.
+ ### Use of system administration and setting commands
1.
+ ### Use of network-related commands
#### 1. Displays information about the current network
Run the following command

`ifconfig`

The information of the current network can be displayed, and the operation result is shown in the figure

![img](./assets/5.5/info.png)

If the prompt as shown in the figure appears, you can run the command shown in the diagram to install the package and try again

`sudo apt install net-tools`

![img](./assets/5.5/install.png)

#### 2. Set the IP address
Run the following command

`ifconfig ens33 192.168.1.10`

You can set the IP address of ens33 to 192.168.1.10

If the following prompts appear

![img](./assets/5.5/error.png)

you can add `sudo` before the command to elevate the privilege, that is, run

`sudo ifconfig ens33 192.168.1.10`

After operation, the IP change is observable

![img](./assets/5.5/ip.png)

#### 3. Set the subnet mask
Run the following command

`ifconfig ens33 netmusk 255.255.255.0`

You can set the subnet musk of ens33 to 255.255.255.0

After operation, the subnet mask change is observable

![img](./assets/5.5/mask.png)

#### 4. Disable the NIC
Run the following command

`ifconfig ens33 down`

It can be observed that the NIC ens33 has been disabled

![img](./assets/5.5/down.png)

#### 5. Test network connectivity
Run the command

`ping 127.0.0.1`

The result is as follows

![img](./assets/5.5/ping.png)

This indicates that the local network loop is normal

#### 6. Enable the NIC
Run the command

`ifconfig ens33 up`

It can be observed that the NIC ens33 is enabled

![img](./assets/5.5/up.png)

#### 7. Displays the kernel routing table
Run the following command

`netstat -r`

The kernel routing table is displayed

The result is shown in the figure

![img](./assets/5.5/-r.png)

#### 8. Displays the TCP connection status
Run the following command

`netstat -t`

The TCP connection status is displayed

The result is shown in the figure

![img](./assets/5.5/-t.png)

#### 9. Displays the UDP connection status
Run the following command

`netstat -u`

The UDP connection status is displayed

The result is shown in the figure

![img](./assets/5.5/-u.png)


+ ### Use of the Compress Backup command
#### 1. Pack the/tmp directory into tmp.tar and place it in the/root directory.
Run the following command:

`tar cf /root/tmp.tar /tmp/*`

The result is shown in the figure



## Questions

**1**  

### Use the `ls` command to view the information under `/root` and redirect the result to save it into the `test.txt` file.

Run the following command:

`sudo ls /root/ `    

> View all files and subdirectory information under the /root directory.

`sudo ls /root > text.txt`

> Write the list of files in the /root directory to the test.txt file.

![屏幕截图 2024-09-12 174854](https://github.com/user-attachments/assets/e024507f-eaba-4d62-b714-0c85a97a1636)

**2**
###  Use disk management and maintenance commands to mount the USB drive to the virtual machine, and copy the `test.txt` file generated in question 1 to the USB drive.

Run the following command:

`sudo cp /tmp/test.txt /mnt/usb/`

> Copy the file test.txt from the /tmp directory to the USB drive.

`ls /mnt/usb`

> Check if the file has been successfully copied to the USB drive.

![屏幕截图 2024-09-12 182726](https://github.com/user-attachments/assets/292a3a10-c8c9-4ea0-9091-b40c4fb08c3e)
**3**
### Use `ifconfig` to change the IP address of `eth0` to `10.3.0.159` and modify the subnet mask to `255.0.0.0`.

Run the following command:

`sudo ifconfig enp0s3 10.3.0.159`

> change the IP address

`sudo ifconfig enp0s3 netmask 255.0.0.0`

> change the subnet mask

`ifconfig enp0s3`

> Verify the modification


![屏幕截图 2024-09-12 214530](https://github.com/user-attachments/assets/dc252c62-24cd-492d-b29c-42d3fcc19070)

**4**
### What is the difference between compression and archiving?

> 

**_Compression:_** _This refers to reducing the size of a file using specific algorithms. Common tools include gzip and bzip2. The compressed file is often a single file._

**_Archiving:_** _This involves combining multiple files or directories into a single file. A commonly used tool is tar. After archiving, the file size may not change, but it makes transmission and storage more convenient._
