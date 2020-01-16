Process Digitalization/Automation for VF Group Shared Services 
---
[Here](https://billigence.sharepoint.com/:f:/s/BilligenceEurope830/EpTTac9yiVlHs9o74uVTuzkBFik9iawaiNsyey-O6atseA?e=9nEITW) you can find main documentation about this project.
### R2R use case
In this project, the task was to automate existing report using the Alterix Designer.
We faced several tasks:
* Create connection to the data sourses (primary *.xlsx files).
* Do all data transformations via Alteryx.
* Extract embedded files from email (*.msg files).
* Create design the output in exatly the same format as the original process.
#### Alteryx Part
Use case workflow you can download here: [R2R_Usecase.yxmd](https://billigence.sharepoint.com/:u:/s/BilligenceEurope830/EfDluhXczhdHg5dWaBKHjaUBQ-W9TncKTZkHrZxxXG0Z7g?e=HkdTEE)
>
The workflow consist of 4 blocks with comments for each block (you can find diagram here: [Worflow_diagram.png](https://billigence.sharepoint.com/:i:/s/BilligenceEurope830/EemZsyQTOElAk-GJi0c5WUYBLKDGsh-GVhGw5HnaFdn8Mw?e=0MCqem>), 
each block receives data, performs set of functions and sends data for further analysis.
1. First block (yellow) connects  to data sources (excel files) and download data to Alteryx workflow. 
2. Second block (blue) is a block for pre-processing and filtering data sets (changing the data type,choosing the right values, renaming). 
3. Third block (green) contains all reports calculations and aggregations. 
4. Fourth block (orange) designs the output in exactly the same format as the original process and downloads it to report file. 
>
#### Python Part
To extract data from email was used python script: [msg_reader.pyw](https://billigence.sharepoint.com/:u:/s/BilligenceEurope830/ETBXjdfR36xGqO_F3mh4gJABC86OR-QycXymnEjAbdzlWA?e=SIjLV7).
This script extract all embeddet files from email file [*.msg](https://billigence.sharepoint.com/:u:/s/BilligenceEurope830/EY0vgFncwu5Drb79PHVkzMYBvzAs94GzLhA18t-Y5WPjjA?e=qPnBuP) to the working directory. 
To move the extracted files to other directory we created [copy_files.pyw](https://billigence.sharepoint.com/:u:/s/BilligenceEurope830/EUA9907nBlZIoPFoj2FSZTEBqZCJVH5y12Xq-JySdzbWCg?e=4ZcHli) script. 
>
[Here](https://billigence.sharepoint.com/:i:/s/BilligenceEurope830/ER7h-2r3AhxNnxsPi5gAXSoBSlbgOL12FdluJlHQB_qW9A?e=UpHdbZ) you can see how to configure running python scripts in Alteryx Designer before/after running the workflow.

### Tax use case
