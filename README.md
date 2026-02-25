# LaTeX input method for MacOS

This [MacOS input method](https://support.apple.com/guide/mac-help/create-and-use-your-own-input-source-on-mac-mchlp2866/mac) for typing math symbols on MacOS using LaTeX macro names.

## Installation

1. Download the **raw format** of [`LaTeX.inputplugin`](./LaTeX.inputplugin) file found in this repository. You must make sure to get the original file in the UTF-16 format, either by cloning the repository to your computer, or clicking on the file in your browser and downloading it in raw form by pressing the download button in the upper right corner above the file. **Do not attempt to cut and paste**, it will not work.

2. Let us assume you downloaded the file at `~/Downloads/LaTeX.inputplugin`. The next step is to remove the Apple security check that would cause your computer to reject it. In the terminal window, run the commands

        cd ~/Downloads
        xattr -d com.apple.quarantine LaTeX.inputplugin

    If you are afraid of the command line, you can proceed to the next step directly. If the OS complains go through the usual process of enabling the file via “Settings → Privacy & Security” (scroll to the bottom).

3. Double-click on the file `LaTeX.inputplugin` in Finder. It will look like nothing happened, but with luck MacOS registered it.

4. Logout and login.

5. Go to “System settings → Keyboard → Text input → Edit…”, then press `+` in lower-left corner to add a new input method. Find “LaTeX” and add it to your input sources (it might be a bit hard to find, it tends to hide under Chinese, Simplified).

5. Possbily logout and login again if you do not see LaTeX as input source.

6. Set up a convenient keyboard shortcut for switching between keyboards under “System settings → Keyboard → Keyboard shortcuts → Input Source”

To type `β` switch to the LaTeX input method and type `beta` and space (no backslash `\`). Consult `LaTeX.inputplugin` to see what can be typed.

## How to customize the symbols

You may customize the file easily enough, just keep in mind:

1. The file must be saved in UTF-16 format:

   * Emacs: use `C-x C-m f`, select `utf-16`, then save the file.
   * Visual Studio Code: the coding is displayed in the status line at the bottom, on the right. You may click on it to select an encoding.

2. The input string and the symbol must be separated by a TAB.