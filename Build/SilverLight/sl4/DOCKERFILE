ARG FRAMEWORK_VERSION=4.8

# FROM microsoft/dotnet-framework:{frameworkVersion}-sdk AS build
# FROM microsoft/dotnet-framework:4.7.2-sdk AS build
FROM mcr.microsoft.com/dotnet/framework/sdk:$FRAMEWORK_VERSION AS build
# FROM mcr.microsoft/com/dotnet/framework/sdk:4.8 AS build

# Import the SL4 SDK installer
RUN "New-Item -Type Directory -Name sl-sdk -Path /; Invoke-WebRequest -Uri https://download.microsoft.com/download/F/2/C/F2CFFB78-03CF-4749-A6AE-EF60FB6FB14E/sdk/silverlight_sdk.exe -O /sl-sdk/silverlight_sdk.exe; & /sl-sdk/silverlight_sdk.exe /quiet /norestart;"
RUN "Remove-Item -Recurse /sl-sdk;"

LABEL version='0.1'  maintainer='Hugo Dahl <hugo@code-jedi.com>'
