# Unistats API Call
This package provides a python interface to the Unistats API.

The unistats-api-call.py file provided has been coded to work with the **Retrieve KIS Data about an Institution** resource but can be modified to work with other requests. Documentation on this request can be found [here](http://data.unistats.ac.uk/api/v4/kis/help/operations/InstitutionByFormat).

The full list of API requests can be found [here](http://dataportal.unistats.ac.uk/Pages/ApiDocumentation).

## About Unistats
Unistats allows users to search for and compare data and information on university and college courses from across the UK. It is owned and operated by the four UK higher education funding bodies:

 - The Department for the Economy in Northern Ireland
 - The Higher Education Funding Council for England
 - The Higher Education Funding Council for Wales
 - The Scottish Funding Council

Website: https://unistats.ac.uk/

Data portal: http://dataportal.unistats.ac.uk/

## Instructions
In the unistats-api-call.py file replace ```YOUR_ACCESS_TOKEN``` with your access token. If you do not have an access token, you can register for one [here](http://dataportal.unistats.ac.uk/). Replace ```YOUR_PASSWORD``` with your password; under current guidance this can be anything.

```
username = "YOUR_ACCESS_TOKEN"
password = "YOUR_PASSWORD"
```

In the same file replace ```YOUR_UKPRN``` with a provider's UKPRN number. UKPRN numbers can be obtained from the [UK Register of Learning Providers](https://www.ukrlp.co.uk/). Replace ```YOUR_FORMAT``` with your response format (either JSON or XML).

```
# Request URL
top_level_url = "https://data.unistats.ac.uk/api/v4/KIS/Institution/YOUR_UKPRN.YOUR_FORMAT"

```

Example: ```https://data.unistats.ac.uk/api/v4/KIS/Institution/10007154.json```
