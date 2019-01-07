# About this Image

## Purpose

This image exists to allow the building of Visual Studio solutions which contain any SilverLight 4 projects.


## Silverlight

This will create a Docker image which will install the SilverLight 4 SDK, in the following order:

1. Create a new image based on [microsoft/dotnet-framework](https://hub.docker.com/r/microsoft/dotnet-framework)
  * Specifically, we are using the image tagged as `microsoft/dotnet-framework:4.7.2-sdk`, which is the current latest available version.
1. Create a temporary working directory in which the SDK installer can be downloaded
1. Download the installer for the SilverLight 4 SDK from Microsoft ([Source](https://www.microsoft.com/en-us/download/details.aspx?id=7335) - [Direct link to installer](https://download.microsoft.com/download/F/2/C/F2CFFB78-03CF-4749-A6AE-EF60FB6FB14E/sdk/silverlight_sdk.exe))
1. Run the installation for the SDK in quiet/unattended mode, and preventing a reboot
1. Clean up the temporary directory into which the installer was downloaded.


