<img src="http://i.imgur.com/WMFG0fo.png">

# SBI2 HCS/HCA Educational Workshop

**Advanced/Elective HCS/HCA Course Topics: Advanced Tools for Data Analysis**

SBI2 High Content 2016, 3rd Annual Conference

Come learn how to do image analysis with **CellProfiler**! CellProfiler is a free open-source software designed to enable biologists without training in computer vision or programming to quantitatively measure phenotypes from thousands of images automatically. 

This advanced course is designed for scientists who wish to get started using CellProfiler to identify objects and measure features on their own images. Familiarity with basic principles of image analysis is assumed. 

**WHEN**

Monday September 12, 2016
11:30 AM - 12:30 PM

**Attending the Image and Data Analysis Introductory Course beforehand (9:00 AM - 10:00 AM, Rm 217) is highly recommended.**

**WHERE**

Joseph B. Martin Conference Center, Harvard Medical School, Boston, MA
Classroom 214

## Pre-workshop instructions

- Sign on to conference guest wireless (SSID: HMS Public). Open browser to wireless greeting page, click "Accept" button at bottom.
- Download and install CellProfiler 2.2.0 from [cellprofiler.org/releases](http://cellprofiler.org/releases/) for your OS
- Download an example set and images as a ZIP file from this [link](http://d1zymp9ayga15t.cloudfront.net/content/Examplezips/ExampleFlyImages.zip)
  - Extract the files in the ZIP file to your desktop. The contents should be a single folder named "ExampleFlyImages".
- Download the repository by clicking the green "Clone or download" button <img align="center" src="https://camo.githubusercontent.com/c6440fe65a8d85b873da9340ffbdbc3a830cee6f/687474703a2f2f7075752e73682f706a73716e2f333166653236616639342e706e67"> at the top of the page and selecting the "Download ZIP" tab.
  - Extract the files in the ZIP file to your desktop. The contents should be a single folder named "sbi2-master".
- Open the workshop exercise PDF in the viewer of your choice. We won't actually be using it much (due to time contraints) but it may be helpful as a reference or note-taking.

## Getting started

The instructions below describe how to set up CellProfiler for the example pipeline and input images we'll be using. Follow these directions if you want to speed ahead to the (more-interesting) Analysis portion, or if you get lost at the Input portion of the session at the beginning.
- Open CellProfiler. 
- Go to the "ExampleFlyImages" folder you extracted from the ZIP file.
  - From your file browser, drag-and-drop the `ExampleFlyURL.cppipe` file into the pipeline panel in CellProfiler (the panel labeled "Analysis modules" on the left-hand-side)
  - A message prompt will appear after loading. Click "OK" to dismiss it.
- Select the **Images** module (top module on left-hand side of CellProfiler)
  - From your file browser, drag-and-drop the `images` folder (contained in the "sbi2-master" folder) into the File List panel.
- Select the **NamesAndTypes** module
  - For *OrigBlue*, change to `[File] [Does] [Contain] "d0"`
  - For *OrigGreen*, change  `[File] [Does] [Contain] "d1"`
  - For *OrigRed*, change to  `[File] [Does] [Contain] "d2"`
  - Click the "Update" button below the horizontal sash to display the matched image channels.
- Click the first **Crop** module.
  - For "Left and right rectangle positions", change to `250` and `end`
  - For "Top and bottom rectangle positions", change to `1` and `250`

You will now be ready to start adjusting the remaining Analysis modules to suit these example images.
