# stackin
2019-05-08

stackin is a new repository meant to be loaded as a submodule into MATLAB for use with cardiac electrophysiology analysis
tools such as Camat, RHYTHM, and ElectroMap. stackin has functions that can be used to load in image stacks (videos) while respecting the frame rate (fps) or period (dt) of the video.

Dependencies for Nikon .ND2, Zeiss .LSM, and other Bio-Formats loading:  
Bio-Formats Matlab from Open Microscopy Environment (OME)
https://github.com/ome/bio-formats-matlab/tree/master/src  
Java package download from this page: 
https://www.openmicroscopy.org/bio-formats/downloads/    
Reference here on how to add .jar to your static java path: 
https://www.mathworks.com/help/matlab/matlab_external/static-path.html

Dependencies for Andor .SIF and .SIFX loading:  
Proprietary .SO or .DLL blobs from Andor and binds in C to create mex.

- Open .TIF/.TIFF files, especially those taken with MetaMorph 7.5 TIFF format
- Open BigTIFF files, specifically those taken with PCO Camware raw files (.pcoraw)
  * You must save and open the comment file and manually enter the FPS information
- Open Andor .SIF and .SIFX files, using some proprietary blobs
- Open Nikon .ND2 or Zeiss .LSM using Bio-formats-matlab*
  * You must also load in bfmatlab repository as another submodule and download bioformats_package.jar from OME.
