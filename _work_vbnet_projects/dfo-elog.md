---
title: "DFO Electronic Logbook"
excerpt: "A Windows-based program that allows Canadian fishermen to report catch data from remote electronically."
header:
  teaser: assets/images/work-vbnet-projects/vbnet-project-default-th.jpg
sidebar:
  - title: "Role"
    text: "Developer, Tester"
  - title: "Programming Languages Used"
    text: "VB.NET, HTML, CSS, SQLite"
---
DFO Electronic Logbook (ELog) is a Windows-based program that allows fishermen to report catch data from remote location to DFO electronically. Fishers are able to enter data with user-friendly interface while on-board their vessels. Plenty of modules are created for different fishing purposes across Canada. The program was built with VB.NET with 3-tier architecture.

A manual of one ELog module can be found [here](https://www.mcwrightonline.com/index.php/download_file/view/61/165/).

I actively participated in developing and testing the program. 

For some modules, fishing trip managements were divided into different trip activities, and each activity was implmented with ADO.NET for SQLite. Customized reports (e.g., trip activity, fish harvest) were displayed using HTML / CSS, and third party libraries were integrated to convert reports to different file formats (e.g., .xls, .pdf). For functionaly testing, plenty of test cases / test templates were wrote and executed manually to test core functionality, usablity features, accessibility features and specific error conditions. My attention to detail helped to check if the program was error-free and ready before release. 

It enriched my knowledge to use and troubleshoot Globalstar and TextAnywhere that are satellite communication hardwares as options for data transmission in the program. Remote technical support was provided for Canadian fishermen over the phone and over the internet.