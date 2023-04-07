# Data-Bias-of-Toxic-Internet-Comments
The goal of this project (which is an assignment for my I 310D: Introduction to Human-Centered Data Science class) was to explore the concept of bias through querying an existing natural language processing model — specifically, the Perspective API released by Google Jigsaw. For this assignment, I examined a dataset of internet comments and their scores and scored the toxicity of each comment based on my own hypothesis (if a comment contains "toxic" keywords (or a high frequency of these keywords), then it is more likely to be flagged as toxic), then through the Perspective API, then comparing the two.

## Conclusions

There is an obvious threshold line between if a comment is considered toxic or not (0.3561489) that was established using FPR, TPR, and threshold report. Anything above 0.3561489 is considered toxic while anything below is considered not toxic.

There is a very soft correlation between a comment's toxicity score and the number of toxic keywords contained in it. As the toxicity score increases, the higher number of toxic keywords there are present in the comment. An argument could be made that for low toxicity scores, it is shown that there are lower number of toxic keywords present. However, one possible counter is that the tests run encompassed mostly comments with a low number of toxic keywords present; therefore, it is obvious that most of the data points would be grouped in the bottom left corner of the graph.

I was surprised by the lack of correlation between a comment's toxicity score and the number of toxic keywords contained in it, as I believed my hypothesis to be correct, which could be traced back to bias based on my own assumptions of how flagging toxic comments worked.

There were a total of 50 toxic comments and 50 non-toxic comments used to train the model, and 200 toxic and non-toxic comments used to test the model. Some values were reported as "NaN", which resulted in the final dataframe of comments and their attributes to total at 198 entries. The low number of comments used to train and test the model may have had an affect on the threshold value used as well as the visualizations of the trends (as I did not incorporate the entire file of comment data as I thought it was too large).

### MIT License

Copyright (c) 2023 rosalynlu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

### Creative Commons Attribution-ShareAlike License

Copyright (c) 2023 rosalynlu

Attribution

To re-distribute a text page in any form, provide credit to the authors either by including a) a hyperlink (where possible) or URL to the page or pages you are re-using, b) a hyperlink (where possible) or URL to an alternative, stable online copy which is freely accessible, which conforms with the license, and which provides credit to the authors in a manner equivalent to the credit given on this website, or c) a list of all authors. (Any list of authors may be filtered to exclude very small or irrelevant contributions.) This applies to text developed by the Wikipedia community. Text from external sources may attach additional attribution requirements to the work, which should be indicated on an article's face or on its talk page. For example, a page may have a banner or other notation indicating that some or all of its content was originally published somewhere else. Where such notations are visible in the page itself, they should generally be preserved by re-users.

Copyleft/Share Alike

If you make modifications or additions to the page you re-use, you must license them under the Creative Commons Attribution-Share-Alike License 3.0 or later.

Indicate changes
