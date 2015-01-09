#Getting Started - Syntax

To write in LaTeX code, you have to provide LaTeX with two things: code to describe what you want to do, and a "guidebook" to tell LaTeX how to intepret what you want to do. 

The "guidebooks" are called packages. TeXLive 2012 comes with all of the packages you'll need for this guide.

**Open Tex Works**

**In LaTeX, you have to set up each of the margins manually, which can seem tedious at first.** However if you have too much information or too little, these settings can be easily adjusted to make your document look its best. This can be done with the following code: 

    \documentclass[11pt]{article} %Sets the default text size to 11pt and class to article.
    %--------------------------------------Dimension---------------------------------------
    \topmargin=0.0in %length of margin at the top of the page (1 inch is added by default)
    \oddsidemargin=0.0in %lengthh of margin on sides for even odd pages
    \evensidemargin=0in %length of margin on sides for even pages
    \textwidth=6.5in %How wide you want your text
    \marginparwidth=0.5in
    \headheight=0pt %1in margins at top and bottom (1 inch is added by default)
    \headsep=0pt %Increase to increase white space in between headers and the top of the page
    \textheight=9.0in %How tall the text body is allowed to be on each page

**The next step is to actually begin your document.** In LaTeX this is done by simply inserting the following code:

    \begin{document}
    \end{document}
    %These 2 lines of code tell LaTeX that everything that goes in between these tags is what you want displayed as     your actual document
