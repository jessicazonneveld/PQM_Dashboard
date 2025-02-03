### app.py file

Walk through of back-end file

The start of the python file contains parts of common functions code when initial trials were taken and kept in use.

```py
@app.get("/")       # test

@app.get("/api/image1") # brings in images through back-end to front-end 
@app.get("/api/image2") # after investigation, there is a way to display images just through front-end
@app.get("/api/image3")


### Energex
@app.get("/excard/{site_id}")   # gets monitor information from energex excel spreadsheet
@app.get("/exsite")             # gets voltage and current data from piwebapi for energex

### Ergon
@app.get("/ergoncard/{site_id}")    # gets monitor information from ergon excel spreadsheet
@app.get("/ergonsite")              # gets voltage and current data from piwebapi for ergon

### MONTHLY REPORTS
# Option 1 - runs the python script in back-end
@app.get("/monthlyreport")
# Option 2 - brings previously run python script to front-end (currently selected process)
@app.get("/monthlyreportrequest")

### BATCH ANALYSIS
# start of back-end of batch analysis request

@app.get("/exsitegraphs")   # gets data from energex PQM graphics dashboard x4 graphs (THD, reactive, active and phase angle)
```