
## azure container
---
<img width="1612" height="291" alt="image" src="https://github.com/user-attachments/assets/00905e7b-43ce-4de1-bc9d-72d7bad44181" />

---
<img width="573" height="229" alt="image" src="https://github.com/user-attachments/assets/35bc9fa9-07f9-4476-8149-4c7ba2148998" />

---

## Get meta data activity
Specifically, it uses the Child items argument combined 
with Advanced Filters to generate a list of only those files that were created or modified between the start 
of the current day ```(@startOfDay(utcNow()))``` and the present moment ```(@utcNow())```. For example, if your folder contains 100 
historical CSV files but a new file named sales_2026_03_20.csv was uploaded this morning, 
this activity will ignore the 100 old files and pass only the single new filename to the subsequent ForEach loop for processing.

---
<img width="1123" height="415" alt="image" src="https://github.com/user-attachments/assets/4cf8520e-9261-45fa-a63e-ce7e3c812422" />

---
## The for each actitity 
```@activity('Get Metadata1').output.childItems```


### the noebook activity [notebook]<https://github.com/SonyTheAnalyst/fabric-school-data-engineering/blob/cfceeac3c230720042b5ad2b0575d18041093e97/loading_data_process/row_to_landing.ipynb>
processes each file identified by the metadata activity. Its particularity lies in its parameterization: 
it is configured to dynamically accept the filename (today_file) from the ForEach iterator and the current date (processed_Date) as inputs. 
For example, if the pipeline finds a file named data.csv, it passes that name into the notebook's logic so the code knows exactly 
which specific file to move or transform from the "raw" zone to the "landing" zone during that specific loop iteration.

--- 
<img width="819" height="382" alt="image" src="https://github.com/user-attachments/assets/cd4f5d1a-58dc-4adf-b9dd-39e490883845" /> 
