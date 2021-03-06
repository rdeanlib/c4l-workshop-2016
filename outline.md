# Installation Instructions
This workshop is designed to help you set up your laptop so that you can more easily participate in code workshops. 

*Table of Contents*

1. [Text Editors](#text-editors-install-sublime-text)
2. [The Command Line](#the-command-line)
  * [Mac Command Line](#mac-command-line)
  * [Windows Command Line](#windows-command-line)
3. [Installing a Programming Language](#installing-a-programming-language-python-351)
4. [Environment Variables](#environment-variables)
  * [Mac PATH: Python 3.5](#mac-updating-your-path-to-include-python-35)
  * [Mac PATH bonus: Java Development Kit (JDK)](#mac-bonus-adding-jdk-to-path)
  * [Windows PATH: Python 3.5](#windows-confirm-that-your-path-includes-python-35)
  * [Windows PATH bonus: Sublime Text 3](#windows-bonus-add-sublime-text-3-to-path)
5. [Virtual Environments](#running-a-virtual-environment-in-virtualbox)
  * [VirtualBox for Mac](#virtualbox-for-mac)
  * [VirtualBox for Windows](#virtualbox-for-windows)


##Text Editors: Install Sublime Text

#### Everybody:
1. Open a web browser and go to [https://www.sublimetext.com](https://www.sublimetext.com)
2. Scroll down to the button that says "Download for (your operating system)". Make sure you're installing version 3 of Sublime Text. If you don't see a button, click the "Download" link at the top of the page.

#### Mac OS
1. Click to download the Sublime Text .dmg file
2. Double-click on the .dmg file to start installation
3. When the Sublime Text window opens, drag the Sublime Text logo into the Applications folder
4. After closing the window and ejecting the disk image from your desktop, go to your Applications folder and open Sublime Text 3

#### Windows 7
1. Click "Save file" to download the Sublime Text .exe file.
2. Double-click on the .exe file to run it and begin the installation process.
3. When you get to the screen "Select Destination Location" make a note of where Sublime Text 3 is being installed (e.g., ```C:\Program Files\Sublime Text 3```)
4. Complete installation using the install wizard.
5. To open, go to Start > All Programs > Sublime Text 3.

### Everybody: Open a Markdown (.md) file in your text editor
#### Mac:
1. In the `c41-workshop-2016` workshop files directory, right click (or two-finger click; you want the "open with" menu) on "outline.md" and select "Open with Sublime Text."

#### Windows:
1. In the ```c4l-workshop-2016``` workshop files directory, right click on "outline.md" and select "Open with Sublime Text."

## The Command Line

Note: these instructions will say to "enter" commands. This means to type the command and then press the Enter button.

Command Line "Cheatsheets"
* Mac: [http://cli.learncodethehardway.org/bash_cheat_sheet.pdf](http://cli.learncodethehardway.org/bash_cheat_sheet.pdf)
* Windows: [http://www1.cs.columbia.edu/~sedwards/classes/2015/1102-fall/Command%20Prompt%20Cheatsheet.pdf](http://www1.cs.columbia.edu/~sedwards/classes/2015/1102-fall/Command%20Prompt%20Cheatsheet.pdf)

### Mac Command Line

1. Open the command line interface (CLI)
  * Use Launchpad, or open a Finder window and choose "Applications," then locate the program called "Terminal" (you should find it under "Utilities")

2. The command prompt
  * Each time you see the command prompt, it lets you know that you can give your computer instructions. Text without a command prompt is "output" (the responses from your computer).
  * In MacOS, the command prompt will look like: `megans-computer:~ username$` 

3. Find where you are (your current path) in the file system (the hierarchy of all the files on your computer)
  * Enter ```pwd``` (for "print working directory").
  * This will print your current directory.
  * Enter ```ls```. This will list everything that's in your currrent directory (files and other directories).
  
4. Navigate to the workshop folder (if you saved it on your Desktop)
  * Type `cd Desktop` to change the current directory to the Desktop. Your file path and command prompt will update to `megans-computer:Desktop username$`
  * View a list of directories on your desktop by entering `ls` again.
  * Continue to the workshop sample files directory by entering `cd gr4ww`
  
  Navigation Tips:
  * If you don't want to type the whole name of a directory, type a few characters and press the `Tab` button to autocomplete a unique file name.
  * To move up several directories, type `cd Desktop/your_folder_name`
  * If your directory or file name has spaces in it, you will get an error if you include the space as-is. 
    * You can "escape" the space (tell the computer to ignore it) by adding a backslash in front of the space: `cd Desktop/Your\ Folder/`. 
	* Alternatively, you can enclose the folder name in double quotes: `cd Desktop/"Your Folder"/`
  * To re-use a command you just typed, hit the up arrow to cycle back through previously typed commands. 
  * To auto-complete a directory or filename, hit `Tab` after you've typed part of the name.
  * To go back to the "top" or left-most directory in the path, type `cd` with nothing after it
  * To go back "up" one directory, type `cd ..`
  
5. Create a new directory
  * In the gr4ww directory, enter `mkdir letters`.
  * Check for your directory by entering `ls`.

6. Move files to your new directory
  * Change to the excerpts directory by typing `cd excerpts`
  * Move the first letter file into the letters directory by entering `mv letter01.txt ../letters/`
    * The backslash at the end of "letters" tells the computer that you are moving the file into a sub-directory.
    * The two periods direct the computer to move up one directory before looking for the directory you specify.
    * You can also copy a file instead of moving it. Enter `cp letter02.txt ../letters/`

7. Rename a file
  * There's an underscore in the "letter_03.txt" file name, which isn't consistent with the other files. Let's rename it!
  * In the excerpts directory, enter `cp letter_03.txt letter03.txt` to copy the file contents into a new file, then enter `rm letter_03.txt` to remove the old version (there's not an exact "file rename" command)

8. Read a file in the command line
  * In the excerpts directory, enter `cat letter06.txt`
  * The text of the letter will display as output on the command line and your prompt will return.

9. Open a file in a text editor from the command line
  * Type `nano letter06.txt`
  * Use the arrow keys to navigate the file; make changes
  * To save and exit, type `ctrl + x` and then hit `enter`

### Windows Command Line

1. Open the command line interface (CLI)
  * Click the Start Button. 
  * In the search box, enter `cmd`

2. The command prompt
  * Each time you see the command prompt, it lets you know that you can give your computer instructions. Text without a command prompt is "output" (the responses from your computer).
  * In Windows, the initial command prompt will look like "C:\Users\Elizabeth>" (where "Elizabeth" is your Windows user name). When you open the command line interface, you will start in your "home directory." 

3. Find where you are (your current path) in the file system (the hierarchy of all the files on your computer)
  * Enter `echo %cd%`.
  * This will print the path of your current directory.
  * Enter `dir`. This will list everything that's in your currrent directory (files and other directories).

4. Navigate through folders (directories)
  * Enter `cd Desktop` to change the current directory to the Desktop. Your file path and command prompt will update to "C:\Users\Username\Desktop."
  * View a list of directories on your desktop by entering `dir` again.
  * Continue to the workshop sample files directory by entering `cd gr4ww`
  * If you don't want to type the whole name of a directory, type a few characters and press the `Tab` button to autocomplete a unique file name.

5. Create a new directory
  * In the gr4ww directory, enter `mkdir letters`.
  * Check for your directory by typing `dir`.

6. Move files to your new directory
  * Change to the excerpts directory by entering `cd excerpts`
  * Move the first letter file into the letters directory by entering `move letter01.txt ..\letters\`
    * The backslash at the end of "letters" tells the computer that you are moving the file into a sub-directory.
    * The two periods direct the computer to move up one directory before looking for the directory you specify.
    * You can also copy a file instead of moving it. Enter `copy letter02.txt ..\letters\`

7. Rename a file
  * There's an underscore in the "letter_03.txt" file name, which isn't consistent with the other files. Let's rename it!
  * In the excerpts directory, enter `copy letter_03.txt letter03.txt` to copy the file contents into a new file, then enter `del letter_03.txt` to remove the old version.
  * In Windows, you can also type `ren letter_03.txt letter03.txt` to rename the file without making a copy first.

8. Read a file in the command line
  * In the excerpts directory, enter `type letter06.txt`
  * The text of the letter will display as output on the command line and your prompt will return.

9. Open a file in a text editor from the command line
  * To open a text file in your default text editor, enter only the file name: `letter06.txt`

## Installing a Programming Language: Python 3.5.1
### Everbody:
1. Open a web browser and go to [https://www.python.org/downloads/](https://www.python.org/downloads/)
2. Click "Download Python 3.5.1"
3. Save the .pkg (mac) or .exe (windows) file to someplace you'll be able to find it (i.e. Downloads, Desktop)

### Mac:
4. Verify that you've installed python: open the command line and type `python --version`
5. If your results are anything other than Python 3.5.1, type `python3 --version`

### Windows:
4. Double-click on the .exe file and click Run if prompted.
5. On the "Install Python 3.5.1" screen, uncheck "Install launcher for all users (recommended)."
6. Click "Customize Installation - Choose location and features."
7. Leave all the "optional features" checked.
8. Under "Advanced Options" select the following:
  * Associate files with Python (requires the py launcher)
  * Create shortcuts for installed applications
  * Add Python to environment variables
9. Under "Customize install location" click "Browse."
  * Under your user directory, create a new folder for Python 3.5.1. For example: C:\Users\Elizabeth\Python3. Select this folder for installation.
10. Click "Install."
11. Once the installation has finished, open the Windows command line.
12. Enter `python --version`. If your results are anything other than Python 3.5.1 go to the next step.
13. On the command line, navigate to the directory where you installed Python3. 
  * `cd Python3`
14. Type `python --version` in this directory. 

## Environment Variables

### Mac: Updating your PATH to include Python 3.5

1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Type `cat ~/.bash_profile` to see if you already have a .bash_profile set up. 
  * If you do, you should see what's in it
  * If you don't, that's ok! Type `touch ~/.bash_profile` to create one, then type `sudo nano ~/.bash_profile` to edit it (you'll need to enter your computer password when prompted)
3. You may see something like: "export JAVA_HOME=$(/usr/libexec/java_home)" -- if so:
	* Copy what you find
	* Exit (type "ctrl-x" and then hit enter)
	* Type `touch .bash_profile.pysave` and then paste the copied message from your original bash profile 
	* Exit the pysave bash profile (type "ctrl-x" and then hit enter)
4. Go back to .bash_profile (`sudo nano ~/.bash_profile`) and add the following text:
```
# Setting PATH for Python 3.5
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.5/bin:${PATH}"
export PATH
```
5. Exit using "ctrl-x"
6. That's it!

### Mac bonus: Adding JDK to PATH 
1. Open a Terminal window (if you want to open a new one, you can click on it in your dock and hold until a menu pops up, then choose "New Window")
2. Type ```echo $JAVA_HOME``` to find out where the "home" directory of your JDK version is. It will probably look something like:

```
/Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home
```
3. Copy and paste that line of text into a text editor, or write it down
4. Type ```cat ~/.bash_profile``` to see if you already have a .bash_profile set up. 
	* If you do, you should see what's in it
	* If you don't, that's ok! Type ```touch ~/.bash_profile``` to create one, then type ```sudo nano ~/.bash_profile``` to edit it (you'll need to enter your computer password when prompted)
5. To add that location to your PATH, type this into your bash profile:

```
export JAVA_HOME="$(/usr/libexec/java_home -v 1.8)"
```
NOTE: the number after the -v should match the number after jdk that you copied and pasted from the previous command

### Windows: Confirm that your PATH includes Python 3.5

1. Go to Start > Control Panel > System and select "Advanced System Properties".
  * You can also search for "Environment Variables".
2. Click `Environment Variables`.
3. There are two levels of environment variables: ones that affect only your user, and system variables. Both have a "Path" entry.
4. Under "User variables for Elizabeth" select `Path` and click `Edit...`.
5. Paths to different locations of installed programs appear in the "Variable value" field. Use CTRL + C to copy the text of this field and paste it in a text editor.
6. Check in the text editor that you have the following entries:
  * C:\Users\Elizabeth\Python3\Scripts\;
  * C:\Users\Elizabeth\Python3\;
7. If you added entries, click `OK`. Otherwise click `Cancel.`

### Windows bonus: Add Sublime Text 3 to PATH

1. Go to Start > Control Panel > System and select "Advanced System Properties".
  * You can also search for "Environment Variables".
2. Click `Environment Variables`.
3. There are two levels of environment variables: ones that affect only your user, and system variables. Both have a "Path" entry.
4. Under "User variables for Elizabeth" select `Path` and click `Edit...`.
5. Go to the end of the text in the "Variable value" field and add a semicolon if one isn't present.
6. After the semicolon, enter the path to Sublime Text 3: `C:\Program Files\Sublime Text 3`.
7. Click `OK` until all the Windows dialogue boxes are closed.
8. Open the Windows command line and enter `subl` to run the text editor.

## Running a Virtual Environment in VirtualBox

### VirtualBox for Mac
1. Download VirtualBox -- see the following link: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
2. Choose the option for "VirtualBox 5.0.14 for OS X hosts" and click the link that says "amd64" to download
3. Save the .dmg file somewhere you'll be able to find it again (Desktop, Downloads, etc.)
4. Double-click the file when it's finished downloading to start the install process
5. In the pop-up window, follow the instructions and double-click on the .pkg icon
6. Follow the install wizard steps and input your password when it asks for one
7. Close the installer window and eject the "VirtualBox" drive image you see on your desktop (you want to run the version you installed in your "Applications" folder just now)

### VirtualBox for Windows

1. Download VirtualBox -- see the following link: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)
2. Choose the option for "VirtualBox 5.0.x for Windows hosts" and click the link that says "x86/amd64" to download
3. Save the .exe file somewhere you'll be able to find it again (Desktop, Downloads, etc.)
4. Double-click the file when it's finished downloading to start the install process. Click "Run" to allow it to install.
5. Click `Next` on the main install setup screen.
6. On the custom page, don't change anything. Click `Next`.
7. Leave all the options checked (create a shortcut on the desktop; create a shortcut in the quick launch bar; register file associations.) Click `Next`.
8. The installer will warn you that installing will reset your network connection. Finish anything that shouldn't be interrupted and click `Yes`.
9. Click `Install` to begin the installation and allow the program to make changes to your computer.
10. When prompted "Would you like to install this device software?" click "Install." You will have to do this a few times to install the separate virtual networking and device components.
11. When prompted, click "Finish" and start Oracle VM VirtualBox.


## Wrap-Up:
* You can do it! Go forth and code workshop!
