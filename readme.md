# Terminals in Sublime Text
This repo contains some JSON code to help you add terminals to Sublime Text 3.

## Requirements
Windows operating system.  
Sublime Text 3 available here: https://www.sublimetext.com/3

## Getting Started

### Step 1: Install Terminus
Terminus is a great package for Sublime made randy3k. More information here: https://github.com/randy3k/Terminus  
  
First you need to install terminus.  
Press Ctrl + Shift + P in Sublime Text to open the Command Palette. Type in 'Terminus' and select it. If you haven't installed Package Control already, you'll be prompted to do that now.  

Once you have installed Terminus go back to the Command Palette (Ctrl + Shift + P) and type in 'Terminus: Open Default Shell in View'. This should open a Command Prompt in a new window.  
If you try the command 'Terminus: Open Default Shell in Panel' it will open Command Prompt at the bottom of your screen.  
  
This is great but we want some other kinds of shells with keyboard shortcuts to them.

### Step 2: Other Shells
In the Command Palette (Ctrl + Shift + P) type in 'Terminus Command Palette'. This should open up a split screen view. In this repository you'll find a 'Terminus Command Palette.json' file. Copy and paste the contents into the right hand side of the split screen view and save it.  
Read the comments in the code to see what it does. Make sure the code is using the correct path to your installation of Git Bash (or other shell). This occurs on lines 49 and 61. The default is:  
'''
"cmd": ["C:\\Program Files\\Git\\bin\\bash.exe", "-i", "-l"],
'''
Note that double slashes are required (in order to escape single slashes).  
  
The code should add new Commands to the Command Palette. Open the Command Palette (Ctrl + Shift + P) and make sure the commands work.  
i.e. The command 'Git Bash (panel)' should open Git Bash in the panel at the bottom of your screen.  
  
You can add your own shells by copy and pasting your code. If your shells are based on Command Prompt then the lines containing the paths only need to be:  
'''
"cmd": "PATH_TO_YOUR_SHELL",
'''
But, if your shells are not Command Prompt based (open externally from Command Prompt) then you need to use the following line:  
'''
"cmd": ["PATH_TO_YOUR_SHELL", "-i", "-l"],
'''

### Step 2: Keyboard Shorcuts
Open the Command Palette (Ctrl + Shift + P) and type 'Terminus Key Bindings'. Then copy the contents of the 'Terminus Key Bindings.json' file into the right hand side of the view and save it. This should add keyboard shortcuts to your shells. Again if you are using Git Bash, the path to it may need correcting.  
  
The following shorcuts should work:
* Ctrl + ' - Toggles the Panel at the bottom of the screen open and closed
* Ctrl + 1 - Opens Command Prompt in the Panel
* Ctrl + 2 - Opens Git Bash in the Panel
* Ctrl + c - Opens Command Prompt in the Panel
* Ctrl + b - Opens Git Bash in the Panel  
  
The code is well commented so it should be clear how it works. Again you can copy and paste the code to add your own shortcuts.  
  
## Acknowledgements
Thanks again to randy3k for developing Terminus. More information here: https://github.com/randy3k/Terminus 