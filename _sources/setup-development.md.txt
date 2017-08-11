# Setting up an OSATE development environment 

Starting with OSATE 2.3, which is based on Eclipse 4.7 (Oxygen), the recommended way to set up a development environment uses the Eclipse Installer.

## 1. Download the installer

The Eclipse Installer can be downloaded from the eclipse Web site. Follow this [link](https://www.eclipse.org/downloads/) to download the installer for your platform. Make sure that the word size of the installer version matches the word size of your Java installation. For example, if you are running 32bit Java on a 64bit Windows you must use the 32bit installer.

On Mac OSX and Linux the installer is a compressed archive. extract it to a directory of your choice.

The installer for Windows is a self-extracting archive. When running the executable you can choose to keep the extracted installer and select an installation directory. 

<small>**Note:** On Windows the initial extraction is into a temporary directory, usually into a temporary directory in C:\User\Joe\AppData\Local\Temp\. The name of the temporary directory starts with the letters *eoi* If your computer is subject to a restrictive security policy that does not allow execution of arbitrary programs from that directory you should copy the directory content to another place from where the installer can be executed.</small>

## 2. Run the installer

![Installer 1](images/installer1.png "Installer 1")

Open the menu (A), bundle pools should be on (B), and switch to advanced mode (C)

## 3. Select the Eclipse platform

![Installer 2](images/installer2.png "Installer 2")

On first use update the installer (A)

If necessary, configure proxy settings, and optionally enter ssh credentials (B). User the help (C) for more detailed information on these steps.

Select *Eclipse Modeling Tools* as the base product to install, and select *Oxygen* as the product version. Choose 32 or 64 bit according to your Java version.

## 4. Add the OSATE setup file

![Installer 3](images/installer3.png "Installer 3")

Add a user project by clicking on the *+* icon (A).

Select the catalog *Github Projects* and enter the following URL as the *Resource URI*:

https://raw.githubusercontent.com/osate/osate2-core/develop/osate.releng/osate2.setup

Check the box next to the added OSATE2 Development entry in the tree under Github Projects/<User>.

## 5. Set required variables

![Installer 4](images/installer4.png "Installer 4")

Check *Show all variables* near the bottom of the dialog. Without this only variables that do not have a value will be displayed. Oomph stores variable values between invocations, so nothing would be shown after the first run.

The first group of variables determines the directory for the new eclipse installation. You can choose between (a) a root directory and a subdirectory within that root directory and (b) a full path to the installation directory.

The next group determines the location of the workspace.

The git clone location is the root directory into which all git repositories are cloned. The tycho build requires that all git repositories share the same root directory.

Finally, choose how to access the git repositories. The default choice uses ssh access and requires ssh credentials, and your public key must be uploaded to github. The  *HTTPS (read-write)* option uses your Github username and password. 

## 6. Install Eclipse

The next screen shows the installation steps that will be executed. Click *Finish* to download eclipse and install it to the selected location. When run for the first time, it will download features and plugins into the bundle pool. The bundle pool is shared among eclipse installations such that subsequent installations are much faster.

## 7. Get OSATE sources

Upon first start eclipse executes additional setup tasks to set preferences, clone git repositories if needed, import projects, and organize projects into working sets.

The OSATE2 setup file sets the following preferences:

* The Java perspective is set as the default and eclipse is configured to start with this perspective.
* The default file encoding is set to UTF-8.
* A source cleanup profile *Osate* is created and enabled for the workspace.
* Java formatter profiles *Osate* and *SMACCM*. Profile *Osate* is enabled for the workspace.
* Java code cleanup on save are configured and enabled for the workspace.
* An Xtend formatter profile *Oosate* is created and enabled for the workspace.

Cloning the git repositories takes some time. Progress can be viewed in a dialog. To show the progress dialog, click on the animated icon the eclipse status bar.

## 8. Updating the development environment

Ideally the development environment is completely managed using the setup file. This implies that additional plugins or git repositories should not be added manually. Instead, the setup file should be updated. All developers can then update the eclipse installation by re-executing the setup process. This happens every time eclipse is stared (unless disabled in the preferences) or can be done manually vie *Help* -> *Perform Setup Tasks ...*

Please report issues with the setup using the osate2-core issue tracker on Github.
