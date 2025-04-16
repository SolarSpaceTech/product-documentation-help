---
id: 49
seoTitle: Windows - Guide - Utility
displayName: For Windows
order: 20
published: true
historyName: Windows Utility Guide
historyDescription: Installation and Update Instructions
---

# Windows Utility Guide

This guide will help you install and use the utility on Windows.

1. Preparing the Utility
   - **Obtain the utility**: Ensure you have the self-extracting script `pd.bat` for Windows. It should be located
   at the same level as your documentation directory.2. Directory Organization
   - **Utility Location**: Place the `pd.bat` file in the same directory as your documentation or one level above it.
   - **Rename the documentation directory**: The documentation directory should be named `content`. If it has
   a different name, rename it to `content`.
   - **Note**: Although you can change the documentation directory path using the `PD_CONTENT_DIR` variable
   in the `pd.bat` script, it is recommended to simply rename the directory to `content` as the set value may reset
   with updates.3. First Run of the Utility
   - **Run the utility**: Double-click on the `pd.bat` file in Windows File Explorer to execute it.
   - **Extracting Files**: During the first run, the `bin` and `plugins` directories will be created. This may take
   a while; try to close all other applications before the first run.



## Subsequent Runs

- **Startup Optimization**: On subsequent runs, the utility will not re-extract the `bin` directory,
speeding up the startup process.
- **Plugin Update**: The `plugins` directory will be re-extracted each time the utility runs, allowing for updates
to existing `plugins` and the addition of new ones without reinstalling the entire utility.

## Updating and Adding Plugins

- **Updating the Utility**: Replace the `pd.bat` file and delete the `bin` and `plugins` directories.
- **Updating Plugins**: Place the new plugin version in the `plugins` directory.
- **Adding New Plugins**: Add a new plugin to the `plugins` directory.
