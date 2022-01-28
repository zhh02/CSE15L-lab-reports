# Week 4 Lab Report 2
## Code Change #1
** Link to failure-inducing input ** : [test-file1](https://github.com/zhh02/CSE15L-lab-reports/blob/main/lab-report-2/test-file1.md)<br/>
In this case, the bug of ```MarkdownParse.java``` is that it fails to recognize the last close parenthesis and will be infinitely adding the ```closeParen``` to the ```toReturn``` value. In order to demonstrate the symptom, a print statement of current index ```System.out.println(currentIndex);``` is added. When the modified ```MarkdownParse.java``` file is called with test file, it prints the index of the last close parenthesis infinitely. 
