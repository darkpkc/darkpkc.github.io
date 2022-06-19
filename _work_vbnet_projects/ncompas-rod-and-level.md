---
title: "NCompas Rod and Level"
excerpt: "An internal program to streamline the collection and calculate site survey data."
header:
  teaser: assets/images/work-vbnet-projects/vbnet-project-default-th.jpg
sidebar:
  - title: "Role"
    text: "Developer, Tester"
  - title: "Programming Languages Used"
    text: "VB.NET, HTML, CSS, SQLite, PostgreSQL"
  - title: "Integrated Development Environment (IDE)"
    text: "Visual Studio"
---

NCompas Rod and Level is an internal Windows-based program to streamline the collection and calculate site survey data. Field workers are able to enter rod and level data, review data, calculate error and export data with this program on a Windows tablet in the field. It saves time and labor to digitalize filed notes and data. The program was built with VB.NET with 3-tier architecture.


Rod and Level survey was used in [terrain modelling](http://mcwrightonline.com/geomatics/terrain-modeling/). 

[Levelling rod](https://en.wikipedia.org/wiki/Level_staff) was used in Rod and Level survey.

I actively participated in design, developement, test and maintenance of the program. 

The program had a user-friendly interface with DevExpress which provided beautiful and easy-to-use winform components. Users can easily set up and manage survey releted fields (e.g., surveyor person, benchmark, etc.) before conducting a survey. For data entry, a form was initially built to allow the surveyor to enter one record of survey data at a time. It was ineffieicent , although it was stable. To improve efficiceny and productivity, DataGridView control was added in a form to enable surveyors to add / modify survey data row by row. Several rules were applied to limit user inputs in the DataGridView, so the survey was guaranteed to be conducted in proper order. 

In the field, survey data can be reviewed in two ways - list and graph. ListView control displayed readings and calculated heights. PictureBox control showed a line chart which comprised two axes (distance and height) by drawing points and lines. The algorithm was developed to calculate heights by analyzing plenty of field notes for Rod and Level survey. Total error or difference was calculated to see if it was acceptable for current loop. If not, surveyors were allowed to figure out problems with existing records and make modifications in the field.

Customized reports (e.g., benchmark) were displayed in WebBrowser control using HTML / CSS, and third party libraries were integrated to convert reports to different file formats (e.g., .csv, .xls, .pdf). 

SQLite was used as a local database, and PostgreSQL was used as a database on the server. The PostgreSQL database had tables which were similiar to the ones in SQLite. Data synchronization was implemented by comparing the timestamps.

The program was successful. It had already been used in the field by surveyors to conduct Rod and Level survey. It enabled users to focus on data entry without worrying about transcription of field nots and calculation.  