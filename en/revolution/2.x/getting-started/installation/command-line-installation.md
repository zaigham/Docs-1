---
title: "Command Line Installation"
_old_id: "349"
_old_uri: "2.x/getting-started/installation/command-line-installation"
---

<div class="note">CLI Installation is available only for MODX Revolution versions 2.2 and later.</div><div>- [Installing MODX via the PHP Command Line](#CommandLineInstallation-InstallingMODXviathePHPCommandLine)
- [New CLI Installations](#CommandLineInstallation-NewCLIInstallations)
- [Doing a Basic Upgrade MODX via CLI](#CommandLineInstallation-DoingaBasicUpgradeMODXviaCLI)
- [Doing an Advanced Upgrade MODX via CLI](#CommandLineInstallation-DoinganAdvancedUpgradeMODXviaCLI)
- [Using a Helper Script](#CommandLineInstallation-UsingaHelperScript)
- [See Also](#CommandLineInstallation-SeeAlso)

</div>Installing MODX via the PHP Command Line
----------------------------------------

MODX allows you to do upgrades and installations via the command line (CLI) while using a config XML file. (More info on this file can be found [here](/revolution/2.x/getting-started/installation/command-line-installation/the-setup-config-xml-file "The Setup Config Xml File").) This allows users to create simple batch scripts to update their MODX installations.

<div class="warning">When running upgrades, it is **always** recommended to backup your files before upgrading.</div>New CLI Installations
---------------------

First off, [download MODX](http://modx.com/download/) and extract the files to your server. In the setup/ directory, copy the file "config.dist.new.xml" and rename it to "config.xml". MODX will automatically look for the setup/config.xml file during installation. You can move it outside of the setup/ directory (and the MODX webroot, if you choose), and specify its location with the "--config=/path/to/config.xml" argument.

Next, edit the XML file and set the appropriate database information, MODX paths, and other configuration parameters, and then in your command line prompt, browse to the MODX setup/ directory, and type:

```
<pre class="brush: php">
php ./index.php --installmode=new

```MODX will proceed to install, and when finished will display the time it took to run the installation, as well as any errors that occurred (which will also be logged in an install log file in core/cache/logs/).

Note : if your core folder is in a "non-standard" location, you might want to use :

```
<pre class="brush: php">
--core_path=/path/to/core/

```Doing a Basic Upgrade MODX via CLI
----------------------------------

Follow the same steps as new installations, but this time in your XML file you need only specify the following attributes:

- inplace
- unpacked
- language
- remove\_setup\_directory

And any other attributes you would like to change during the upgrade. There is an example upgrade xml file named "config.dist.upgrade.xml". Then, once you are ready, browse to the MODX setup directory, and type:

```
<pre class="brush: php">
php ./index.php --installmode=upgrade

```This will upgrade your MODX installation, and when finished will display the time it took to run the installation, as well as any errors that occurred (which will also be logged in an install log file in core/cache/logs/).

Doing an Advanced Upgrade MODX via CLI
--------------------------------------

Follow the same steps as basic upgrade, but this time in your XML file you need all the attributes included in the config.dist.upgrade-advanced.xml file, as all can be changed in an advanced upgrade.

Then, once you are ready, browse to the MODX setup directory, and type:

```
<pre class="brush: php">
php ./index.php --installmode=upgrade-advanced

```This will upgrade your MODX installation, and when finished will display the time it took to run the installation, as well as any errors that occurred (which will also be logged in an install log file in core/cache/logs/).

Using a Helper Script
---------------------

There is a helper script **installmodx.php** available on Github: [https://github.com/craftsmancoding/modx\_utils/blob/master/installmodx.php](https://github.com/craftsmancoding/modx_utils/blob/master/installmodx.php)

It provides command line options for this process. Here's a video of it in action:

<object height="300" width="400"><param name="movie" value="http://www.youtube.com/v/-FR10DR16CE&hl=en&fs=1"></param><param name="allowFullScreen" value="true"></param><param name="allowscriptaccess" value="always"></param><embed allowfullscreen="true" allowscriptaccess="always" flashvars="$flashVars" height="300" src="http://www.youtube.com/v/-FR10DR16CE&hl=en&fs=1" type="application/x-shockwave-flash" width="400"></embed></object>See Also
--------

1. [Basic Installation](/revolution/2.x/getting-started/installation/basic-installation)
  1. [MODx Revolution on Debian](/revolution/2.x/getting-started/installation/basic-installation/modx-revolution-on-debian)
  2. [Lighttpd Guide](/revolution/2.x/getting-started/installation/basic-installation/lighttpd-guide)
  3. [Problems with WAMPServer 2.0i](/revolution/2.x/getting-started/installation/basic-installation/problems-with-wampserver-2.0i)
  4. [Installation on a server running ModSecurity](/revolution/2.x/getting-started/installation/basic-installation/installation-on-a-server-running-modsecurity)
  5. [MODX and Suhosin](/revolution/2.x/getting-started/installation/basic-installation/modx-and-suhosin)
  6. [Nginx Server Config](/revolution/2.x/getting-started/installation/basic-installation/nginx-server-config)
2. [Advanced Installation](/revolution/2.x/getting-started/installation/advanced-installation)
3. [Git Installation](/revolution/2.x/getting-started/installation/git-installation)
4. [Command Line Installation](/revolution/2.x/getting-started/installation/command-line-installation)
  1. [The Setup Config Xml File](/revolution/2.x/getting-started/installation/command-line-installation/the-setup-config-xml-file)
5. [Troubleshooting Installation](/revolution/2.x/getting-started/installation/troubleshooting-installation)
6. [Successful Installation, Now What Do I Do?](/revolution/2.x/getting-started/installation/successful-installation,-now-what-do-i-do)
7. [Using MODx Revolution from SVN](/revolution/2.x/getting-started/installation/using-modx-revolution-from-svn)