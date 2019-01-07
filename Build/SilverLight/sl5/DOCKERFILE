# ARG frameworkVersion=4.7.2

# FROM microsoft/dotnet-framework:{frameworkVersion}-sdk AS build
FROM microsoft/dotnet-framework:4.7.2-sdk AS build

RUN "New-Item -Type Directory -Name sl-sdk -Path /; Invoke-WebRequest -Uri https://download.microsoft.com/download/3/A/3/3A35179D-5C87-4D0A-91EB-BF5FEDC601A4/sdk/silverlight_sdk.exe -O /sl-sdk/silverlight_sdk.exe; /sl-sdk/silverlight_sdk /quiet /norestart;
RUN "Remove-Item -Recurse /sl-sdk;"


LABEL version='0.1'  maintainer='Hugo Dahl <hugo@code-jedi.com>'
