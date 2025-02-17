# Drawing a symbol for schema

Here we will briefly describe how to add your symbol libraries to KiCad.
In the main KiCad project manager menu, select, or click the `OP-amplifier symbol`.

        Tools->Edit Schematic Symbols


## Symbol Editor

Note that one library file may contain more than one schema symbol.
So when naming the new library, keep this in mind if it only contains one specific part or not.
Here we will create a generic library for many Bosch BME680 environment sensor break-out boards. First, in the `Symbol Editor` menu, do the following:

        File->New Library

Name the library `MY-BME680-BOARDS.lib`, put MY as a prefix and use all capital letters, so it stands out in KiCad menus and lists. 
Save the library in the `/new-project-name/kicad/new-project-name-symbols/` folder, i.e., your drawn symbol folder. 
Alternatively, save the new library in the project folder (KiCad default location).

## Scope

The Next dialog will ask for the library scope, `Global` or `Project`, and select `Project`. The list menu is automatically updated.

        Preferences->Manage Symbol Libraries.

The new library should now appear in the list of loaded libraries in the left pane as `MY-BME680-BOARDS`. If not
select from the menu.

        File->Add Library

Select the library file just created.

## Draw a new electrical symbol

Begin to create a new symbol. Let's start with Sparkfun's board. In the menu, select, or click the `OP-amplifier symbol`.

        File->New Symbol

In the first dialog window, decide which library to use for the new symbol, and select our `MY-BME680-BOARDS`.
Open a second properties dialog window. Here name the part `Sparkfun-BME680`, and press `Enter`.
Now draw your symbol. The left pane shows the saved status.
Once finished, save it with (Ctrl-S), or

        File->Save

## Draw another symbol and add it to the library.

Name the new symbol `CJMCU-680`, a standard unbranded Chinese part in six pins configuration.
Save it once done. 

Continue like so with all symbols you wish to put in the library.

## Exit back to KiCad schema/KiCad Manager

Select

        File->Quit

To go back and continue with the design project.

## Tips

In case you need an active low signal, use the `~` before the name so

        ~CS
