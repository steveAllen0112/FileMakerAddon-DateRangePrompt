# FileMakerAddon-DateRangePrompt
Add-on for FileMaker Pro 19+.  When called, displays a configured Card window prompting the user for a Date Range.

# Installation

To install this addon, do the following steps:

  1. Get the desired Release ([latest](https://github.com/steveAllen0112/FileMakerAddon-DateRangePrompt/releases/latest)), and install the Addon into your FileMaker installation in the usual way.

     You can obtain the Addon itself from either the `dist/` folder of the Source Code, OR
     through the official release file, `Date_Range_Module_Add-On.zip`.
     
     Whichever location you get it from, you will find two options:
     
     A. Drag the `Date_Range_Module_Add-On` folder to the appropriate installation location.
     
     B. (Mac only) Double-click the `Date_Range_Module_Add-On.fmaddon` file.
     
     Note that Option A is recommended, because Option B will result in the module showing without full information in FileMaker.
     It will show in category called `__...__`, with the generic icon, no preview, and supposedly authored by Claris!
     None of this, of course, is correct, but it _is_ the default, which as of yet we don't have a way to override in the `.fmaddon` file.

  2. Immediately after installing the Addon:
    
     A. Go to the newly created layout: `Date Range Prompt > Public > Prompt for Date Range {( config )}`
    
     B. Go to Layout Mode (Ctrl/Cmd+L)
		
     C. Select the main group (named in the Objects `Ungroup this group`, and Ungroup it (Shift+Ctrl/Cmd+R).
		
     There is a bug in FileMaker's Addon installation process that will cause a display issue with the prompt.
		
     The above steps cause FileMaker to fix the layout automatically and display properly from then on.

  3. OPTIONAL but RECOMMENDED On your first time installing the Addon:

     A. Duplicate the `INTERFACE: Prompt for Date Range {( config )}` script.
        This will produce a script right next to it in the same folder called `INTERFACE: Prompt for Date Range {( config )} Copy`
     
     B. Delete the original.
    
     C. Rename the copy to remove the appended string, " Copy".
     
     D. Optionally (recommended) move the script somewhere outside the Addon's script folder.
    
     E. Call this duplicate script INSTEAD OF the `Prompt for Date Range {( config )}` script whenever you want to raise the prompt.
        See comments in the `INTERFACE` script for why.  TL;DR; it makes global customization and upgrading way easier.

# Usage

  After installation, to raise a prompt, call the INTERFACE script, per the recommendation (see above).  Or else call the `Prompt for Date Range {( config )}` script directly, if you must.
  
  Pass in a JSON Object to the Script Parameter, with the configuration options you want, if any.
  
  (See the comments in the script `Prompt for Date Range {( config )}` for configuration options.)
