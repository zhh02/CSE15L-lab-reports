# Week 4 Lab Report 2
## Code Change #1
**Screenshot of code change**: ![Code-change-1](lab-report-2/Infinite_loop_diff.jpg)
**Link to failure-inducing input** : [test-file1](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/test-file1.md)<br/><br/>
**Symptom**: ![Command](lab-report-2/Infinite_loop_cmd.jpg)<br/>
![Output](lab-report-2/Infinite_loop_output.jpg)<br/>
In this case, the bug of ```MarkdownParse.java``` is that it fails to recognize the last close parenthesis and will be infinitely adding the ```closeParen``` to the ```toReturn``` value. In order to demonstrate the symptom, a print statement of current index ```System.out.println(currentIndex);``` is added into the while loop to show how the current index is changed. When the modified ```MarkdownParse.java``` file is called with test file, it prints the index of the last close parenthesis infinitely. The reason of this input causing the failure it that it has an empty line after the last link, which probably causes the while loop to fail to end the while loop and therefore go over the process of finding the next ```")"``` infinitely without a break. <br/><br/>
## Code Change #2
**Screenshot of code change**: ![Code-change-2](lab-report-2/Carrots_diff.jpg)
**Link to failure-inducing input** : [test-file2](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/test-file2.md)<br/><br/>
**Symptom**: ![Output](lab-report-2/Carrots_output.jpg)<br/>
In this case, the bug of ```MarkdownParse.java``` is that it can only add the link within brackets but not carrots. The symptom of this bug is that the link cannot be returned when running a test file with link within carrots. This bug causes such symptom because carrots are not recognized and therefore the links within carrots in ```test-file2.md``` cannot be added to the ```toReturn``` string list. <br/><br/>
## Code Change #3
**Screenshot of code change**: ![Code-change-3](lab-report-2/incomplete_diff.jpg)<br/>
**Link to failure-inducing input** : [test-file3](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/test-file3.md)<br/><br/>
**Symptom**: ![Output](lab-report-2/incomplete_output.jpg)<br/>
In this case, the bug of ```MarkdownParse.java``` is that when one parenthesis is missing, the value of ```openParen```/```closeParen```/```nextOpenBracket```/```nextCloseBracket```/```nextOpenCarrot```/```nextCloseCarrot```can be -1. The corresponding symptom is that an exception will be thrown when trying to run ```MarkdownParse.java``` with ```test-file3.md``` which contains a link with close parenthesis missing. 
