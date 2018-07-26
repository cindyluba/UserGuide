+-----------------------------------------------------------------------+
| Welcome                                                               |
+=======================================================================+
| to                                                                    |
|                                                                       |
| RaptorX 2.7.1                                                         |
+-----------------------------------------------------------------------+
|                                                                       |
+-----------------------------------------------------------------------+
| Introducing the Raptor Suite                                          |
|                                                                       |
| The Raptor Suite is a collection of US Government owned, license-free |
| mapping and situational awareness software tools. With applications   |
| on Android, Cloud, PC, Mac, and server environments, the Raptor Suite |
| provides a highly flexible deployment capability to meet almost any   |
| use case, in any environment, from highly connected analytic          |
| operations centers down to tactical users in disadvantaged or covert  |
| environments.                                                         |
|                                                                       |
| As one of the original applications in the Raptor Suite, RaptorX is   |
| installed and run locally on computer systems online or offline.      |
| RaptorX features a 3D globe provided by NASA, complete with elevation |
| data, satellite imagery, and accurate geographic projection so that   |
| items added to the map are accurately overlaid on imagery and         |
| referenced precisely with the map's geo-coordinate system.            |
|                                                                       |
| RaptorX also allows for tying into live data streams such as video    |
| feeds, intelligence overlays, alerts and alarms, and more. RaptorX    |
| also allows for establishing connections to physical devices for      |
| manually controlling sensors and payloads. This can range from simple |
| manipulation of emplaced sensor configuration to actually flying      |
| UAS's through Raptor interfaces.                                      |
|                                                                       |
| RaptorX, along with the rest of the Raptor Suite, has been created    |
| and maintained by the US Government, and is available at zero cost to |
| the US Government and contractors on Government projects. For more    |
| information, to access latest releases of RaptorX, and to participate |
| in the Raptor Community, visit                                        |
| [www.RaptorX.org](http://www.RaptorX.org).                            |
+-----------------------------------------------------------------------+

Getting Started 4

Glossary of Terms 5

System Requirements 7

Installation 9

Uninstallation 11

RaptorX Quick-look 12

RaptorX Project 13

What Is a RaptorX Project? 13

What Is a RaptorX Package? 14

Ribbon Bar 15

What Is a Ribbon Bar? 15

Quick Access Toolbar 15

Settings & Preferences 16

Project Settings 16

User Preferences 17

Globe Controls 23

Mouse Controls 23

Common Keyboard Controls 24

Onscreen Controls 25

View Ribbon 26

Panels in RaptorX 30

On-Screen Indicators 31

RaptorX Ribbon Bar Details 33

Home Tab Overview 34

Connect Tab Overview 37

Devices Tab Overview 40

Maps Tab Overview 41

Layers 41

Adding Imagery 41

Adding Elevation Models 45

Overlays 45

Tools 52

Attachments Tab Overview 59

Data Tab Overview 61

Import 61

Export 61

Draw Tab Overview 62

2D Shapes 62

3D Shapes 64

Other Draw Tools 69

Apps Tab Overview 71

Help Tab Overview 72

+-----------------------------------------------------------------------+
| Getting Started                                                       |
+=======================================================================+
|                                                                       |
+-----------------------------------------------------------------------+
| Overview                                                              |
|                                                                       |
| This section will discuss three major aspects of getting started with |
| RaptorX:                                                              |
|                                                                       |
| -   Glossary of Terms                                                 |
|                                                                       |
| -   System Requirements                                               |
|                                                                       |
| -   Installation                                                      |
+-----------------------------------------------------------------------+

Glossary of Terms

  Cache                   A Cache in Raptor refers to a collection of stored satellite imagery tiles. These are saved in a directory structure on the Raptor computer.
  ----------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  Device                  A Device is any physical hardware device or simulated device that has been integrated into Raptor through a plug-in. These are represented in Raptor as a Device Icons.
  Globe                   In Raptor, the Globe is the 3D map which satellite imagery, elevation data, and more are added to providing a 3D representation of the earth.
  Glyph                   A Glyph is an icon that is added to track points to indicate something unique about that point or to display track heading.
  Icon                    Icons are simple markers such as pushpins and do not connect to or provide access to any material or simulated device. Icons can be used as containers for devices, files, and other icons.
  Map Object              A Map Object is anything on the map in Raptor, including Icons, Devices, Shapes, and some other drawings.
  MapSet                  A MapSet in Raptor is a map data set comprised of satellite imagery and/or elevation data downloaded for offline use.
  Overlay                 An Overlay is some type of additional information that is placed on top of satellite imagery and the elevation model in Raptor. This can be a series of icons such as with the Placemark Overlay, it can be an image without geo-information such as a JPEG, or it can be shapes and drawings.
  Package                 A Package in Raptor is essentially a "zipped" project. Some files are only referenced by a Project (such as imagery tiles) but are not stored with the Project. When a user creates a Package, they are ensured to have the Project and all of the tangential pieces stored in one file.
  Plugin                  A Plugin in Raptor is a piece of code written outside of the Raptor core application that adds an additional capability to Raptor. Plugins are ".jar" files which are dropped into the plugins directory where Raptor is installed. When Raptor is restarted, it discovers these plugins and exposes the new functionality, connection, feature, or capability to the user.
  Project                 A Project in Raptor is a Raptor session. It is created when a user starts a new session in Raptor, and contains all of the settings, preferences, records, etc. associated with that session. Projects do not contain everything though, that's where Packages come in.
  Web Map Service (WMS)   A Web Map Service (WMS) is a capability that allows for streaming of image tiles over the internet to subscribers. In Raptor, subscribing to a WMS means connecting to an external server and requesting image tiles at various resolution levels that correspond to the location being viewed.

System Requirements

Windows

This section will discuss the system requirements for installing RaptorX
on a Windows operating system.

OS Version

Windows 7 & Windows 10

Minimum Requirements

Admin rights

i3 CPU

4 GB RAM

50 GB disk space

OpenGL capable graphics

Recommended Configuration

i7 CPU

8 GB+ RAM

100 GB+ disk space

NVidia graphics with updated drivers and OpenGL support

Mac

This section will discuss the system requirements for installing RaptorX
on a Mac operating system.

OS Version

MacOS 10.11+

Minimum Requirements

Admin rights

i3 CPU

4 GB RAM

50 GB disk space

OpenGL capable graphics

Recommended Configuration

i7 CPU

8 GB+ RAM

100 GB+ disk space

NVidia graphics with updated drivers and OpenGL support

Linux

This section will discuss the system requirements for installing RaptorX
on a Linux operating system.

OS Version

Ubuntu Linux 16.04 LTS

Minimum Requirements

Admin rights

i3 CPU

4 GB RAM

50 GB disk space

OpenGL capable graphics

Recommended Configuration

i7 CPU

8 GB+ RAM

100 GB+ disk space

NVidia graphics with updated drivers and OpenGL support

Required Ports

  Port(s)       Service/Usage                                       Type      Host
  ------------- --------------------------------------------------- --------- --------------------
  1500          RaptorX Simulator Traffic                           Core      Localhost & Remote
  5000+         Remote Process Manager                              Core      Localhost
  5431          Map Object Importer                                 Plugin    Localhost
  5433          Postgres Database                                   Core      Localhost
  5433+         Multiple instances of Raptor using Postgres         Core      Localhost
  8000          Default NASA WMS port                               WMS       Localhost & Remote
  8081 - 8082   McAfee software (avoid using these ports)           N/A       Localhost
  9001          Hypersonic Database used in integration tests       Core      Localhost
  30300+        Media Analysis (1 port for each Audio/Video cell)   Plug-in   Localhost

Installation

This section will discuss how to install RaptorX on a Windows operating
system.

+-----------------------------------+-----------------------------------+
| 5.  Double-click the installer to | > ![](media/image1.png){width="0. |
|     start the Installation        | 7442836832895888in"               |
|     Wizard. The \_x64 in the name | > height="0.8520089676290463in"}  |
|     of this installer shows that  |                                   |
|     it is the 64bit version.      |                                   |
                                                                       
+===================================+===================================+
| 1.  On the Machine Graphics Power | > ![](media/image2.png){width="2. |
|     panel, choose the option that | 88125in"                          |
|     best matches your machine's   | > height="2.282638888888889in"}   |
|     capabilities.                 |                                   |
+-----------------------------------+-----------------------------------+
| 2.  On the Destination Directory  | > ![](media/image3.png){width="2. |
|     panel, indicate a directory   | 9611111111111112in"               |
|     to install Raptor to. This    | > height="2.3444444444444446in"}  |
|     can be named however you      |                                   |
|     like. If installing multiple  |                                   |
|     versions of Raptor on the     |                                   |
|     same computer, append the     |                                   |
|     version number to the RaptorX |                                   |
|     directory to create that      |                                   |
|     separate directory for        |                                   |
|     install.                      |                                   |
+-----------------------------------+-----------------------------------+
| 3.  On the Project Data Directory | ![C:\\Users\\BoylesCG\\Desktop\\I |
|     panel, choose where you want  | ronKey                            |
|     RaptorX project information,  | Backup\\User Manual\\RX 1.14 SP1  |
|     map files, and other data     | User Manual\_KM\\1.14 SP1         |
|     stored. This directory will   | Screenshots\\Setup4.png](media/im |
|     grow throughout the life of   | age4.png){width="2.93819444444444 |
|     your Raptor install, as       | 46in"                             |
|     imagery is cached here,       | height="2.292361111111111in"}     |
|     projects are stored here,     |                                   |
|     etc. If you are installing    |                                   |
|     multiple versions of Raptor   |                                   |
|     on the same machine as        |                                   |
|     indicated above, give this    |                                   |
|     directory the same name as    |                                   |
|     you gave the install          |                                   |
|     directory in step 3. This     |                                   |
|     will ensure clean separation  |                                   |
|     between data belonging to     |                                   |
|     each installed version.       |                                   |
+-----------------------------------+-----------------------------------+
| 4.  Continue through the steps in | ![](media/image5.png){width="2.89 |
|     the Installation Wizard.      | 67804024496937in"                 |
|     Raptor will be installed in   | height="2.1438035870516186in"}    |
|     the directory indicated in    |                                   |
|     step 3. If you specified,     |                                   |
|     there will also be a desktop  |                                   |
|     and start menu icon that can  |                                   |
|     be used to start Raptor.      |                                   |
+-----------------------------------+-----------------------------------+

Uninstallation

This section will discuss how to remove RaptorX from a Windows operating
system.

+-----------------------------------+-----------------------------------+
| 5.  Double-click the              | > ![../../../../Uninstall.png](me |
|     "uninstall.exe" in the        | dia/image6.png){width="1.85290354 |
|     directory where Raptor is     | 33070866in"                       |
|     installed. In this case it is | > height="2.1438035870516186in"}  |
|     C:\\Program Files\\RaptorX    |                                   |
                                                                       
+===================================+===================================+
| 1.  Delete Project Data folders   | > ![../../../../Screen%20Shot%202 |
|     to ensure projects, data, and | 017-01-24%20at%2011.34.02%20AM.pn |
|     stored imagery are removed.   | g](media/image7.png){width="1.710 |
|     The Program Data folder is    | 0962379702538in"                  |
|     hidden by default, so be sure | > height="1.124446631671041in"}   |
|     to show hidden files or       |                                   |
|     folders to make that folder   |                                   |
|     visible                       |                                   |
+-----------------------------------+-----------------------------------+
| 2.  Raptor Projects and Project   | > ![../../../../remove.png](media |
|     Data is stored here:          | /image8.png){width="1.99321631671 |
|     C:\\ProgramData\\RaptorX      | 0411in"                           |
|                                   | > height="1.8298687664041995in"}  |
+-----------------------------------+-----------------------------------+
| 3.  Default imagery caches and    |                                   |
|     settings are stored here:     |                                   |
|     C:\\ProgramData\\WorldWindDat |                                   |
| a                                 |                                   |
+-----------------------------------+-----------------------------------+
| 4.  Manually converted or stored  |                                   |
|     imagery is located here:      |                                   |
|     C:\\ProgramData\\WorldWindIns |                                   |
| talled                            |                                   |
+-----------------------------------+-----------------------------------+

+-----------------------------------------------------------------------+
| RaptorX Quick-look                                                    |
+=======================================================================+
|                                                                       |
+-----------------------------------------------------------------------+
| Overview                                                              |
|                                                                       |
| This section will discuss a high level overview of the RaptorX        |
| application:                                                          |
|                                                                       |
| -   RaptorX Project                                                   |
|                                                                       |
| -   Ribbon Bar                                                        |
|                                                                       |
| -   Settings & Preferences                                            |
|                                                                       |
| -   Globe Controls                                                    |
|                                                                       |
| -   Primary, Left, Right, & Bottom Panels                             |
|                                                                       |
| -   On Screen Indicators                                              |
+-----------------------------------------------------------------------+

RaptorX Project

This section will discuss the named collection of files, settings, and
data called a Raptor Project.

What Is a RaptorX Project?

A Raptor Project is started the first time a user starts up Raptor, and
it represents all of the changes, additions, configurations, and
settings that have been made during that Raptor session. In subsequent
Raptor sessions, the user must decide to open and continue working in an
existing Project, or to create a new Project and start from a blank
slate.

Raptor Projects are identified by folders which mirror the Project's
name, and are stored on your computer here:

C:\\ProgramData\\RaptorX\\ProjectData\\Projects

![](media/image9.png){width="4.846527777777778in"
height="2.7818077427821524in"}

When Raptor starts up, you will be asked to create a New Project, or
Open and continue to use an existing Project.

What Is a RaptorX Package?

Although the above directory represents the storage location for most
Project data, it does not include all the data that you might have in
your Project. If you want to collect every aspect of your Project to
give to another Raptor user, or to move to another computer to use in
Raptor, you must create a Raptor Package.

Create a Raptor Package by clicking in the Application Menu (upper right
corner) and choosing "Package".

![../../../../Package.png](media/image10.png){width="1.9815551181102362in"
height="3.2888888888888888in"}

If you want to include cached imagery in your package, be sure to select
Package Imagery in the Package dialog. This will make the resulting
Package much larger, and might not be necessary if there is imagery on
the computer you are opening this Package on, but it is an option if you
want to keep satellite imagery with the Project data.

Ribbon Bar

This section will discuss the main user interface element of RaptorX,
the Ribbon Bar.

What Is a Ribbon Bar?

RaptorX uses a common arrangement of tabs and buttons across the top of
the application, providing access to almost every feature and capability
of Raptor. This is called a Ribbon Bar.

![../../../../Ribbon.png](media/image11.png){width="6.5in"
height="1.0895833333333333in"}

At the top left of the RaptorX screen is a round "globe" icon that is
called the Application Menu. This holds several features common to most
application "File" menus -- Open, Save, Preferences, Settings, and more.

Quick Access Toolbar

Beside the Application Menu is a series of smaller icons called the
Quick Access Toolbar.

![../../../../QuickAccess.png](media/image12.png){width="2.6417202537182853in"
height="1.3748818897637796in"}

Both the Ribbon Bar and the Quick Access Toolbar are configurable to
hold the icons that you choose.

Settings & Preferences

This section will discuss adjusting Project Settings and User
Preferences, where many adjustments and customizations can be made.

Project Settings

+-----------------------------------+-----------------------------------+
| In the Application Menu, there is | ![../../../../Settings.png](media |
| a menu item called Project        | /image13.png){width="1.1585892388 |
| Settings.                         | 451444in"                         |
|                                   | height="3.0105850831146106in"}    |
| These settings apply to the       |                                   |
| Project you are currently working |                                   |
| in, and will not be carried over  |                                   |
| into other Projects.              |                                   |
+===================================+===================================+
| The Info tab in Project Settings  | ![../../../../Settings1.png](medi |
| holds descriptive information     | a/image14.png){width="2.281323272 |
| such as Title and User associated | 090989in"                         |
| with this Raptor Project. This    | height="3.342208005249344in"}     |
| can be entered by the user for    |                                   |
| reference purposes.               |                                   |
|                                   |                                   |
| Note that once a Project is       |                                   |
| created, the Project ID cannot be |                                   |
| changed.                          |                                   |
|                                   |                                   |
| This information is referenced on |                                   |
| the Raptor welcome screen when    |                                   |
| existing Projects are selected.   |                                   |
+-----------------------------------+-----------------------------------+
| The Display tab in Project        | ![](media/image15.png){width="2.9 |
| Settings allows a user to         | 07930883639545in"                 |
| indicate Project Labels. Project  | height="1.6952351268591426in"}    |
| Labels appear on the main screen  |                                   |
| in Raptor and can be used to      |                                   |
| indicate classification levels,   |                                   |
| Project or mission identifiers,   |                                   |
| and more.                         |                                   |
+-----------------------------------+-----------------------------------+
