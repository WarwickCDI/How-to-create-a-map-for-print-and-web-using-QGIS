![](Output\_mydocx.001.png)

**Evaluation Only. Created with Aspose.Words. Copyright 2003-2021 Aspose Pty Ltd.**



![](Output\_mydocx.002.png)

**IDG Technology for Research**

**Client Experience,**

**Information & Digital Group (IDG),**

**University of Warwick**



By Dr. Godwin Yeboah

**How to create a map for print and web using QGIS**

` `**(Workshop Guide Version 1.0)**

Image copyright: qgis.org

![](Output\_mydocx.003.png)![](Output\_mydocx.004.png)![](Output\_mydocx.005.png)![](Output\_mydocx.006.png) 
# Table of Contents
` `**TOC \o "1-3" \h \z \u [1.**	**Learning goals and requirements	 PAGEREF _Toc87974192 \h 2**](#_Toc87974192)**

[Learning outcomes	 PAGEREF _Toc87974193 \h 2](#_Toc87974193)

[Requirements	 PAGEREF _Toc87974194 \h 2](#_Toc87974194)

[**2.**	**How to install QGIS 3.22 (if not already done!)	 PAGEREF _Toc87974195 \h 3**](#_Toc87974195)

[**3.**	**Brief overview of QGIS 3.22	 PAGEREF _Toc87974196 \h 4**](#_Toc87974196)

[**4.**	**Installation of plugins in QGIS 3.22	 PAGEREF _Toc87974197 \h 4**](#_Toc87974197)

[**5.**	**Setup your QGIS project and folder	 PAGEREF _Toc87974198 \h 5**](#_Toc87974198)

[**6.**	**Creating a basic map for print	 PAGEREF _Toc87974199 \h 6**](#_Toc87974199)

[**Step 1: Loading the Afghanistan war diaries data	 PAGEREF _Toc87974200 \h 6**](#_Toc87974200)

[**Step 2: Extract and add country boundary of Afghanistan	 PAGEREF _Toc87974201 \h 9**](#_Toc87974201)

[**Step 3: Add OpenStreetMap as a basemap	 PAGEREF _Toc87974202 \h 12**](#_Toc87974202)

[**Step 4: Prepare you map using layout manager	 PAGEREF _Toc87974203 \h 12**](#_Toc87974203)

[**Step 5: Export map as a pdf	 PAGEREF _Toc87974204 \h 16**](#_Toc87974204)

[**7.**	**Creating a basic map as an interactive web map	 PAGEREF _Toc87974205 \h 16**](#_Toc87974205)

[**8.**	**Examples of hosting the interactive map or embedding in a web page online	 PAGEREF _Toc87974206 \h 17**](#_Toc87974206)




1. # Learning goals and requirements

### Learning outcomes
By the end of this tutorial, participants should be able to

- Know how to use different visual cartographic techniques to effectively present outcomes of data exploration in QGIS
- Understand and use some functions in QGIS and QuickOSM plugin
  - Know how to use QGIS to create a basic map for presentation/publication
  - Learn how to download data from OpenStreetMap and visualise in QGIS
  - Learn how to load data into QGIS and visualise
  - Know how to use a QuickOSM plug in QGIS
- Learn how to export your data using qgis2web plugin and generate an interactive web map and visualise using a browser. 

### Requirements
- Good internet connection throughout the workshop session
- Access to a computer with internet connection
- Properly installed [Quantum GIS software version 3.22](https://www.qgis.org/en/site/forusers/download.html) (See Section 2 below).
- Data sources for this tutorial 
  - Afghanistan War Diaries data
    - [Afghan War Diaries](https://wikileaks.org/afg/), a released document by Wikileaks in 2010, is “an extraordinary compendium of over 91,000 reports covering the war in Afghanistan from 2004 to 2010. The reports, while written by soldiers and intelligence officers, and mainly describing lethal military actions involving the United States military, also include intelligence information, reports of meetings with political figures, and related details.” 
    - The data has been geocoded which is the process in which text (e.g., street addresses) are converted into geographic coordinates (e.g., longitude and latitude).
    - You will download the data here (you may need to login using you University of Warwick account): <https://files.warwick.ac.uk/gyeboah/files/qgis/AfghanWarDiary_EnemiesDetained.csv> 
    - Disclaimer: The Afghan War Diaries data was taken directly from “[Tutorial for Data Literacy: space](https://moodle.warwick.ac.uk/mod/book/view.php?id=1041120&chapterid=116557)” course on Moodle and not from Wikileaks website.
  - OpenStreetMap data
    - [OpenStreetMap](https://www.openstreetmap.org/) (OSM) is a free editable map of world created by people like you. It is free to use under an [open license](https://www.openstreetmap.org/copyright). 
    - As a demonstration of how to extract data from this resource, this tutorial will show how to extract the [country boundary of Afghanistan](https://www.openstreetmap.org/relation/303427#map=6/33.257/67.379) in QGIS.

1. # How to install QGIS 3.22 (if not already done!)

- If you don’t have QGIS already, open your web browser - this may be Firefox, Chrome, Opera, or Internet Explorer.
- Go to the following website: <https://qgis.org/en/site/forusers/download.html> 
  - Windows users: download “[QGIS Standalone Installer Version 3.22](https://qgis.org/downloads/QGIS-OSGeo4W-3.22.0-3.msi)”
  - Mac users: download “[QGIS macOS Installer Version 3.22](https://qgis.org/downloads/macos/qgis-macos-pr.dmg)”
  - If you are using managed desktop, please install via *Software Center* or request via [helpdesk](https://warwick.ac.uk/services/its/servicessupport/helpdesk/).
- The website should look like something below where you have options to choose your operating system (e.g., Windows, Mac OS, Linux, etc.):

![Graphical user interface, application

Description automatically generated](Output\_mydocx.007.png)

- Look for “QGIS Standalone Installer Version 3.22” on [the website](https://www.qgis.org/en/site/forusers/download.html) and download to your computer. 
  - This version was released on 30.10.2021 and is also referred to as ' Białowieża ' with the aim of supporting the celebration of 100-year anniversary of [Białowieża National Park in Poland](https://qgisbialowieza.pl/). 
  - Note where you downloaded the file. For example, if you are using Windows Microsoft Edge to download, you can click on the “Open” button to start the installation or “Save as” button to save the file in a specific folder.

![Graphical user interface, text, application, email

Description automatically generated](Output\_mydocx.008.png)

- If you downloaded the file in a specific folder, locate where the file is downloaded, double click the file, and follow the instructions to install QGIS 3.22.







1. # Brief overview of QGIS 3.22
- Quantum GIS 3.22 is a free and open-source geographical information system. This means it can be used and developed further freely.
- Start GIS 3.22 in Windows or Mac per your installation.

**Coordinate system**

Where your data **layers** will be listed.

You can use this **browser panel** to select your data here.

**Open project icon in toolbar.**

**Toolbars** panel: where icons of tools are listed to be selected.

**Menu bar** (Web is a menu item)

**Unsaved project**

**Canvas** area: where your map will be displayed.
- ![](Output\_mydocx.009.png)The first time you open QGIS 3.22 software, the interface might look like pointing you to some news items and showing an empty list of recent projects. 

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.010.png)
1. # Installation of plugins in QGIS 3.22
- QGIS plugins are additional tools to the core QGIS software which provide additional functionality. First, let us list the proposed plugins to be installed (the list of plugin names to fetch/search):
  - QuickOSM (For extracting data from OpenStreetMap (OSM) database)
  - QGIS2WEB (For generating interactive maps in browsers)
  - QuickMapServices (For loading online basemaps like Google map or OSM.)

- To download and install QGIS 3.22 plugins, go to **Plugins > Manage and Install Plugins…** from the menu bar

![Graphical user interface, text, application, Word, website

Description automatically generated](Output\_mydocx.011.png)

- Search for QuickOSM, select it from the list, and click Install plugin button.

**HINT:** Be mindful of the logo for the plugin. 

You will need it for a quick start of the program in the Toolbars area.

![](Output\_mydocx.012.png)![Graphical user interface, text, application, chat or text message

Description automatically generated](Output\_mydocx.013.png)

- **Note only (Do nothing here)**: You can start QuickOSM from several locations depending on how your operating system configures the installation. Thus, direct from the Toolbar or via ***Vector*** ![Play](Output\_mydocx.014.png)***QuickOSM*** ![Play](Output\_mydocx.014.png)***QuickOSM…***

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.015.png)

- **CHALLENGE 1**: Use your experience from installing QuickOSM plugin to install the following two plugins: **QGIS2WEB** and **QuickMapServices**.
1. # Setup your QGIS project and folder
- **Warning**: Your folder location should be directly at your drive to avoid long path problems. For example, it could be like: **C:\qgis\_tutorial\**
- Save your empty “Untitled” project in a newly created as “**my\_qgis\_project**”. Go to Menu bar  ![Play](Output\_mydocx.014.png)Project  ![Play](Output\_mydocx.014.png)Save  ![Play](Output\_mydocx.014.png)Select folder  ![Play](Output\_mydocx.014.png)Type name of your project file and save


|![Graphical user interface

Description automatically generated](Output\_mydocx.016.png)|![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.017.png)|
| :- | :- |

- Download the Afghanistan War Diaries data using the following link: <https://files.warwick.ac.uk/gyeboah/files/qgis/AfghanWarDiary_EnemiesDetained.csv> 
- Make sure the downloaded file is saved or copied to your “qgis\_tutorial” project folder.
- Let’s make it easier to always go to your project folder inside QGIS by adding the project folder to as favourite. Go to Browser panel  ![Play](Output\_mydocx.014.png)Right click “qgis\_tutorial” folder  ![Play](Output\_mydocx.014.png)Add as a Favourite.

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.018.png)
1. # Creating a basic map for print
Our objective is to create a basic map based on the Afghanistan War Diaries data. You will use *QuickOSM plugin* to extract country boundary of Afghanistan from the OpenStreetMap.org database. You will also use OpenStreetMap as a basemap for your map.

## Step 1: Loading the Afghanistan war diaries data 
1) Open your empty project file created earlier above by double-clicking on the file, if it is closed. There are so many ways of opening existing qgis project. You can open files directly using open folder icon in toolbars area, Project ![Play](Output\_mydocx.014.png) Open…, via Favorites, or double click project file. 

|![Graphical user interface, application

Description automatically generated](Output\_mydocx.019.png)|![Graphical user interface, text, chat or text message

Description automatically generated](Output\_mydocx.020.png)|![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.021.png)|
| :- | :- | :- |

1) Add the diaries data as a delimited text layer. Note that the file itself is in a delimited text format. Go to Menu bar ![Play](Output\_mydocx.014.png)Layer  ![Play](Output\_mydocx.014.png)Add Layer  ![Play](Output\_mydocx.014.png)Add Delimited Text Layer…  ![Play](Output\_mydocx.014.png)Select diaries data file and look for the longitude and latitude files to select.

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.022.png)

![Graphical user interface, text, application, Teams

Description automatically generated](Output\_mydocx.023.png)

1) **WELL DONE!** You have been able to import your diaries data into QGIS!
1) Save you project. Make sure you save your project often to avoid losing any of your work.
1) Save (or export) the layer as **Afghanistan War Diaries from 2004 to 2010** using **.geojson file format**. This step is important because the current layer is still seen by QGIS as delimited text layer and the layer is linked to the raw data which can make it difficult to edit the layer. Go to layer ![Play](Output\_mydocx.014.png)Right-click layer ![Play](Output\_mydocx.014.png)Export ![Play](Output\_mydocx.014.png)Feature As…

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.024.png)

![Graphical user interface

Description automatically generated with medium confidence](Output\_mydocx.025.png)

1) Remove the “AfghanWarDiary\_EnemiesDetained “ layer. Go to layer ![Play](Output\_mydocx.014.png)Right-click layer ![Play](Output\_mydocx.014.png)Remove Layer…![Play](Output\_mydocx.014.png)Ok button

|![Graphical user interface, text, application, chat or text message

Description automatically generated](Output\_mydocx.026.png)|![Graphical user interface, text

Description automatically generated](Output\_mydocx.027.png)|
| :- | :- |
1) Create a symbology for different events which occurred in the diary. 
   1. Go to layer properties. Go to layer ![Play](Output\_mydocx.014.png)Right-click layer ![Play](Output\_mydocx.014.png)Properties. You can also double click layer.

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.028.png)

1. Categorize the different types of events using random colours.

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.029.png)

1. You can reshuffle the random colours.

![Graphical user interface, application

Description automatically generated](Output\_mydocx.030.png)

1. You can also double click each categorized layer and change the colour manually.

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.031.png)

1) **Note**: It is important to always save your project from time to time to avoid losing all the work you have done so far!

## Step 2: Extract and add country boundary of Afghanistan
1) First, let’s explore the tags given to Afghanistan country boundary in OpenStreetMap database. Open your internet browser [I am using Microsoft Edge browser] ![Play](Output\_mydocx.014.png)Type OpenStreetMap.org ![Play](Output\_mydocx.014.png)Search Afghanistan ![Play](Output\_mydocx.014.png)Click “Country Afghanistan” in the results. 

|![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.032.png)|![Map

Description automatically generated](Output\_mydocx.033.png)|
| :- | :- |

**IMPORTANT**. Observe the “**alt\_name:af | Afganistan**"; we will use the tag in next step. In QGIS, this will be used as “**Key | Value**" in QuickOSM dialog. If you are finding problem understanding this, you can go to the final OpenStreetMap page [here](https://www.openstreetmap.org/relation/303427#map=5/33.651/68.335).

1) Start QuickOSM plugin. You will need to accept copyrights.

|![Graphical user interface, text, application, Word, email

Description automatically generated](Output\_mydocx.034.png)|![Graphical user interface, text, website

Description automatically generated](Output\_mydocx.035.png)|
| :- | :- |
||<p></p><p>![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.036.png)</p>|
1) Enter the parameters below, including the tags in the Step 2 (a) above, and run query to extract the country boundary. Thus, **Key** column is “**alt\_name:af”**, **Value** column is “**Afganistan**”, and make sure “**Canvas Extent**” is selected in Step 4 below.

![Graphical user interface, application

Description automatically generated](Output\_mydocx.037.png)

1) Save “**alt\_name:af\_Afganistan [![](Output\_mydocx.038.png)]**” layer as “**Afghanistan boundary”** in .geojson file format. 

![Graphical user interface, application

Description automatically generated](Output\_mydocx.039.png)

![Graphical user interface

Description automatically generated with medium confidence](Output\_mydocx.040.png)

1) Remove all layers with names “**alt\_name:af\_Afganistan”**. We no longer need them and we don’t have to save them. Highlight the three layers (i.e., polygons, lines, and point layers) ![Play](Output\_mydocx.014.png)Right-click the highlighted area ![Play](Output\_mydocx.014.png)Remove Layer…

|![Graphical user interface, text, application, chat or text message

Description automatically generated](Output\_mydocx.041.png)|![Graphical user interface, text

Description automatically generated](Output\_mydocx.042.png)|
| :- | :- |

1) Go to the layer properties of “**Afghanistan boundary”** layer.![A picture containing graphical user interface

Description automatically generated](Output\_mydocx.043.png)

1) Change symbology so that you can see only black outline of the boundary. 

![Graphical user interface, text, application

Description automatically generated](Output\_mydocx.044.png)

1) Save your project file by going to Project ![Play](Output\_mydocx.014.png)Save.
1) Move “Afghanistan War Diaries from 2004 to 2010” layer to the first on the list of layers. Click and hold the layer using the mouse and move the top of the layers. 

![A picture containing diagram

Description automatically generated](Output\_mydocx.045.png)

Layers should finally look like the following below.

![A picture containing chart

Description automatically generated](Output\_mydocx.046.png)

1) If not already the case, try and zoom the extent of the boundary so that you can see the full spatial extent of Afghanistan country boundary.

![Graphical user interface, text, chat or text message

Description automatically generated](Output\_mydocx.047.png)

1) **WELL DONE**! You have added the boundary layer/data to your project! Save project.

## Step 3: Add OpenStreetMap as a basemap
**This document was truncated here because it was created in the Evaluation Mode.**
**Created with an evaluation copy of Aspose.Words. To discover the full versions of our APIs please visit: https://products.aspose.com/words/**

` `PAGE   \\* MERGEFORMAT 12

