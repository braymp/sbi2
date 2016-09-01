<img src="http://i.imgur.com/WMFG0fo.png">

# SBI2 HCS/HCA Educational Workshop

**Advanced/Elective HCS/HCA Course Topics: Advanced Tools for Data Analysis**

SBI2 High Content 2016, 3rd Annual Conference

Come learn how to do image analysis with **CellProfiler**! CellProfiler is a free open-source software designed to enable biologists without training in computer vision or programming to quantitatively measure phenotypes from thousands of images automatically. 

This advanced course is designed for scientists who wish to get started using CellProfiler to identify objects and measure features on their own images. Familiarity with basic principles of image analysis is assumed. Attending the Image and Data Analysis Introdutory Course is recommended.

**WHEN**

Monday September 12, 2016
9:00 AM - 12:00 PM

**WHERE**

Joseph B. Martin Conference Center, Harvard Medical School, Boston, MA
Classrooms 214, 216, & 217

## Pre-workshop instructions

- Download and install CellProfiler 2.2.0 from [cellprofiler.org/releases](http://cellprofiler.org/releases/) for your OS
- Download the repository by clicking the "Clone or download" button <img align="center"  src="https://help.github.com/assets/images/help/repository/clone-repo-clone-url-button.png" alt="Clone or download button"> and selecting the "Download ZIP" tab.
- Extract the files in the ZIP file to your desktop.

## Getting started

The instructions below describe how to set up CellProfiler for the example pipeline and input images we'll be using. Follow these directions if you want to speed ahead to the (more-interesting) Analysis portion, or if you get lost at the Input portion of the session at the beginning.
- Open CellProfiler
- If you don't see the Welcome Screen, go to *Help > Show Welcome screen*
- Load an example pipeline by clicking the link under "See an pipeline in action".
- Select the **Images** module (top module on left)
  - Clear the file list by right-clicking in panel on right-hand side, and selecting "Clear File List" from the context menu that appears.
  - From your file browser, drag-and-drop the `images` folder extracted from the ZIp file into the file list panel.
  - Click the "apply filters to the file list" button.
- Select the **Metdata** module (second module on left). Select "Yes" to enable it.
    - For the "Metadata extraction method" setting, select "Extract from file/folder names"
    - For the "Regular expression" setting, click the magnifying glass on the right. Clear the "Regex" box and cut/paste the following regular expression into it, then click "Submit":
`^(?P<Plate>.*)_(?P<Well>[A-P][0-9]{2})f(?P<Site>[0-9]*)d(?P<ChannelNumber>[0-9])`
- Select the **NamesAndTypes** module
    - For *OrigBlue*, change to `[Metadata] [Does] [Have ChannelNumber matching] "1"`
    - For *OrigGreen*, change  `[Metadata] [Does] [Have ChannelNumber matching] "2"`
    - For *OrigRed*, change to  `[Metadata] [Does] [Have ChannelNumber matching] "3"`
    - For the `Image set matching method` (bottom-most setting), change from `Order` to `Metadata`
    - For the `Match metadata" setting:
      - Select `Plate` for each of the three drop-downs. Click the `+` button to the right.
      - Select `Well` for each of the three drop-downs. Click the `+` button to the right.
      - Select `Site` for each of the three drop-downs.

You will now be ready to start adjusting the Analysis modules to suit these example images.
