# Ketariner

This is a collection of third-party open-source tools and scripts used to manage software packages on Windows.

## Install

1. Download [Katerin](https://ketarin.org/download) and extract the ZIP archive to a location of your choice, e.g. `%LocalAppData%\Programs\Ketarin`.
2. Launch Ketarin. This will create a database named jobs.db under your `%AppData%` folder. For a portable installation that you can easily move between computers, launch Ketarin from the command line as follows to save the database in the same folder as the ketarin.exe executable:
    ```
    cd %LocalAppData%\Programs\Ketarin
    ketarin.exe /database=jobs.db
    ``` 
