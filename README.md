# KiCAD init project folder structure v2
# NEW - migrated original for future updates

![Placeholder for missing photographs](./images/placeholder-for-missing-photographs.png)

[Placeholder for missing photographs](./images/placeholder-for-missing-photographs.png)

[![GitHub version](https://img.shields.io/github/release/berrak/berrak/kicad-init-file-structure.svg?logo=github&logoColor=ffffff)](https://github.com/berrak/berrak/kicad-init-file-structure/releases/latest)
[![GitHub Release Date](https://img.shields.io/github/release-date/berrak/berrak/kicad-init-file-structure.svg?logo=github&logoColor=ffffff)](https://github.com/berrak/berrak/kicad-init-file-structure/releases/latest)
[![GitHub stars](https://img.shields.io/github/stars/berrak/berrak/kicad-init-file-structure.svg?logo=github&logoColor=ffffff)](https://github.com/berrak/berrak/kicad-init-file-structure/stargazers)
[![GitHub issues](https://img.shields.io/github/issues/berrak/berrak/kicad-init-file-structure.svg?logo=github&logoColor=ffffff)](https://github.com/berrak/berrak/kicad-init-file-structure/issues)
![Badge Hit Counter](https://visitor-badge.laobi.icu/badge?page_id=berrak_berrak/kicad-init-file-structure)


Initiates the disk folder structure with the `kicad-init.sh` script.
Files and directories are named identical except for the KiCad-project name.

Replace the zero-sized placeholder files with actual files.

## Install the script

Download or clone this repository, and then copy the shell script into your $PATH

        cd bin
        sudo cp ./kicad-init.sh /usr/local/bin/kicad-init.sh

alternatively:

        cd bin
        cp ./kicad-init.sh $HOME/.local/bin/kicad-init.sh

## Run script

Run the script in the root of the new KiCad project, with the new project name as an argument.

        mkdir ~/KICAD-2022
        cd KICAD-2022
        bash kicad-init.sh "new-project-name"

Set up the `new-project-name` as a potential GitHub repository, and do `git init` to get started.

Install the useful `tree` command

        sudo install tree
        
The script creates the following directory structure for the new KiCad project:

        ~/KICAD-2022/new-project-name$ tree -a
        ├── 3rd-parties-libraries
        │   ├── tmp        
        │   ├── 3D-models
        │   ├── footprints.pretty
        │   └── schematic-symbols
        ├── fabrication
        │   ├── assembly
        │   │   ├── place-holder-for-missing-bom-file
        │   │   └── place-holder-for-missing-footprint-position-file
        │   └── gerbers
        │       └── placeholder-for-missing-zip-archive
        ├── images
        │   └── placeholder-for-missing-photographs
        ├── datasheets
        │   └── placeholder-for-missing-datasheet-files
        ├── kicad6
        │   ├── new-project-name-3D-models
        │   ├── new-project-name-footprints.pretty
        │   └── new-project-name-schematic-symbols
        ├── LICENSE.md
        ├── README.md
        └── schematic-diagram
            └── placeholder-for-missing-schematic-pdf

## Start KiCad

Start KiCad in the `new-project-name/kicad6` directory, create the new project (`File->New->Project`), and name the new project `new-project-name`. KiCad will create this directory and populate it with the standard KiCad project files.

## Directory contents

* **/new-project-name/kicad6/new-project-name** - KiCad project, schema and board design files
* **/new-project-name/3rd-parties-libraries** - schematic symbols, footprints, and 3D models downloaded from e.g [SnapEDA](https://www.snapeda.com/home/), [UltraLibrarian](https://www.ultralibrarian.com), [Componentsearch](https://componentsearchengine.com), and [grabcad](https://grabcad.com).
* **/new-project-name/kicad6/new-project-name-schematic-symbols** - schematic symbols drawn by yourself
* **/new-project-name/kicad6/new-project-name-footprints.pretty** - footprints drawn by yourself
* **/new-project-name/kicad6/new-project-name-3D-models** - 3D-models created by yourself
* **/new-project-name/fabrication** - fabrication output files; eg bom, gerbers, assembly footprint position
* **/new-project-name/images** - KiCad rendered images of the created design
* **/new-project-name/schematic-diagram** - schematic diagram for the created design
* **/new-project-name/datasheets** - important datasheets


## Planned Improvements/Changes

For planned changes, improvements, and possible encountered issues, please visit the [Github issues tracker](https://github.com/berrak/berrak/kicad-init-file-structure/issues).
