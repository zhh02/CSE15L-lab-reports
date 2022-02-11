# Week 6 Lab Report 3
## Streamline ```ssh``` Configuration
### Step 1: Set up config file
Find the config file under ```C:\Users\[Custom Username]\.ssh```. If there isn't one, create one. I don't have one so I create a new ```config``` file with no extension. 
![create-config](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/config_file.jpg)<br/>
Then open ```config``` file in VSCode, add following content to it: <br/>
```Host ieng6```<br/>
&nbsp;&nbsp;&nbsp;&nbsp```HostName ieng6.ucsd.edu```<br/>
&nbsp;&nbsp;&nbsp;&nbsp```User cs15lwi22zzz (use your username)```<br/>
Remember to replace User with your username.<br/>
![edit_config](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/config_edit.jpg)<br/>
### Step 2: Try a faster and easier login command
Open a terminal and use the command ```ssh ieng6``` to login. <br/>
![new-login](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-3/login.jpg)<br/>
