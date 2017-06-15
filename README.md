# SanskritDictionariesInstaller
Generates Simple Installer for Sanskrit Dictionaries created by Sanskrit Programmers group

The goal of this project is to provide a simple installer for the [stardict Sanskrit dictionaries](https://github.com/sanskrit-coders/stardict-sanskrit) created by the [Sanskrit Programmers group](https://sites.google.com/site/sanskritcode/home) using [Goldendict](http://www.goldendict.org) as the dictionary program. [Izpack](http://izpack.org) is used to generate the installer based on the provided configuration files.

In this initial version, the installer includes all the [released dictionaries](https://archive.org/download/stardict_collections/all_dicts_stardict_sanskrit.tar.gz) from the stardict-sanskrit project. However, the install.xml file can be easily modified to create custom installers.

## Installer
The generated installer is available [here](https://archive.org/download/SanskritDictionariesInstaller/SanskritDictionariesInstaller.jar)

## Installer Generation Files
The files used to create the installer are available in the Izpack-files folder. Note that this does not include Goldendict or the actual repositories.

### To generate the installer
1. Clone the repository and cd to Izpack-files
2. Download the latest version of Goldendict Portable for Windows from [goldendict.org](http://www.goldendict.org/download.php) and rename it to GoldenDict.zip
3. Download the latest release of [stardict Sanskrit dictionaries](https://github.com/sanskrit-coders/stardict-sanskrit)
4. Run $IZPACK_INSTALL_DIR/bin/compile.bat install.xml -b . -o ../Installer/SanskritDictionariesInstaller.jar -h $IZPACK_INSTALL_DIR


## TODO
1. Provide users the option to choose which dictionaries to install. Could parse the tars.MD list from the stardict-sanskrit git repo and auto-generate the corresponding entries in the install.xml file
2. Taking it a step further, could migrate to a web installer which automatically downloads the tars.MD list, and presents the dictionary options to the user. It could then download and extract the files. Could leverage the ideas from [pydictupdater] (https://github.com/nangia/pydictupdater). The installer would not need to be updated each time.
