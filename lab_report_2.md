# Lab Report 2: Code Changes

# 1.

This is the screenshot of the code change diff from Github. Here we address the problem of possible infinite loop.

![Image][11]

[11]: 1.png

To be honest, here I cannot find the original version of code. So this is the revised version.
And the revised part is listed above.

[Link][1]

[1]:  https://github.com/AnonymousGym/markdown-parse/blob/main/MarkdownParse.java

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

[2]: https://github.com/sha0xy/markdown-parse/blob/main/MarkdownParse.java
