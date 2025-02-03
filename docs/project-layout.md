# Project Layout

Here outlines the IMPORTANT contents within folders NpWeb and NpFast (all other documents are needed however never edited)

### NpFast
    .venv/                      # virtual environment
    
    Batch Analysis Input/       # holds batch analysis input files for testing

    images

    Important Dashboard Files/  # holds excel files for Energex, Ergon and EOLV containing monitor information

    Monthly Reports/            # location for the monthly reports previously run

    app.py                      # location to run back-end when testing
    BatchAnalysis.py
    Common_Functions.py
    Constant.py
    EnergexDashbaordScript.py
    MonthlyReportScript.py
    test.py                     # test file to make sure app.py will perform the right tasks


### NpWeb

    Layout/
        MainLayout.razor        # provides simple outline layer
        NavMenu.razor           # primary navigation menu

    Pages/
        Assess.razor            # future development for assess neutral integrity
        Chart.razor             # test page for plotting charts
        Check.razor             # future development for check data availability
        Counter.razor           # test page when web application was set up
        Grid.razor              # main front page 
        Home.razor              # initial set up test page
        Reports.razor           # main page for report developing
        Weather.razor           # test page

    wwwroot/
        css                     # extra design
        js                      # currently holds monthly report download capabilities
        sample-data             # holds any data in the form of .json to test with
        combined_logo.png       # compnay logo
        favicon.png             # supplied icon in web tab (changed to company logo)
        appsettings.json        # directs what server you are working on 

    _Imports.razor              # includes what packages Blazor is using
    App.razor                   # routes the data to a functioning web application
    BlazorApp2.sln              # PQM Dashboard solution in which you open to start editing the web application
    MyApiService.cs             # file that connects to python back end, bringing in python outputs to front end as variables

!!! note
    To view the test pages, build the website on Blazor, then add the page URL to the end of the current domain.

    Example:
    
    If you are wanting to view edits in Weather.razor, confirm the @page name is "/weather" and add to the end of the URL. The following changes should be made.

    Original domain: https://localhost:7124/

    New domain: https://localhost:7124/weather

!!! danger 
    For appsettings.json:

    When sending off for deployment (Max), have this only this line uncommented: "https://sbnswts45.services.local:8005/"
    
    When editing on local host, have this only this line uncommented: "http://localhost:8000"