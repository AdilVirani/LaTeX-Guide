#Getting Started - Syntax

To write in LaTeX code, you have to provide LaTeX with two things: code to describe what you want to do, and a "guidebook" to tell LaTeX how to intepret what you want to do. 

The "guidebooks" are called packages. TeXLive 2012 comes with all of the packages you'll need for this guide. Now let me teach you how to make your own résumé. Feel free to customize it however you like.

**Open Tex Works**

**In LaTeX, you have to set up each of the margins manually, which can seem tedious at first.** However if you have too much information or too little, these settings can be easily adjusted to make your document look its best. This can be done with the following code: 

```TeX
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
```

**The next step is to actually begin your document.** In LaTeX this is done by simply inserting the following code after what you just inserted:

```TeX
\begin{document}
\end{document}
%These 2 lines of code tell LaTeX that everything that goes in between these tags is what you want displayed as your actual document
```

**In LaTeX you write your document in the same manner that you would in Word, except you have to use commands.** These commands are written in between the `\begin{document}` and `\end{document}`. Now let's make a header! Let's start by inserting the following code (Note: Be sure to read the comments they are very useful to know what each line does):

```TeX
\centerline{ {\LARGE \bf Sample Student}} %Put the text in the center and make it large and bold

%With special characters like bullets they must be in between dollar signs
\centerline{1234 Special St. $\bullet$ Dallas, TX 10102 $\bullet$ (123) 456-7890 or (555) 555-5555}
\centerline{sample.student@unt.edu}
\noindent %LaTeX will treat all new text as a paragraph and indent by default
\line(1,0){470}\\ %Insert a line with direction(1,) with length 470
```

Now your header should look a little something like this.

![alt text][header]
[header]: https://github.com/AdilVirani/LaTeX-Guide/blob/master/Basic_Header.png

**The next part of your resume should be some simple objective and summary type sections.** This can easily be accomplished by making headers and following them with text. Here's some more code that will do that for you:

```TeX
\noindent {\Large \bf Objective}%dont indent this line and make it bold and only kind of large
\smallskip

\noindent%This is to make the following text not indented
To obtain a job or internship in software developement where I could use my experience to create software necessary for the company to develop and prosper


\bigskip%This makes a large line skip (\smallskip s also a command but has a smaller gap)
\noindent{\Large \bf Executive Summary}
\smallskip

\noindent
Three years of experience in Software Development for a plethora of technologies. Great group work ethic, presentation skills, and work proficiency. Follow directions well and try my best to write clean code.
\bigskip
```

Here's a snippet of what your code should look like:

![alt text][snippit]
[snippit]: https://github.com/AdilVirani/LaTeX-Guide/blob/master/Code_Snippit.png

This code should result in the following output:

![alt text][body]
[body]: https://github.com/AdilVirani/LaTeX-Guide/blob/master/Basic_Body.png

***Extra Helpful Commands*** While this may look a little bit silly on the sample resume we created, it serves the purpose of demonstrating how you can make columns in LaTeX. In order to do a list of known programming languages I used the following command: 

```TeX
\hfill %This command will create even spacing between whatever you put it in between (text and margin, text and text, etc.)
```

**Here is a sample of `\hfill` using the following code: 

```TeX
\noindent{\Large \bf Technical Skill}  %Make sure that there is no line skip for as long as you want this effect
Can Program in a large variety of languages including: \\ %The \\ is the same as a return
\centerline{\hfill $\bullet$ Java \hfill $\bullet$ JavaScript \hfill $\bullet$ HTML/CSS, \hfill $\bullet$ PHP, \hfill $\bullet$ Python, \hfill $\bullet$ Ruby \hfill}\\
\centerline{\hfill $\bullet$ Bash \hfill $\bullet$ IDL \hfill}\\
Proficeint with the following Technologies: \\
\centerline{\hfill $\bullet$ Node.js \hfill $\bullet$ \LaTeX \hfill $\bullet$ Git \hfill}\\

\noindent{\Large \bf Professional Experience}
\smallskip

\centerline{ {\large \bf Lead Developer for broadlinkone \hfill 2011-Present} }
$\bullet$ Fixed front-end and back-end for the company's website, along with other branches of broadlinkone's website.

$\bullet$ Created Cloudworx website along with other cloud assisting websites.

$\bullet$ Skills used: HTML, CSS, PHP, Wordpress
\bigskip
```
***Repeat these last 4 lines for each section you want to add*** Here's a look at the semi-finished résumé:

![alt text][fin]
[fin]: https://github.com/AdilVirani/LaTeX-Guide/blob/master/pictures/Semi-Finished_Resume.png
