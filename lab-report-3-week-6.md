# Week 6 Lab Report 3
## Streamline ```ssh``` Configuration
### Step 1: Set up config file
Find the config file under ```C:\Users\[Custom Username]\.ssh```. If there isn't one, create one. I don't have one so I create a new ```config``` file with no extension. 
![create-config](config_file.jpg)<br/>
Then open ```config``` file in VSCode, add following content to it: <br/>
```Host ieng6```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;```HostName ieng6.ucsd.edu```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;```User cs15lwi22zzz (use your username)```<br/>
Remember to replace User with your username.<br/>
![edit_config](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/config_edit.jpg)<br/>
### Step 2: Try a faster and easier login command
Open a terminal and use the command ```ssh ieng6``` to login. <br/>
![new-login](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/login.jpg)<br/>
With the new command, we can login to the ieng6 account without typing or copying and pasting the full account name. <br/>
### Step 3: Copy a file to ieng6 account with the configuration
First create a new file on local device. I created a ```ImATestFile.java``` file with following content:<br/>
```public class ImATestFile{```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;```public static void main (String[] args){```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```System.out.println(":)");```<br/>
&nbsp;&nbsp;&nbsp;&nbsp;```}```<br/>
```}```
![test-file](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/test_file.jpg)
Then I copy it to the remote device and login to ieng6 account using command ```scp ImATestFile.java ieng6; ssh ieng6```.<br/>
![scp](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/scp_config.jpg)<br/>
```ImATestFile.java``` has been successfully copied to remote account using scp and ssh configuration. 
