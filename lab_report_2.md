# Lab Report 2: Code Changes

__1.__

This is the screenshot of the code change diff from Github.

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

