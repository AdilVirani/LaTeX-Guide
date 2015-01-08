# <a id"setup"></a>Preface - Installation


## MAC Installation
Before we begin, you'll probably need to install some things on your computer. So let's walk through the following steps: 

1. [Opening Terminal] (#term)
2. [Choosing a text editor] (#text)
3. [Installing \LaTeX] (#install)
4. [Creating a home for TeX files] (#folder)

#### <a id="term"></a>Opening Terminal
--------------------------------------

Click ⌘Space, which will open Spolight, then type in 'Terminal', and it will show up click on it to make it open. Keep it open for now we'll use it later. 

#### <a id="text"></a>Choosing a Text Editor
---------------------------------------------

As far as text editors go, your choices are essentially infinite. On OS X, you can simply use the native text editor Apple supplies. But, the most obvious choice would be to use [Sublime Text] (http://www.sublimetext.com), but there are many more available, such as [Vim] (http://www.vim.org/).

#### <a id="install"></a>Installing LaTeX
-------------------------------------------

LaTeX is a pretty easy install. TUG (TeX Users Group) created a download for Mac called ['MacTeX'] (http://mirror.ctan.org/systems/mac/mactex/MacTeX.pkg). Once the download finishes, double click the installer, and follow the instructions. The installer will tell you when you're set.

#### <a id="folder"></a>Creating a home for TeX files
-------------------------------------------------------

Now this can get a little tricky. LaTeX installs inside the root folder of your hard drive. If you're running Mac OS 10.6 or later, you won't be able to see the install location. You can fix this by going back to the Terminal, and typing the following command:

    sudo chflags nohidden /usr
    killall Finder

Hit enter - you'll have to type in your administrator password (which is your computer password), because 'sudo' means "run this command as an administrator." Once you do this, you can navigate to your your `/usr` folder - but we don't need that for now, so we'll get to it when we need it.

##### Changing Your Path

Okay, this next part is a little bit tricky. To briefly explain, you need to tell Terminal to look in the right places for the commands you're going to use. So, to do that, it takes a few steps.

**Step 1 - Cut a Hole in the Box**

Open the Terminal and paste this in:

    sudo defaults write com.apple.Finder AppleShowAllFiles TRUE
    killall Finder

Hit enter  - type your password again. *A lot* of files probably showed up in the Finder - that's fine, because you'll hide them in a minute.

**Step 2 - Put Your Stuff in that Box**

Open your text editor of choice. Make sure it's in **plain text** format, and copy/paste this in:

    export PATH=/usr/local/texlive/2012/bin/universal-darwin:$PATH

Then, save it in your home folder as '.profile' - **[NB]** *make sure* your save it with the period at the beginning and no extension on the end (you may have to uncheck the box if you're using Text Edit).

**Step 3 - Make It Open That Box**

Once it's saved, quit Terminal and restart it.

 Just for fun type in `xetex` and hit enter. It should say:
 
 `This is XeTeX, Version 3.1415926-2.4-0.9998 (TeX Live 2012)
 restricted \write18 enabled.`
 
 If it does, you're all set. Just press 'x' and hit enter to quit out of XeTeX. You're almost ready to start typesetting!
 
 
 When LaTeX typesets your documents, it creates a number of temporary files (such as yourdocument.aux, yourdocument.bcf, etc.). You don't really need these, and you probably don't want these sitting on your desktop, so it's best to create a folder specifically for them. I call mine 'Manuscripts'.

Note that once you've created a folder, you'll want to change the Terminal's "working directory," which is the folder the Terminal looks in for files to do things with. To do this open the Terminal and then type `cd` and then the path to the file. So if my home folder was called USER, and my LaTeX folder was inside my documents folder and called "LaTeX", I'd type:

    cd "~/Documents/LaTeX/"

On a Mac, "~" just means "home directory," which is shorter than typing USER every time. Now you're all set up and ready to get started.
