# EF 6.3 MetadataGenerator
By CloudNimble, Inc.

Written by Robert McLaws (https://twitter.com/robertmclaws)

## Background
A year ago, I attempted to port an EF 6.1.3 project from the old-style .csproj file format to the new SDK-style projects. In the process, I discovered that the build task that split the CSDL, SSDL, and MSL components of the EDMX file into separate files and embedded them into the assembly was incompatible. So I wrote a T4 template that replicated the functionality by writing new files to the file system and manipulated the project to make sure the name of the embedded resource matched the old system.

## Using the Generator
1) Copy this file into the EF 6.3 project running in a .NET Core Assembly.
2) Change Line 21 to point to the EDMX file relative to the Generator file.
3) Set the CustomTool for the file to `TextTemplatingFileGenerator`.
4) Profit!

Questions? Problems? Open an issue, I'll be happy to help.
