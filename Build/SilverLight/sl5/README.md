# About this Image

## Purpose

This image exists to allow the building of Visual Studio solutions which contain any SilverLight 5 projects.


## Silverlight

This will create a Docker image which will install the SilverLight 5 SDK, in the following order:

1. Create a new image based on [microsoft/dotnet-framework](https://hub.docker.com/r/microsoft/dotnet-framework)
  * Specifically, we are using the image tagged as `microsoft/dotnet-framework:4.7.2-sdk`, which is the current latest available version.
1. Create a temporary working directory in which the SDK installer can be downloaded
1. Download the installer for the SilverLight 5 SDK from Microsoft ([Source](https://www.microsoft.com/en-US/download/details.aspx?id=28359) - [Direct link to installer](https://download.microsoft.com/download/3/A/3/3A35179D-5C87-4D0A-91EB-BF5FEDC601A4/sdk/silverlight_sdk.exe))
1. Run the installation for the SDK in quiet/unattended mode, and preventing a reboot
1. Clean up the temporary directory into which the installer was downloaded.


