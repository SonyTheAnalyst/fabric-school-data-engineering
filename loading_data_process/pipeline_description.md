<img width="573" height="229" alt="image" src="https://github.com/user-attachments/assets/35bc9fa9-07f9-4476-8149-4c7ba2148998" />

---

## Get meta data activity
Specifically, it uses the Child items argument combined 
with Advanced Filters to generate a list of only those files that were created or modified between the start 
of the current day ```(@startOfDay(utcNow()))``` and the present moment ```(@utcNow())```. For example, if your folder contains 100 
historical CSV files but a new file named sales_2026_03_20.csv was uploaded this morning, 
this activity will ignore the 100 old files and pass only the single new filename to the subsequent ForEach loop for processing.

---
## The for each actitity 
```@activity('Get Metadata1').output.childItems```


### the noebook activity
processes each file identified by the metadata activity. Its particularity lies in its parameterization: 
it is configured to dynamically accept the filename (today_file) from the ForEach iterator and the current date (processed_Date) as inputs. 
For example, if the pipeline finds a file named data.csv, it passes that name into the notebook's logic so the code knows exactly 
which specific file to move or transform from the "raw" zone to the "landing" zone during that specific loop iteration.
