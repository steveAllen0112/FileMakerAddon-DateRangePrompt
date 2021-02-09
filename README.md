# FileMakerAddon-DateRangePrompt
Add-on for FileMaker Pro 19+.  When called, displays a configured Card window prompting the user for a Date Range.

# Installation

  To install this addon, do the following steps:

  1. Get the desired Release, and install the Addon for your FileMaker installation in the usual way.

  1. Immediately after installing the Addon:
    
    A. Go to the newly created layout: `Date Range Prompt > Public > Prompt for Date Range {( config )}`
    
    B. Go to Layout Mode (Ctrl/Cmd+L)
    
    C. Select the main group (named in the Objects `Ungroup this group`, and Ungroup it (Shift+Ctrl/Cmd+R).

      There is a bug in FileMaker's Addon installation process that will cause a display issue with the prompt.
      The above steps cause FileMaker to fix the layout automatically and display properly from then on.

  1. OPTIONAL but RECOMMENDED On your first time installing the Addon:

    A. Duplicate the `Date Range Prompt > Public > INTERFACE: Prompt for Date Range {( config )}` script.
       This will produce a script right next to it called `Date Range Prompt > Public > INTERFACE: Prompt for Date Range {( config )} Copy`
    
    B. Delete the original.
    
    C. Rename the copy to remove the appended string, " Copy".
    
    D. Call this duplicate script INSTEAD OF the `Prompt for Date Range {( config )}` script whenever you want to raise the prompt.
       (see comments in the `INTERFACE` script for why.  TL;DR; it makes global customization and upgrading way easier.)
