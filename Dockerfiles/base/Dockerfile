# escape=`
# app image
FROM microsoft/dotnet-framework:4.6.2-windowsservercore-10.0.14393.1884

RUN mkdir "c:\apps\meissa"
ADD "./meissa_bld/" "/apps/meissa"

EXPOSE 5000

WORKDIR "/apps/meissa"
