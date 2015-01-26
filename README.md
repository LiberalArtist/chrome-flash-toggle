# chrome-flash-toggle
This is a pair of AppleScript scripts I use to quickly enable/disable the PPAPI Flash plugin in Google Chrome.

(It's also my first experiment with using github.)

I wrote these because I find running Flash, even if it's not actually doing anything, takes more of a toll than I'd like on my system resources. Since enough of the world has finally switched to HTML5 video that I can get by without it most of the time, I try to disable it when I'm not actually using it; however, going manually to `chrome://plugins` every time all the time got rather tedious.

**Known Issues**

0. When Chrome automatically updates to a new version, the scripts break until you relaunch Chrome. I immagine that this is because the `version` Chrome reports to AppleScript is temporarily different than the version number that shows up in the path to the file.
1. AppleScript is not an ideal way to implement this, since it's very platform-specific and external to Chrome. However, Chrome restricts running JavaScript, extensions, etc. on pages in the `chrome://` zone, and AppleScript was the best way I could find to get around it. See detailed discussion at http://stackoverflow.com/questions/23797209/enable-disable-chrome-plugin-from-extension
2. There is no indicator of what the current status of Flash is.

**Serving Suggestion**

Place both script files in `~/Library/Scripts` and show the AppleScript menu in the menu bar. That will leave you just two clicks awaw from enabling or disabling Flash.

(To show the AppleScript menu, open the `AppleScript Editor` program, open "Preferences" (`⌘,`), and check the box next to "Show Script menu in menu bar".)
