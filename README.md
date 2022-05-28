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

# How to Use

## Template nomenclature

Template names follow this convention: `<appname>-<architecture>[-unofficial].xml`.

- **appname:** Application name
- **architecture:** Hardware architecture
- **[-unofficial]:** Optional, indicates unofficial installer

1. Download the desired template file in XML format (e.g. `Zotero.xml`).
2. Launch `Ketarin.exe`.
3. From the menu bar, select `File`, followed by `Import...`.
4. Select the template file and click `Open`.

File names ending in `-unofficial.xml` refer to templates that generate a custom installer. The official installers of some apps will not allow installation to proceed without administrator rights. The custom installer be used to circumvent the requirement for administrator rights by installing the software in a user-writable location, e.g. `%LocalAppData%`.
