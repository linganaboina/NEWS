# NEWS
Intro about News API :

News API_Project is an application that works based on a REST API. The API defines the proper way for a developer to request services and receive responses from the news data provider, which provides data and various information from the server based on API key credentials.

News API_Project can provide information such as top headlines, articles, and news sources from various categories. REST API responses are commonly used to build news-related websites, mobile apps, and other software applications that need access to up-to-date news data.

This News API at present is working on requesting information about top headlines, articles, and news sources. Using this application, users can quickly and easily access the latest news and stay informed about current events.


Required packages for News API_Project:
       
     1.configparaser
     2.yaml
     3.json
     4.sys
     5.requests
     6.csv
     7.openpyxl
     8.tabulate
     9.datetime
 Configuration Selection:

   - *Request*: In the `select_config()` function, the user is prompted to select the type of configuration (INI file, YAML file, or JSON file) for accessing API keys, URLs, and other settings.
   
   - *Response*: The function returns the user's selected configuration type (`select_val`).

   - *Build*: The selected configuration type is returned to the main script and is used later to load configuration data.

 Output Formatting:

   - *Request*: In the `output_format()` function, the user chooses an output format (console, text file, CSV file, or Excel file) for presenting the retrieved news data. If a file format is chosen, the user provides a file name.

   - *Response*: The function returns the user's chosen output format (`new_choice`) and, if applicable, the file name.

   - *Build: The selected output format and file name are returned to the main script for use in saving or displaying data.

 Query Customization:

   - *Request*: Several functions, such as `q_validation()`, `category_calling()`, `country_calling()`, `articels_calling()`, `lang_val()`, and `sort_validation()`, interact with the user to collect various query parameters like search query, category, country, number of articles, language, and sorting options.

   - *Response*: These functions update the `query_params` dictionary with the user's selections.

   - *Build*: The `query_params` dictionary, which contains the user's customized query parameters, is returned to the main script for constructing the API request.

 API Call:

   - *Request*: The `api_call()` function sends an HTTP GET request to the News API URL with the specified query parameters and API key.

   - *Response*: If the API call is successful (HTTP status code 200, 201, or 204), the function returns the JSON response from the API. Otherwise, it prints an error message.

   - *Build*: The JSON response containing news articles and headlines is returned to the main script.

 Data Presentation:

   - *Request*: The script processes the JSON response data, extracting information such as source names, authors, titles, publication dates, and descriptions.

   - *Response*: Depending on the user's selected output format (`new_choice`), the data is either displayed in the console, saved as a text file, CSV file, or Excel file, or stored in a dictionary (`my_dict`) for later use.

   - *Build*: The processed and formatted data is presented to the user or saved based on the selected output format.

 Multiple Configurations:

   - *Request*: Users have the option to continue making multiple API requests with different parameters.

   - *Response*: The script allows users to decide whether to continue or exit.

   - *Build*: The script continues executing based on the user's choice, or it completes execution and provides the desired output.

These are the main components and operations within the provided script, showing how user requests for configuration and query customization are processed, how API calls are made and their responses are handled, and how data is presented or saved based on user preferences.
