---
title: "Thermal Risk Analysis Modification"
excerpt: "Discover bugs in running existing Python scripts with ArcMap to perform thermal risk analysis, and fix them."
header:
  teaser: assets/images/work-python-projects/python-project-default-th.jpg
sidebar:
  - title: "Role"
    text: "Developer, Tester"
  - title: "Programming Languages Used"
    text: "Python, ArcGIS"
---

Thermal risk analysis was to conduct a spatial anlysis to generate thermal tolerance risk for various factors (e.g., species, time slices, etc.). It used several tools which were written in Python and run in ArcGIS to achieve the results. 

Issues occurred due to several iterations with these tools. The purpose of this project was to discover bugs in running existing Python scripts with ArcMap and fix them. The biologists in the company were able to do thermal risk analysis with modified Python scripts and write a report.

The most important task that I figured out and worked on was to modify Python scripts to accommodate double digit months and triple digit sigmas in the naming convention.

I went through the tutorial "Get Started with ArcGIS" on Esri website to learn the essential concepts and be familiar with the ArcGIS desktop program. The procedures to run various tools were determined after reading through the technique report of thermal risk analysis. Given large Geospatial datasets, It took times to identify the inputs for each tool in running specific toolboxes with Python scripts in ArcMap.

One way to debug the Python scripts in ArcGIS was to use print methods. Since script tools supported tool messages, scripts can be editted to include calls to AddMessage(), AddWarning(), or AddError() to print values.

Print methods example, 

```
monthAbb = "Jan"
arcpy.AddMessage("The abbreviation of month={}".format(monthAbb)) # Add a custom informative message to the Python script tool 
```

With this debugging technique, issues were found on dealing with naming conventions for given inputs. The infos from given file names were processed incorrectly in existing codes. To fix several bugs, month data and sigma data were formatted with leading zero using zfill() method. Most codes related with data were also modified to meet formatting rules. Brief comments were added and unused codes were removed to make the scripts less clutter and better understanding.

zfill() method example,

```
month.zfill(2) # Pad month with zeros to 2 digits
sigma.zfill(3) # Pad sigma with zeros to 3 digits
```

This small project was really important and successful. Tho biologists from company and DFO were excited to run various tools with modified Python scripts to perform thermal risk analysis. The thermal tolerance risk results were produced properly and were extremely imporant parts of the report.