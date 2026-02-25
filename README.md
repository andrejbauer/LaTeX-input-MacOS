# LaTeX input method for MacOS

This [MacOS input method](https://support.apple.com/guide/mac-help/create-and-use-your-own-input-source-on-mac-mchlp2866/mac) for typing math symbols on MacOS using LaTeX macro names.

## Installation

MacOS is quite brittle and finicky when it comes to installing input methods. The following instructions work on Sequoia 15.7.4.

### Download the file in raw input format

Download the **raw format** of [`LaTeX.inputplugin`](./LaTeX.inputplugin) file found in this repository. You must make sure to get the original file in the UTF-16 format, either by cloning the repository to your computer, or clicking on the file in your browser and downloading it in raw form by pressing the download button (it looks like a downward arrow pointing to a tray) in the upper right corner above the file. **Do not attempt to cut and paste**, it will not work.

### Installation

1. Let us assume you downloaded the file at `~/Downloads/LaTeX.inputplugin`. If not, change the `cd` command below accordingly. Open a terminal window and run these commands:

        cd ~/Downloads
        mkdir -p ~/Library/Input\ Methods
        xattr -d com.apple.quarantine LaTeX.inputplugin
        open LaTeX.inputplugin

    Explanation of the above code: we switch to the directory where your file is, we optionally create the destination directory `~/Library/Input Methods`, we remove Apple security check that prevents the file from being open, and then we open the file.

    If all went well, the file `LaTeX.inputplugin` has appeared in `~/Library/Input\ Methods`, which you can check by running

        ls ~/Library/Input\ Methods

    Do **not** attempt to place the file in `~/Library/Input Methods` by hand.

2. Logout and login. This will cause MacOS to recognize the new input method.

3. Go to “System settings → Keyboard → Text input → Edit…”, then press `+` in lower-left corner to add a new input method. Find “LaTeX” and add it to your input sources (it might be a bit hard to find, it tends to hide under Chinese, Simplified).

4. Possbily logout and login again if you do not see LaTeX as input source.

5. Set up a convenient keyboard shortcut for switching between keyboards under “System settings → Keyboard → Keyboard shortcuts → Input Source”

## Usage

To type `β` switch to the LaTeX input method and type `beta` and space (no backslash `\`). If you are in the LaTeX input method but want to type ordinary text, type it and press Enter.

Consult `LaTeX.inputplugin` to see what can be typed.

# Customization

You may customize the file easily enough, just keep in mind:

1. The file must be saved in UTF-16 format:

    * Emacs: use `C-x C-m f`, select `utf-16`, then save the file.
    * Visual Studio Code: the coding is displayed in the status line at the bottom, on the right. You may click on it to select an encoding.

    After editing the file, you can check if it is still correctly encoded by running the command

        file -I LaTeX.inputplugin

    It should say `LaTeX.inputplugin: text/x-c; charset=utf-16be`.

2. The input string and the symbol must be separated by a TAB, not spaces.