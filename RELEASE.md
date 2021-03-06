areaDetector Releases
====================

The latest untagged master branch can be obtained at
https://github.com/areaDetector/areaDetector.

Tagged source code and pre-built binary releases prior to R2-0 are included
in the areaDetector releases available via links at
http://cars.uchicago.edu/software/epics/areaDetector.html.

Tagged source code releases from R2-0 onward can be obtained at 
https://github.com/areaDetector/areaDetector/releases.

Tagged prebuilt binaries from R2-0 onward can be obtained in the detector-specific directories in:
http://cars.uchicago.edu/software/pub/.  For example the Pilatus binaries are in 
http://cars.uchicago.edu/software/pub/ADPilatus.

The versions of EPICS base, asyn, and other synApps modules used for each release can be obtained from 
the EXAMPLE_RELEASE_PATHS.local, EXAMPLE_RELEASE_LIBS.local, and EXAMPLE_RELEASE_PRODS.local
files respectively, in the appropriate release of the 
[top-level areaDetector](https://github.com/areaDetector/areaDetector) repository.


Release Notes
=============

Each submodule contains detailed release notes for each release of that submodule.  The release notes below
only provide a short summary of the most significant items from the submodules.

R2-0
----
* Moved the repository to [Github](https://github.com/areaDetector/areaDetector).
* Re-organized the directory structure to separate the driver libraries from the example IOC applications.
* Added new detector drivers:
    - ADLightField:  Driver for newer Princeton Instruments detectors using their LightField program
    - ADPixirad: Driver for CdTe pixel array detectors from Pixirad
    - ADPointGrey: Driver for Firewire, USB, and GigE cameras from Point Grey
* ADmarCCD driver: Added support for triggered and timed acquisition modes on the new high-speed (-HS) series
  of detectors.
* ADProsilica driver: Added support for conversion from raw Bayer to RGB1, RGB2, and RGB3 in the driver. 
  In areaDetector releases prior to R2-0 this could be done in the NDPluginColorConvert plugin.  
  That capability has been removed from the plugin to make the plugin independent of the AVT PvApi library.
* All submodules now have display files for medm (adl), edm (edl), CSS Boy (opi), and caQtDM (ui).  
  The original files are the medm adl files.  The edm, CSS Boy, and caQtDm files that were created by converting 
  the medm files are found in the autoconvert directories (e.g. pilatusApp/op/opi/autoconvert).
  If there are manually tweaked files they are found in the level above the autoconvert directory 
  (e.g. pilatusApp/op/opi).  Thanks to Tim Mooney for doing all of these conversions.
* Added new NDPluginAttribute plugin from Matt Pearson.

R1-9-1 and earlier
------------------
Release notes are part of the
[areaDetector Release Notes](http://cars.uchicago.edu/software/epics/areaDetectorReleaseNotes.html).

