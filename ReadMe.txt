¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
Alias Run Box
¯¯¯¯¯¯¯¯¯¯¯¯¯
Version 3.2
Sunday, 10 October 2004
________________________________________________________________________

What?
¯¯¯¯¯
The Alias Run Box functions similarly to your standard Windows Run box,
except that it also allows you to execute PowerPro commands (like
PowerPro's command line) and to execute one-word aliases that you
define, with parameters passable to these aliases.
________________________________________________________________________

Requirements
¯¯¯¯¯¯¯¯¯¯¯¯
This script uses features found only in PowerPro versions v4.1 and
above.
________________________________________________________________________

Upgrading
¯¯¯¯¯¯¯¯¯
1. Open your existing ‘ARB.PowerPro’ script (assuming that you haven't
   renamed the script) and copy all of your aliases to a new, temporary
   file; that is, every line following and including the first line that
   starts with an @ sign.

2. Replace your copy of ‘ARB.PowerPro’ with the copy from this archive.

3. Add your own aliases to the bottom of the new copy.

4. Optionally modify the AliasCachePath and CmdHistoryPath variables to
   point to your desired locations again if you initially changed them.

5. Optionally modify the DefaultCmd variable to reference your desired
   default command.

6. Run the PowerPro command ‘.ARB("Rebuild")’ to have any new aliases
   recognised, such as the alias manipulation aliases included with the
   script.

7. If your configuration references the command ‘.ARB("Refresh")’, these
   references will need to be changed to ‘.ARB("Rebuild")’.
________________________________________________________________________

New Installation
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
1. Extract ARB.PowerPro to your Scripts folder, e.g.:
   C:\Program Files\PowerPro\Scripts\ARB.PowerPro

The following steps are optional -- everything will work as expected
if these steps are not taken.

2. Rename the script if you wish. It must however keep its .PowerPro or
   .TXT extension and it must reside immediately under ‘\Scripts’.

3. Add the following command to your Scheduler tab, set to run at
   startup (assuming that you haven't renamed the script):

   .ARB("Load")

   This will load the alias cache into memory at PowerPro startup, which
   will result in ARB displaying virtually instantly when invoked for
   the first time.

4. Modify the AliasCachePath and CmdHistoryPath variables to point to
   your desired locations. These paths will hold a list of aliases found
   in the script and the command history, respectively.

5. Optionally modify the DefaultCmd variable to reference your desired
   default command.
________________________________________________________________________

Invoking
¯¯¯¯¯¯¯¯
Set up a hotkey or bar button to execute the following command, assuming
that you haven't renamed the script:

.ARB

This will open ARB's input box, loading the alias cache into memory
and/or building it if not already done so.
________________________________________________________________________

Usage
¯¯¯¯¯
Invoke ARB's input box in the way that you have programmed (e.g. hotkey,
bar button, mouse click, etc.).

Enter the location of a program, folder, document or Internet resource
to have that item opened.

Enter a PowerPro command to have it executed.

Enter the name of an alias that you have defined and optionally follow
it with a space and parameters to execute this alias.

After entering a few letters, any potential matches will appear beneath
the text field. Pressing Tab will alternate through these choices.

You can create simple aliases through a graphical user interface using
the ‘ARB_Add’ alias. This will allow you to easily add aliases for
documents, programs, one-lined PowerPro commands and such.

You can remove unwanted aliases through ARB using the ‘ARB_Remove’
alias. You will then be prompted for the alias to remove.

You can create more complex aliases or modify existing ones by opening
the script in a text editor and moving to the bottom of the file. This
can be done through ARB's interface via the included ‘ARB_Edit’ alias.
After editing the script, you will need to invoke ARB and run the
‘ARB_Rebuild’ alias for new entries to be recognised.

An alias is defined by preceding its name with an @ sign, and then
every PowerPro command that follows it will be executed until a ‘Quit’
instruction is reached. A few examples are included with the script.
________________________________________________________________________

To Conclude
¯¯¯¯¯¯¯¯¯¯¯
I'd really like to know if you need any help with this script or if it
grows on you, so please feel free to Email me with any questions or
comments that you may have. My Email address can be found through the
PowerPro Yahoo! Group at:

> http://groups.yahoo.com/group/power-pro/

...or you can just leave a message at the Group -- there's a good chance
that I'll see it just as quickly.

Thanks to Ravi, Sean and Luciano Espirito Santo for coming up with the
original idea and implementations.

Best regards,
Alex Peters
________________________________________________________________________

Version History
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
v3.2 (10/10/2004)
*  The ARB_Add, ARB_Remove and Eval aliases no longer require Standard
   Configuration to be enforced in order to work properly
*  The DefaultCmd variable has been introduced near the top of the
   script to aid customising the default entry in ARB's input box
*  The ARB_Rebuild and ARB_Edit aliases now execute without error
*  The Eval alias will now output to a message box if invoked with
   Shift+Enter

v3.1 (5/10/2004)
*  The script no longer conforms to Standard Configuration and should
   now function without modification on any PowerPro v4.1 configuration
   (currently with exception to the ARB_Add, ARB_Remove and Eval
   aliases, which require Standard Configuration for the moment)
*  ARB_Add now adds a commented separator to newly created aliases
*  ARB now accepts any parameter besides "Rebuild" to load the alias
   cache and command history into memory

v3.0 (22/5/2004)
*  Script:
   *  Modified to conform to standard configuration
   *  Renamed included ‘Add’, ‘Rebuild’, ‘Remove’ and ‘Edit’ aliases to
      ‘ARB_Add’, ‘ARB_Rebuild’, ‘ARB_Remove’ and ‘ARB_Edit’
      respectively, as per David Troesch's request
   *  Renamed included ‘Acronym’ alias to ‘Acro’ for ease of typing
   *  Added ‘G’, ‘Go’ and ‘Eval’ aliases -- comments on their usage are
      included within their definitions
*  Documentation:
   *  Added revised plugin inormation to Requirements section

v2.0 (8/5/2004)
*  Script:
   *  Complete rewrite
   *  Added ‘Remove’ alias, as per David Troesch's request
   *  Global variables are no longer created or modified
   *  ARB now responds to "Rebuild" as a parameter instead of
      "Refresh" -- this is intended to cause less confusion as to what
      is performed

v1.1 (6/5/2004)
*  Script:
   *  Added ‘Add’ alias, as per David Troesch's request
*  Documentation:
   *  Added Upgrading section

v1.0 (6/5/2004)
*  Initial release
________________________________________________________________________
