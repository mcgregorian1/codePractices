# Visual Studio Code

## What is it?
VSCode is an integrated development environment (IDE) like RStudio, but it supports many more coding languages and has other methods of helping people code faster, like extensions. It can be downloaded from [here](https://code.visualstudio.com/download).
- For general documentation, see [here](https://code.visualstudio.com/docs).
- For a more in-depth overview of why people like it, see [here](https://shiftmag.dev/vs-code-171/) from 2023.

## Tutorial
My labmate Xiaojie Gao gave a presentation about using R in VSCode during our PhD in 2022 and he put his resources on GitHub - you can find them [here](https://github.com/MrJGao/vscode_r_intro).

## Other useful information
### Extensions
VSCode runs on extensions, some of which are provided by default and many others that individuals have created. Extensions are used both for using your coding language (like R or Python) and for facilitating how you code (like allowing you to fold coding chunks).

Here are some extensions that are helpful:
- #region folding
- Code spell checker
- Better comments
- Path intellisense (automatic path completion when writing code)
- Color Pick (choose colors interactively in R (e.g.))
- Project Manager (similar to "Projects" in RStudio)
- Rainbow CSV (color codes csv columns when viewed in VSCode)

Some other extensions that are good too
- Live Share (allows you to look at the same document with someone else and edit like a google doc)
- Markdown All in One

Of course, you also need to add the extension for the coding language you're using, e.g.
- R
- Python
- Pylance

### Keyboard shortcuts
VSCode has **many** keybindings (keyboard shortcuts). Here are a couple useful ones
- collapse all code chunks = cmd + k + 0
- open all code chunks = cmd + k + cmd + j
- open a terminal = cmd + j
- search for settings = ctrl + shift + p

### Settings for R and Python
Note that you may have to restart VSCode after changing some of these settings in order to see it take effect.

#### Tips for using R
Use active terminal
- By default, when you try to run a line of R code by doing Ctrl + enter, VSCode will open an interactive R terminal. If you instead just want it to use whatever terminal you have open (e.g. when using a conda environment), go to settings and type "R active terminal", then click in the box under "R: Always use active terminal".

Have plots show within VSCode
- This requires the use of the `httpgd` and `languageserver` packages, which you will need to install within R. See this [stack question](https://stackoverflow.com/questions/52284345/how-to-show-r-graph-from-visual-studio-code) for steps.

Get rid of all the blue squiggles
- Each wavy line corresponds to a recommended way to write the code to a specific standard. The easiest way to get rid of these is to open settings, type "r.lsp", and then uncheck the box under "R>Lsp:Diagnostics".
- For a more thorough discussion and a more fine-tuned way to do change when the lines appear, see [this stack question](https://stackoverflow.com/questions/68858490/disable-r-linting-in-vscode).

#### Tips for using Python
Run code with ctrl + enter like in R
- The default way to run lines of code in Python is by doing Shift + enter. If you want to change that, go to Keybindings (Keyboard shortcuts), type "Run selection", then click on the pencil next to the entry labeled "Python: Run selection/line in python terminal". Type Ctrl + enter, then press enter again.

Run line of code and have cursor move to next line like in R:
- Install the extension "macros" by user geddski
- Follow the steps on [this stack question](https://stackoverflow.com/questions/58404225/vs-code-python-move-to-next-line-on-run-ctrl-enter) - the top answer should be enough, but if you want to do the same thing for Jupyter things, you will also need to input the changes in the second top answer.
