# IaKee's Installer System (IIS)

IaKee's Installer System (IIS) is a lightweight, user-friendly installation system designed to simplify the process of installing and uninstalling software on Windows systems. With a focus on ease-of-use and flexibility, IIS allows developers to create professional-looking installers quickly and easily, with minimal effort required.

Built using Python and the tkinter framework, IIS offers a customizable, dark-themed user interface that can be tailored to fit any project's branding. The installer system handles all the heavy lifting, automatically creating Windows Registry entries, program shortcuts, and uninstaller entries, while allowing developers to specify custom installation locations, add-on components, and more.

IIS also includes a built-in uninstaller that can be used to remove software installations cleanly and completely, ensuring that no traces are left behind on the system.

With IaKee's Installer System, developers can focus on creating great software, knowing that the installation process is taken care of. Plus, with the open-source MIT license, IIS can be used freely in both commercial and non-commercial projects.

Features:

-Lightweight and easy-to-use
-Customizable, dark-themed user interface
-Handles Windows Registry entries, program shortcuts, and uninstaller entries automatically
-Allows developers to specify custom installation locations, add-on components, and more
-Includes a built-in uninstaller to remove software installations cleanly and completely
-Open-source MIT license

## Example usage:
```python

import IaKeeInstaller as iis

# Create an installer object
installer = iis.Installer("My Application")

# Add files to the installer
installer.add_file("C:/path/to/my/app.exe", "Program Files/My Application/app.exe")

# Add shortcuts to the installer
installer.add_shortcut("Program Files/My Application/app.exe", "Desktop")

# Specify custom installation options
installer.install_dir = "C:/Program Files/My Application"
installer.add_option("Install add-on component", "yesno")

# Build the installer
installer.build("My Application Setup.exe")

# Create an uninstaller object
uninstaller = iis.Uninstaller("My Application")

# Build the uninstaller
uninstaller.build("My Application Uninstaller.exe")
```
