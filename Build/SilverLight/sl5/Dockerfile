ARG frameworkVersion=4.8

# FROM microsoft/dotnet-framework:{frameworkVersion}-sdk AS build
FROM mcr.microsoft.com/dotnet/framework/sdk:4.8 AS build

RUN "New-Item -Type Directory -Name sl-sdk -Path /; Invoke-WebRequest -Uri https://download.microsoft.com/download/3/A/3/3A35179D-5C87-4D0A-91EB-BF5FEDC601A4/sdk/silverlight_sdk.exe -O /sl-sdk/silverlight_sdk.exe; /sl-sdk/silverlight_sdk /quiet /norestart;
RUN "Remove-Item -Recurse /sl-sdk;"


LABEL version='0.1'  maintainer='Hugo Dahl <hugo@code-jedi.com>'
