# FileMakerAddon-DateRangePrompt
Add-on for FileMaker Pro 19+.  When called, displays a configured Card window prompting the user for a Date Range.

# Installation

  To install this addon, do the following steps:

  1. Get the desired Release, and install the Addon for your FileMaker installation in the usual way.

  1. Immediately after installing the Addon:
    a. Go to the newly created layout: `Date Range Prompt > Public > Prompt for Date Range {( config )}`
    
    a. Go to Layout Mode (Ctrl/Cmd+L)
    
    a. Select the main group (named in the Objects `Ungroup this group`, and Ungroup it (Shift+Ctrl/Cmd+R).

      There is a bug in FileMaker's Addon installation process that will cause a display issue with the prompt.
      The above steps cause FileMaker to fix the layout automatically and display properly from then on.

  1. OPTIONAL but RECOMMENDED On your first time installing the Addon:

    a. Duplicate the `Date Range Prompt > Public > INTERFACE: Prompt for Date Range {( config )}` script.
       This will produce a script right next to it called `Date Range Prompt > Public > INTERFACE: Prompt for Date Range {( config )} Copy`

    a. Delete the original.
    
    a. Rename the copy to remove the appended string, " Copy".
    
    a. Use this duplicate script INSTEAD OF the `Prompt for Date Range {( config )}` script whenever you want to raise the prompt.
    
      (see comments in the `Date Range Prompt > Public > INTERFACE: Prompt for Date Range {( config )}` script for why)
