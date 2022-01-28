# Week 4 Lab Report 2
## Code Change #1
**Screenshot of code change**: ![Code-change-1](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/Infinite_loop_diff.jpg)
**Link to failure-inducing input** : [test-file1](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/test-file1.md)<br/>
**Symptom**: ![Command](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/Infinite_loop_cmd.jpg)<br/>
![Output](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/Infinite_loop_output.jpg)<br/>
In this case, the bug of ```MarkdownParse.java``` is that it fails to recognize the last close parenthesis and will be infinitely adding the ```closeParen``` to the ```toReturn``` value. In order to demonstrate the symptom, a print statement of current index ```System.out.println(currentIndex);``` is added into the while loop to show how the current index is changed. When the modified ```MarkdownParse.java``` file is called with test file, it prints the index of the last close parenthesis infinitely. The reason of this input causing the failure it that it has an empty line after the last link, which probably causes the while loop to fail to end the while loop and therefore go over the process of finding the next ```")"``` infinitely without a break. 
