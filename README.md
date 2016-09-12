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
- Download the repository by clicking the "Clone or download" button <img align="center"  src="https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png" alt="Clone or download button"> and selecting the "Download ZIP" tab.
- Extract the files in the ZIP file to your desktop. The contents should be a single folder named "sbi2-master".
- Open the workshop exercise PDF in the viewer of your choice. We won't actually be using it much (due to time contraints) but it may be helpful as a reference or note-taking.

## Getting started

The instructions below describe how to set up CellProfiler for the example pipeline and input images we'll be using. Follow these directions if you want to speed ahead to the (more-interesting) Analysis portion, or if you get lost at the Input portion of the session at the beginning.
- Open CellProfiler. You should see a Welcome Screen (a box with "Welcome to CellProfiler" in the title).
  - If you don't see the Welcome Screen, select *Help > Show Welcome screen* from the main menu.
- From the Welcome Screen, load an example pipeline by clicking the link under the "See an pipeline in action" header.
  - There may be a warning dialog saying the pipeline was saved with an old vesion of CellProfiler. Click "OK" to load the pipeline anyway.
  - A message prompt will appear after loading. Click "OK" to dismiss it.
- Select the **Images** module (top module on left-hand side of CellProfiler)
  - Clear the file list by right-clicking in the File List panel on right-hand side, and selecting "Clear File List" from the context menu that appears. Click "Yes" to confirm the action at the prompt.
  - From your file browser, drag-and-drop the `images` folder (contained in the "sbi2-master" folder) into the File List panel.
- Select the **Metdata** module (second module on left-hand side of CellProfiler). 
  - Select "Yes" to enable it.
  - For the "Metadata extraction method" setting, change `Extact from image file headers` in the drop-down to `Extract from file/folder names`.
  - For the "Regular expression" setting, clear the text in the edit box, and then cut/paste the following regular expression into it:
`^(?P<Plate>.*)_(?P<Well>[A-P][0-9]{2})f(?P<Site>[0-9]*)d(?P<ChannelNumber>[0-9])`
  - Click the "Update" button below the horizontal sash to display the extracted metadata.
- Select the **NamesAndTypes** module
  - For *OrigBlue*, change to `[File] [Does] [Contain] "d0"`
  - For *OrigGreen*, change  `[File] [Does] [Contain] "d1"`
  - For *OrigRed*, change to  `[File] [Does] [Contain] "d2"`
- Click the "Update" button below the horizontal sash to display the matched image channels.
- Click the first **Crop** module.
  - For "Left and right rectangle positions", change to `250` and `end`
  - For "Top and bottom rectangle positions", change to `1` and `250`

You will now be ready to start adjusting the remaining Analysis modules to suit these example images.
