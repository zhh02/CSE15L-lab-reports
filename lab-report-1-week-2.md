# Week 2 Lab Report #1
## Installing VSCode
I have downloaded and installed VSCode for another course. If the VSCode is not downloaded yet, follow the instruction on VSCode website and install it according to your system:
[VSCode download page](https://code.visualstudio.com/).
![Screenshot VSCode](https://github.com/zhh02/Week-2-Lab-Report/blob/main/VSCode.jpg)

## Remotely Connecting
First, check if the device has OpenSSH installed: if not, download at [OpenSSH download page](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse). 
![Check OpenSSH](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Remote1_CheckSSH.jpg)
After having OpenSSH installed, find CSE15L account at [Accound page](https://sdacs.ucsd.edu/~icc/index.php) and remember to reset your password following the instruction poste on piazza. Finally open powershell terminal and call ```ssh cs15lwi22aar@ieng6.ucsd.edu``` and enter the password to log into course account. 
![Login](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Remote2_Login.jpg)

## Trying Some Commands
After logging into the course account, I called ```ls -lat``` and ```cd``` commands in the Powershell terminal. The outputs of commands are shown in the screenshot. 
![Commands](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Commands.jpg)

## Moving Files with scp
Create a WhereAmI.java file at local device with the following content:<br/>```class WhereAmI```<br/>
```    public static void main(String[] args) {```<br/>
```      System.out.println(System.getProperty("os.name"));```<br/>
```      System.out.println(System.getProperty("user.name"));```<br/>
```      System.out.println(System.getProperty("user.home"));```<br/>
```      System.out.println(System.getProperty("user.dir"));```<br/>
```    }```<br/>
```  }```<br/>
Make sure you are at the directory of WhereAmI.java before running the scp command. Use the scp command to send WhereAmI.java to remote computer. After sending the file, log into the remote computer and should be able to compile and run WhereAmI.java successfully. 
![SCP](https://github.com/zhh02/Week-2-Lab-Report/blob/main/SCP.jpg)

## Setting an SSH Key
First call the ssh-keygen command on local client which creates public key and private key files.
![Key_1](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Key_1.jpg)
And then log into the remote server and call ```mkdir .ssh```. After calling the command, log out and call scp to copy the public key file to the ssh directory.
![Key_2](https://github.com/zhh02/Week-2-Lab-Report/blob/main/Key_2.jpg)

## Optimizing Remote Running
In this section I want to demonstrate oprimizing remote running by copying a ```WhereamI1.java``` file from local server to remote server. A regular way of doing so is to call ```scp WhereamI1.java cs15lwi22aar@ieng6.ucsd.edu:~\``` command, which copies the file. And then I want to check if the file is moved to the correct directory, therefore I login to my remote account by calling ```ssh cs15lwi22aar@ieng6.ucsd.edu```. After loging in, I call the ```ls``` command and shows the list of files. In this case, I typed **127** keystrokes to finish the task as the following screenshot shows. I also compile and run the file to demonstrate the edit I made to the file (seems to be a error-causing one though). 
![Regular](https://github.com/zhh02/CSE15L-lab-reports/blob/main/Regular.jpg)
However, this task can be completed more easily by typing in the three commands together in one line: I call the command ```scp WhereamI2.java cs15lwi22aar@ieng6.ucsd.edu:~\; ssh cs15lwi22aar@ieng6.ucsd.edu "ls"``` to copy a file with same content, check, compile and run, which shows the same error message, by only running one time and typing **15** keystrokes using tab, up arrow and copy paste as the following screenshot shows. 
![Optimized](https://github.com/zhh02/CSE15L-lab-reports/blob/main/Optimized.jpg)
