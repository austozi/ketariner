# Ketariner

This is a collection of third-party open-source tools and scripts used to manage software packages on Windows.

(This is work in progress)

## Install

### Ketarin

1. Download [Ketarin](https://ketarin.org) and extract the ZIP archive to a location of your choice, e.g. `%LocalAppData%\Programs\Ketarin`.
2. Launch Ketarin. This will create a database named jobs.db under your `%AppData%` folder. For a portable installation that you can easily move between computers, launch Ketarin from the command line as follows to save the database in the same folder as the ketarin.exe executable:
    ```
    cd %LocalAppData%\Programs\Ketarin
    ketarin.exe /database=jobs.db
    ``` 

### Inno Setup

1. Download and install [Inno Setup](https://jrsoftware.org/isdl.php).
2. Copy the Inno Setup folder to the Ketarin folder above, e.g. `%LocalAppData%\Programs\Ketarin\Utils\Inno Setup`.

### 7-Zip

1. Download and install [7-Zip](https://www.7-zip.org) to the Ketarin folder, e.g. `%LocalAppData%\Programs\Ketarin\Utils\7-Zip`.

# How to Use

## Template nomenclature

Template names follow this convention: `<appname>-<architecture>[-unofficial].xml`.

- **appname:** Name of the sofware application.
- **architecture:** Hardware architecture, see below.
- **[-unofficial]:** Optional, indicates unofficial installer.

## Hardware architecture

| Label | Executable              | Windows compatibility |
|-------|-------------------------|-----------------------|
| win32 | 32-bit                  | 32-bit and 64-bit     |
| win64 | 64-bit                  | 64-bit only           |
| w6432 | 64-bit and 32-bit       | 32-bit and 64-bit     |



1. Download the desired template file in XML format (e.g. `Zotero.xml`).
2. Launch `Ketarin.exe`.
3. From the menu bar, select `File`, followed by `Import...`.
4. Select the template file and click `Open`.

File names ending in `-unofficial.xml` refer to templates that generate a custom installer. The official installers of some apps will not allow installation to proceed without administrator rights. The custom installer be used to circumvent the requirement for administrator rights by installing the software in a user-writable location, e.g. `%LocalAppData%`.
