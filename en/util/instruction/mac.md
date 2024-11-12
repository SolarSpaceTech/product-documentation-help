---
id: 48
title: MacOS - Guide - Utility
displayName: For MacOS
order: 10
published: true
historyName: MacOS Utility Guide
historyDescription: Installation and Update Instructions
---

# MacOS Utility Guide

This guide will help you install and use the utility on macOS.
1. Preparing the Utility
   - **Obtain the utility**: Ensure you have the self-extracting script `pd` for macOS. It should be located in the same
   directory as your documentation.<br/>

2. Directory Organization
   - **Utility Location**: Ensure the utility pd is at the same level as the documentation directory.
   - **Rename the documentation directory**: The documentation directory should be named `content`. If it has a different
   name, rename it to `content`.
   - **Note**: Although you can change the documentation directory path using the `PD_CONTENT_DIR` variable
   in the `pd` script, it’s recommended to simply rename the directory to `content` as the set value may reset
   with updates.<br/>

3. Setting Permissions
   - **Make the script executable**: By default, the utility is not executable. Open the terminal and navigate to
   the directory where the `pd` file is located.
   ```bash
   chmod +x ./pd
   ```
   
4. First Run of the Utility
   - **Extracting Files**: During the first run of the utility, the bin and plugins directories will be created.
   ```bash
   sudo ./pd
   ```
   Ensure you run the utility from the same directory where the `pd` script is located.

<br/>


## Subsequent Runs

- **Startup Optimization**: On subsequent runs, the utility will not re-extract the `bin` directory, speeding up
the startup process.
- **Plugin Update**: The `plugins` directory will be re-extracted each time the utility runs, allowing for updates to
existing `plugins` and the addition of new ones without reinstalling the entire utility.

## Updating and Adding Plugins

- **Updating the Utility**: Replace the `pd` file and delete the `bin` and `plugins` directories.
- **Updating Plugins**: Place the new plugin version in the `plugins` directory.
- **Adding New Plugins**: Add a new plugin to the `plugins` directory.

## Additional Notes:

- **Access Rights**: Always run the utility with superuser rights (`sudo`) to avoid issues with file and directory access.
