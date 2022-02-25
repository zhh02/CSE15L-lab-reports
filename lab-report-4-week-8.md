# Week 8 Lab Report 4 <br/>
## Repository links
### [My Markdown-parse repository](https://github.com/zhh02/markdown-parse.git)<br/>
### [Markdown-parse repository reviewed](https://github.com/jdweak/markdown-parse.git)<br/><br/>
## Snippet 1
> ### What it should produce according to the CommonMark demo site: <br/>
![Snippet1_preview](lab-report-4/Snippet1_demo.png)<br/>
Therefore the link to be returned from this snippet should be ```[`google.com, google.com, ucsd.edu]```
> ### Make it a test in MarkdownParseTest.java
![Snippet1_test](lab-report-4/Snippet1_test.png)<br/>
> ### Run JUnit test with my MarkdownParse
![Snippet1_myMDP](lab-report-4/Snippet1_myMDP.png)<br/>
The JUnit test fails because my implementation fails to exclude ```url.com```. <br/>
> ### Run JUnit test with the reviewed MarkdownParse
![Snippet1_reviewedMDP](lab-report-4/Snippet1_reviewedMDP.png)<br/>
The JUnit test fails because it fails to exclude ```url.com``` and to return ```ucsd.edu```.<br/>
> ### Answering Questions
+ I am not particularly sure about my implementation since our group is using a very different approach from professor's original approach. However, the test result seems like backticks are allowed and can be returned successfully by our implementation while the error is that it fails to determine the location of the backticks, therefore returning ```url.com``` as well. In order to fix this, a small code change might not be enough since we need to determint the index of brackets and differentiate the backticks in front of the open brackets to not return ```url.com```<br/><br/>

## Snippet 2
> ### What it should produce according to the CommonMark demo site: <br/>
![Snippet2_preview](lab-report-4/Snippet2_demo.png)<br/>
Therefore the link to be returned from this snippet should be ```[a.com, a.com(()), example.com]```
> ### Make it a test in MarkdownParseTest.java
![Snippet2_test](lab-report-4/Snippet2_test.png)<br/>
> ### Run JUnit test with my MarkdownParse
![Snippet2_myMDP](lab-report-4/Snippet2_myMDP.png)<br/>
The JUnit test fails because my implementation fails to include any of the links.
> ### Run JUnit test with the reviewed MarkdownParse
![Snippet2_reviewedMDP](lab-report-4/Snippet2_reviewedMDP.png)<br/>
The JUnit test fails because it fails to exclude ```url.com``` and to return ```ucsd.edu```.<br/>
