# Lab Report 2: Code Changes

# 1.

This is the screenshot of the code change diff from Github. Here we address the problem of possible infinite loop.

![Image][11]

[11]: 1.png

To be honest, here I cannot find the original version of code. So this is the revised version.
And the revised part is listed above.

[Link][1]

[1]:  https://github.com/AnonymousGym/markdown-parse-1/blob/main/MarkdownParse.java

Here is the screenshot of failure.

![Image][12]

[12]: 2.png

Here, if we miss the break part, we will fall into an infinite loop if there are more irrelevant stuff after the last eligible _[]()_ set. In test-file.md, the format is well-designed, but in new.md it is not. To solve this, we break the loop when there is no more available __nextOpenBracket__.
![Image][13]

[13]: 3.png
![Image][14]

[14]: 4.png

# 2.

This is the screenshot of the code change diff from Github. Here we solve the problem of throwing an exception when running an image.
![Image][15]

[15]: 5.png
This is the link to the test file.
[Link][2]

[2]: https://github.com/sha0xy/markdown-parse/blob/main/new.md

Here are the screenshots of comparison between failure and success.
![Image][16]

[16]: 6.png
![Image][17]

[17]: 7.png

As we can see, if we miss the break part, we will go into an infinite loop again as currentIndex remains 0 and cannot get out of the loop. So we add this break line to break the loop if there is no more __[]()__ in the file.

# 3.

This is the screenshot of the code change diff from Github. 
![Image][18]

[18]: 8.png

This is the link to the test file.
[Link][3]

[3]: https://github.com/littlefishy1/markdown-parse/blob/main/MarkdownParse.java
[Link][4]

[4]: https://github.com/littlefishy1/markdown-parse/blob/main/MarkdownParseTest.java

Here is the screenshot of failure.
![Image][19]

[19]: 9.png

Here in test 3 and 4 we have the IndexOutOfBoundsException. They have the same symptom. The main reason is in test-file3.md and test-file4.md.
In these files, there is no "()", so the program will crash when it cannot find the parentheses. We can also use break to exit when we cannot find parentheses to solve the problem.
