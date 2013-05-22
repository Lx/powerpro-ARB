# Alias Run Box (ARB) v4.0

Written by Alex Peters, 13/6/2005

## What?

The Alias Run Box functions similarly to your standard Windows Run box,
except that it also allows you to execute PowerPro commands (like
PowerPro's command line) and to execute one-word aliases that you
define, with parameters passable to these aliases.

Aliases may exist as labels within the ARB script and/or as external
scripts matching a user-specified wildcard.  For those not interested
in backward compatibility with internal aliases a lighter,
'external-only' edition without that facility is included.

## Requirements

This script uses features found only in PowerPro versions 4.1 and above.

## Installation

Instructions vary depending on whether you are upgrading from a
previous ARB version or performing a fresh install.

### Upgrading from earlier versions

1.  Open your existing `ARB.PowerPro` script (assuming that you haven't
    renamed the script) and copy all of your aliases into a new,
    temporary file; that is, every line following and including the
    first line that starts with an `@` sign.

2.  Replace your copy of `ARB.PowerPro` with the copy from this archive.

3.  Add your own aliases to the bottom of the new copy.

4.  Optionally modify the `CACHE_PATH` (formerly `AliasCachePath`) and
    `HISTORY_PATH` (formerly `CmdHistoryPath`) variables to point to
    your desired locations again if you initially changed them.

5.  Extract the `ARB_Aliases` folder into your PowerPro `Scripts`
    folder.  If you wish to rename it, ensure that you update the
    `EXT_PREFIX` variable in the script accordingly.

6.  Remove any PowerPro configuration references to `.ARB("Rebuild")`
    or `.ARB("Refresh")` as this task is now performed automatically.

### Fresh install

1.  Extract `ARB.PowerPro` (or `ARB_External.PowerPro` if you don't
    want to define any aliases within the ARB script itself) into your
    PowerPro `Scripts` folder, e.g.:

        C:\Program Files\PowerPro\Scripts\ARB.PowerPro

2.  Optionally rename the script if you wish.  If you choose to extract
    the 'external-only' edition, you may want to rename it to simply
    `ARB.PowerPro`.

3.  Optionally modify the `HISTORY_PATH` variable to point to your
    desired location.  The file referenced by this path will hold the
    command history.

4.  If you extracted the 'hybrid' version of ARB (which also supports
    alias definitions internal to the script itself), optionally modify
    the `CACHE_PATH` variable to point to your desired location.  The
    file referenced by this path will hold internal alias cache data.

5.  Extract the `ARB_Aliases` folder into your PowerPro `Scripts`
    folder.  If you wish to rename it, ensure that you update the
    `EXT_PREFIX` variable in the script accordingly.

## Invoking

Set up a hotkey or bar button to execute the following command,
assuming that you have named the script `ARB.PowerPro`:

    .ARB

This will open ARB's input box.

## Usage

Invoke ARB's input box in the way that you have programmed (e.g.
hotkey, bar button, mouse click, etc.).

*   Enter the location of a program, folder, document or Internet
    resource to have that item opened.

*   Enter a PowerPro command to have it executed.

*   Enter the name of an alias that you have defined and optionally
    follow it with a space and parameters to execute this alias.  After
    entering a few letters, any potential matches will appear beneath
    the text field.  Pressing Tab will alternate through these choices.

You can create more complex aliases in the `ARB_Aliases` folder of your
PowerPro `Scripts` folder.  Aliases can accept arguments via `arg(1)`.
Refer to the existing alias definitions in this folder for a better
idea of how new ones are written.

The 'hybrid' version of ARB may also contain 'internal' aliases, found
by opening the script in a text editor and moving to the bottom of the
file.  An internal alias is defined by preceding its name with an `@`
sign, and then every PowerPro command that follows it will be executed
until a `Quit` instruction is reached.  Examples of internal aliases
are not provided as use of external aliases is more highly recommended.

## Support

Questions and comments regarding this script can be posted to the
PowerPro Yahoo! Group:

*   http://groups.yahoo.com/group/power-pro/

Bug reports and feature requests can be submitted on GitHub, where the
code for this script is hosted:

*   https://github.com/Lx/powerpro-ARB/issues

## Acknowledgments

Thanks to Ravi, Sean and Luciano Espirito Santo for coming up with the
original idea and implementations.

## Version history

### v4.0 (13/6/2005)

*   Externally defined aliases are supported; see the `EXT_PREFIX`
    variable in the script.
*   New internal aliases are automatically recognised, making the use
    of `.ARB("Rebuild")` and `.ARB("Refresh")` unnecessary.
*   The ARB box's initial value defaults to its last used command
    string, removing the need for a `DefaultCmd` configuration
    variable.
*   Aliases `ARB_Add`, `ARB_Remove` and `ARB_Edit` are no longer
    provided; using external aliases is now preferred.
*   All other previously internal aliases are now provided as external
    ones.

### v3.2 (10/10/2004)

*   The `ARB_Add`, `ARB_Remove` and `Eval` aliases no longer require
    Standard Configuration to be enforced in order to work properly
*   The `DefaultCmd` variable has been introduced near the top of the
    script to aid customising the default entry in ARB's input box
*   The `ARB_Rebuild` and `ARB_Edit` aliases now execute without error
*   The `Eval` alias will now output to a message box if invoked with
    Shift+Enter

### v3.1 (5/10/2004)

*   The script no longer conforms to Standard Configuration and should
    now function without modification on any PowerPro v4.1
    configuration (currently with exception to the `ARB_Add`,
    `ARB_Remove` and `Eval` aliases, which require Standard
    Configuration for the moment)
*   `ARB_Add` now adds a commented separator to newly created aliases
*   ARB now accepts any parameter besides "Rebuild" to load the alias
    cache and command history into memory

### v3.0 (22/5/2004)

*   Script:
    *   Modified to conform to standard configuration
    *   Renamed included `Add`, `Rebuild`, `Remove` and `Edit` aliases
        to `ARB_Add`, `ARB_Rebuild`, `ARB_Remove` and `ARB_Edit`
        respectively, as per David Troesch's request
    *   Renamed included `Acronym` alias to `Acro` for ease of typing
    *   Added `G`, `Go` and `Eval` aliases -- comments on their usage
        are included within their definitions
*   Documentation:
    *   Added revised plugin information to Requirements section

### v2.0 (8/5/2004)

*   Script:
    *   Complete rewrite
    *   Added `Remove` alias, as per David Troesch's request
    *   Global variables are no longer created or modified
    *   ARB now responds to "Rebuild" as a parameter instead of
        "Refresh" -- this is intended to cause less confusion as to
        what is performed

###v1.1 (6/5/2004)

*   Script:
    *   Added `Add` alias, as per David Troesch's request
*   Documentation:
    *   Added Upgrading section

### v1.0 (6/5/2004)

*   Initial release
