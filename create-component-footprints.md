# Create a footprint for a component

Here we will briefly describe how to add your footprints-libraries to KiCad.
In the main KiCad project manager menu, select or click the `IC-circuit` symbol.

        Tools->Edit PCB Footprints


## Footprint Editor

Note that your footprint library may contain many footprints. In the filesystem, the library is the folder that ends with `<library-name>.pretty`.
Here we will create a generic library for several versions of Bosch BME680 environment sensor break-out boards. Since we already made this directory and decided to use this location, go direct to add the folder. If using another location, use `File->New Library`, which essentially creates the `pretty-folder`.

In the `Footprint Editor` menu, do the following:

        File->Add Library

Save the library in the `/new-project-name/kicad/new-project-name-symbols/` folder, i.e., your created footprint folder. Alternatively, save the new library in the project folder (KiCad default location). After this, the new library should appear in the left pane of loaded libraries as `new-project-name-footprints`, if we used the location we have created with the script. 

The Next dialog will ask for the library scope, Global or Project, and select `Project`. Next, add the new library, which will appear in the list under project libraries.

        Preferences->Manage Symbol Libraries.

Go to `Preferences->Manage Footprints Libraries`. Then, in the Project tab for Libraries, use the `MY-FOOTPRINTS` as `Nick name`. I put `MY` as a prefix and use all capital letters, so it stands out in KiCad menus and lists.

## Workflow difference with footprints vs. schema symbol creation

The significant difference when drawing new footprints is that you don't typically create more than the initial project-specific `<library-name>.pretty`,  
already made by the `kicad-init` script. Thus you use `File->New Footprint` and keep adding footprint to the `<library-name>.pretty`. 
Compared to when creating new schema symbols, one may keep opting to either add ` symbols ` in an existing library (*.lib), or create an entirely new library file.

## New footprint

Create a new footprint with

        File->New Footprint

Name the new footprint `BME680-SPARKFUN`.  
Now draw your symbol. The symbol is not saved, as the left pane shows.
Save the new symbol (Ctrl-S), or

        File->Save

You may have to specify in which directory to save the new footprint. Thus, scroll down in the list and select the newly created above.

## Draw another footprint and add it to the library.

Name the new footprint `BME680-PIMORONI`. Save it once done. 

Continue like so with all footprints you wish to put in the library.

## Exit back to KiCad schema/KiCad Manager

Select

        File->Quit

To go back and continue with the design project.

## Tips

* Grid: Use inch, and set a user-grid (View->Grid Settings) to `0.05`, since the pad separation is `0.10`.
* Top fabrication layer: Outline of part, use four mil line thickness
* Front silk screen layer: Indicate parts placement, do not draw on pads. Use eight mil line thickness. Indicate pin `1` with a dot. 
* Front CrtYrd line: To set the `keep out` from the surrounding area around the part. Use two mil line thickness.
* Put parts `REF**` above the footprint and the name below. 
* The header-pin hole diameter is typically 40 mil (ie, 1.02 mm), and the pin mask is set to 74 mils.
* Use the `tab` key to zero `dx`, and `dy` and then move the cursor to measure distance, or use the caliper tool.
* The `anchor` symbol sets the footprint's center if repositioning is required.
* Add some text on the Front Silkscreen to identify the part.

