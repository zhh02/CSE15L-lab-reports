# Week 2 Lab Report #1
## Installing VSCode
I have downloaded and installed VSCode for another course. If the VSCode is not downloaded yet, follow the instruction on VSCode website and install it according to your system:
(https://code.visualstudio.com/).
![Screenshot VSCode](https://github.com/zhh02/Week-2-Lab-Report/blob/main/VSCode.jpg)

## Remotely Connecting
First, check if the deviece has OpenSSH installed: if not, download at (https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). 
![Check OpenSSH](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Remote1_CheckSSH.jpg)
After having OpenSSH installed, find CSE15L account at (https://sdacs.ucsd.edu/~icc/index.php) and remember to reset your password following the instruction poste on piazza. Finally open powershell terminal and call the ssh cs15lwi22aar@ieng6.ucsd.edu and enter the password to log into course account. 
![Login](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Remote2_Login.jpg)

## Trying Some Commands
After logging into the course account, I called ls -lat and cd commands in the Powershell terminal. The outputs of commands are shown in the screenshot. 
![Commands](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Commands.jpg)

## Moving Files with scp
Create a WhereAmI.java file at local device with the following content: ```class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
} ```
Make sure you are at the directory of WhereAmI.java before running the scp command. Use the scp command to send WhereAmI.java to remote computer. After sending the file, log into the remote computer and should be able to compile and run WhereAmI.java successfully. 
![SCP](https://github.com/zhh02/Week-2-Lab-Report/blob/main/SCP.jpg)

## Setting an SSH Key
First call the ssh-keygen command on local client which creates public key and private key files.
![Key_1](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Key_1.jpg)
And then log into the remote server and call mkdir .ssh. After calling the mkdir command, log out and call scp to copy the public key file to the ssh directory.
![Key_2](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Key_2.jpg)
