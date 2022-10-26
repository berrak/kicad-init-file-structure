# Clone the KiCad project (change names/paths) for a new project.

Sometimes it makes sense to continue with a new design based on an existing project but keep the old one intact. Here we do not only want to clone the schematics but also `pcb-layout` and all other aspects of the original design. So the new plan starts by editing/changing and adding elements to the cloned kiCad project.

## The overall process.

1. Create the new-name-directory at the same level as an old project.
2. Recursively copy the old project files into the new project tree.
3. Remove fabrication output contents.
4. Remove, in the KiCad directory, the `fp-info-cache` file and the `backups` directory. 
5. Use the `rpl` command to first simulate a run, with the `-s` option for the text replacement, i.e., the project name.
6. Replace the old project name with the new project name.
7. Rename a few KiCad files in the KiCad directory and the directory path up to the top folder.
8. Done!


## Install rpl.

```
sudo apt-get install rpm
```

## Create a new directory and copy files recursively.

Do not leave whitespace in the project name; here, use a hyphen like `new-project-name`.

```
mkdir new-project
cp -r old-project/* new-project
```

Remove the `fabrication` files, the `cache` file, and the `backup` directory in the KiCads home directory. Also, remove all pdf-datasheets and the ` tmp`-directory, which rpl does not handle. Finally, copy the datasheets manually and delete any temporary files to save space.

## Use rpl to replace text string and paths inside KiCad files.

If the rpl simulated run results in failures, see above.

```
cd new-project-name
rpl -s -R old-project-name new-project-name *
rpl -R old-project-name new-project-name *
```
## Rename files and the KiCad home directory.

Finally, rename a few files in the KiCad directory with the prefix `new-project-name` and update the directory path with the new project name.

Open the new project, and everything is now ready.