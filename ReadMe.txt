¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
Alias Run Box
¯¯¯¯¯¯¯¯¯¯¯¯¯
Version 1.1
Thursday, 6 May 2004
________________________________________________________________________

What?
¯¯¯¯¯
The Alias Run Box functions similarly to your standard Windows Run box,
except that it allows you to execute PowerPro commands (like PowerPro's
command line) and to execute one-word aliases that you define, with
parameters passable to these aliases.
________________________________________________________________________

Requirements
¯¯¯¯¯¯¯¯¯¯¯¯
This script uses features found in PowerPro v3.9 and later.

The ‘Use Quote for Escape in Expression Strings’ checkbox, found under
Setup > Advanced Setup > Characters, must be ticked for the script to
work. This option is not ticked by default.
________________________________________________________________________

Upgrading
¯¯¯¯¯¯¯¯¯
1. Open your existing ‘ARB.PowerPro’ script (assuming that you haven't
   renamed the script) and copy all of your aliases to a new, temporary
   file; that is, every line following and including the first line that
   starts with an @ sign.

2. Replace your copy of ‘ARB.PowerPro’ with the copy from this archive.

3. Open the new copy and delete replace the aliases within with your
   own ones.

4. Optionally modify the AliasListPath and HistoryListPath variables to
   point to your desired locations again, if you initially changed them.
________________________________________________________________________

New Installation
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
1. Extract the ‘ARB.PowerPro’ script to your Scripts folder (generally
   ‘C:\Program Files\PowerPro\Scripts’). You may rename the script if
   you wish but it must keep its .PowerPro or .TXT extension and it must
   reside immediately under ‘\Scripts’.

The following steps are optional -- everything will work as expected
even if these are not carried out.

2. Add the following command to your Scheduler tab, set to run at
   startup (assuming that you haven't renamed the script:

   .ARB("Load")

   This will load the alias list into memory at PowerPro startup, so
   that this will not need to be done when the Run box is first shown.

3. Modify the AliasListPath and HistoryListPath variables to point to
   your desired locations. These paths will hold a list of aliases found
   in the script and previously used commands, respectively.
________________________________________________________________________

Invoking
¯¯¯¯¯¯¯¯
Set up a hotkey or bar button to execute the following command, assuming
that you haven't renamed the script:

.ARB

This will open the Run box, loading the alias list into memory and/or
building it if not already done so.
________________________________________________________________________

Usage
¯¯¯¯¯
Invoke the Run box in the way that you choose.

Enter the location of a program, folder, document or Internet resource
to have that item opened.

Enter a PowerPro command to have it executed.

Enter an alias that you have defined and optionally follow it with a
space and a parameter to have this alias get to work.

After entering a few letters, any potential matches will appear beneath
the text field. Pressing Tab will alternate through these choices.

You can create simple aliases through a graphical user interface using
the ‘Add’ alias. This will allow you to easily add aliases for
documents, programs, one-lined PowerPro commands and such.

You can create more complex aliases or modify existing ones by opening
the script in a text editor and moving to the bottom of the file. After
editing the script, you will need to Invoke the Run box and run the
‘Refresh’ aliases for new entries to be recognised.

An alias is defined by preceding its name with an @ sign, and then
every PowerPro command that follows it will be executed until a ‘Quit’
instruction is reached. A few examples are included in the script.
________________________________________________________________________

To Conclude
¯¯¯¯¯¯¯¯¯¯¯
I'd really like to know if you need any help with this script, or if it
grows on you, so please feel free to Email me with any questions or
comments that you may have. My Email address can be found through the
PowerPro Yahoo! group, at:

> http://groups.yahoo.com/group/power-pro/

...or you can just leave a message at the Group -- there's a good chance
that I'll see it just as quickly.

Thanks to Ravi, swzoh and Luciano Espirito Santo for coming up with the
original idea and implementations.

Best regards,
Alex Peters
________________________________________________________________________

Version History
¯¯¯¯¯¯¯¯¯¯¯¯¯¯¯
v1.1 (6/5/2004)
* Script:
  * Added ‘Add’ alias, as per David Troesch's request
* Documentation:
  * Added Upgrading section

v1.0 (6/5/2004)
* Initial Release
________________________________________________________________________
