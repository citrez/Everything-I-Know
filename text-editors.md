# Text Editors / IDEs


## VScode
I spend most of my time in vscode. I like its versatility, it does everything (includeing notebooks) well.
I use it for everything from production python code to markdown editing. It is so feature rich, I learn new things about it all the time. It has very good code completion, this comes particularly handy when altering settings, ctr+space gives you all the available options. All settings are also certrally sycned to your account via github. Editing markdown documents is also a pleasure in vscode.


## Notes
If having problems in vscode connecting your venv to the jupyter kernel. Add the path to the venv in setting.json "python.defaultInterpreterPath" setting. Then select it as an interpreter, then it will show up.

Show command pallete. Jupyter: create interactive window, when working within notebooks

VScode has been an absoloute reveleation to me. Not only does it make you feel like a 'real programmer' but it just works how you'd want it to. The efficiencies you gain are real. 
[data science in VScode](https://code.visualstudio.com/docs/datascience/overview)

[VScode user guide](https://code.visualstudio.com/docs/editor/codebasics) - this looks like a very good guide to the main features.

[python in vscode](https://code.visualstudio.com/docs/python/editing) has incredible tricks and tips. 
[Key binding for VScode](https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-reference)
[Shortcuts in VScode](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)

* shift + enter
run one line in the termianl

* `ctrl + shift + -` - this is a notebook shortcut, splitting the cell in 2, from where your cursor is. 

If having problems connecting your venv to the jupyter kernel. Add the path to the venv in setting.json "python.defaultInterpreterPath" setting. Then select it as an interpreter, then it will show up.
[vscode personalisation](https://iashin.ai/ide_customization.html) - this is a great blog post with loads of good ideas about how to personalise your vsocde experience.

### VScode extensions

* Gitlens - Supercharge git in vscode
    [walkthrough](https://www.youtube.com/watch?v=rxKGgSLwOnU) - tried this out but was a bit maximalist for my taste


## VScode Links

* [Visual Studio videos](https://code.visualstudio.com/docs/introvideos/codeediting)
* [Use venv in vscode](https://code.visualstudio.com/docs/python/environments)
* [Kite for VScode](https://help.kite.com/article/69-using-the-vs-code-plugin)
* [Great reasons to use VS code for developing jupyter notebooks](https://pbpython.com/vscode-notebooks.html)
  * All the top reason for using vscode for notebooks
* [use a snippet with a keyboard shortcut](https://stackoverflow.com/questions/39333639/visual-studio-code-snippet-as-keyboard-shortcut-key)
* [data science in VScode](https://code.visualstudio.com/docs/datascience/overview)
* [VScode user guide](https://code.visualstudio.com/docs/editor/codebasics)
  * A very good guide to the main features.
* [python in vscode](https://code.visualstudio.com/docs/python/editing)
  * Incredible tricks and tips. 
* [Key binding for VScode](https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-reference)
* [Shortcuts in VScode](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)


## RStudio

ctr + 1 - Move focus to editor
ctr + 2 - Move focus to console

## Datagrip
[datagrip wedsite](https://www.jetbrains.com/datagrip/) - click on 'take a tour' for a 45 min intro video.
cmd + j - live templates (snippets of code)
cmd + enter - run code
alt + enter

## Pycharm
This seems to be a very powerful IDE for developing in python

ctr+shft+r - run script
crt+space to auto complete itelisense stuff
opt+enter to add intentions
cmd+shift+a - to find an action within pycharm
alt + up/down to select the word phrase where the caret is. do it multiple times. 

opt+shft+up/down - move lines
cmd+shft+up/down - move whole methods

cmd+ -/= - to minimise/ maximise code
cmd+ shift +  -/= - to minimise/ maximise all code

ctr+shift+up.down to go to next /previous method

ctr+g - to select the sybol, keep pressing to get more. undo the last using ctr+shift+g

the difference between tab completion and enter completion is that tab replaces, enter enters it. Useful to remember. 
postfix completion. add a .if add the end of your expression, itl do the rest. 

use local history, if you want to bring back pieces of code, without undoing code you did after that. 

[Debugging - stepping through the program](https://www.jetbrains.com/help/pycharm/stepping-through-the-program.html)

## Vim/ Vi
Vim is a nice very minimal text editor that is convenient to use from the command line and makes you look like a real developer. Since point and click is not possible all the navigation is done with shortcuts. Run `vimtutor` command in the terminal for a great interactive tutorial.

Vim has 2 modes.
Command mode - to save and quit the program (and other more advance things)
Insert mode. This is used to write and edit text.

Upon creation of a file, vim is in command mode. Typing 'i' changed to insert mode.
Pressing esc returns you to command mode.


## Jupyter

[How jupyter works and collaberating with it](https://www.youtube.com/watch?v=GQr1uMK74F4&ab_channel=PyData)
