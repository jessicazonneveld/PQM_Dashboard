### MyApiService.cs

Follows the same layout as `app.py`

```c
///Energex
# gets monitor information from energex excel spreadsheet
public async Task<SiteNetworkData> GetTestCardAsync(string site)

# after investigation, there is a way to display images just through front-end
public async Task<List<MonitorData>> GetMDAsync(string site, DateTime? start, DateTime? end)

# gets data from energex PQM graphics dashboard x4 graphs (THD, reactive, active and phase angle)
public async Task<List<GraphicsData>> GetGraphDataAsync(string site, DateTime? start, DateTime? end)

///Ergon
# gets monitor information from ergon excel spreadsheet
public async Task<SiteNetworkData> GetErgonCardAsync(string site)

# gets voltage and current data from piwebapi for ergon
public async Task<List<MonitorData>> GetErgonMDAsync(string site, DateTime? start, DateTime? end)

//Monthly reports option 2:
# Option 2 - brings previously run python script to front-end (currently selected process)
public async Task<HttpResponseMessage> GetExcelFileAsync(string analysisMonth)

//Batch analysis
public async Task<string> GetBacthAnalysisAsync(DateTime? start, DateTime? end)
```