# Test Front-end and Back-end


### Back-end
To test the back end and make sure the correct data is received in the right format, copy this URL into google to view the documentation:
    ```py
    http://localhost:8000/docs
    ```

### Front-end
The front end uses the URL https://localhost:7124/ when you build website through Blazor.

1. Call the back-end api data through MyApiService.cs to store as variable
2. Call the awaitable just created into respective page you are wanting to place the information


!!! warning
    Error codes to look out for in VS Code terminal when testing the front end
    
    200: this is a successful request
    
    400, 404, 500: anything other than 200 is an invalid request where there may be something wrong between the front-end requesting for information / data from the back-end