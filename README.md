# LaTeX input method for MacOS

This [MacOS input method](https://support.apple.com/guide/mac-help/create-and-use-your-own-input-source-on-mac-mchlp2866/mac) is based on [TeX113](https://gist.github.com/pyrocto/22a92ecbe4f5423ea0bed3e0607d8642) input.

## How to install and use the input method

1. Download the **raw format** of `LaTeX.inputplugin` file found here. You must make sure to get the original file in the UTF-16 format (do not attempt to cut and paste). The best way to do this is to clone the gist with `git clone ⟨gist-location⟩` where the location can be obtained in the upper right corner of this web page (select "Clone via ..." where you see "Embed").
2. Double-click on it in Finder. It will process by the operating system and placed into `~/Library/Input Methods` folder. (Do *not* put it in that folder by hand.)
3. Logout and login.
4. Go to “System settings → Keyboard → Text input → Edit…”, then press `+` in lower-left corner to add a new input method. Find “LaTeX” and add it to your input sources (it might be a bit hard to find, it tends to hide under Chinese, Simplified).
5. Set up a convenient keyboard shortcut for switching between keyboards under “System settings → Keyboard → Keyboard shortcuts → Input Source”

To type `β` switch to the LaTeX input method and type `beta` and space. Consult `LaTeX.inputplugin` to see what can be typed.

## How to customize the symbols

You may customize the file easily enough, there is just one catch: you need to save the file in UTF-16 format. On Emacs you can accomplish this with `C-x C-m f`, select `utf-16`, then save the file.