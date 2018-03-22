import urllib.request
import json

# Request URL
top_level_url = "https://data.unistats.ac.uk/api/v4/KIS/Institution/YOUR_UKPRN.YOUR_FORMAT"

def auth():

    # Access token and password
    username = "YOUR_ACCESS_TOKEN" #YOUR_ACCESS_TOKEN
    password = "YOUR_PASSWORD"
    
    password_mgr = urllib.request.HTTPPasswordMgrWithDefaultRealm()

    # Add the username and password
    password_mgr.add_password(None, top_level_url, username, password)

    handler = urllib.request.HTTPBasicAuthHandler(password_mgr)

    # Create "opener" (OpenerDirector instance)
    opener = urllib.request.build_opener(handler)

    # Use the opener to fetch a URL
    opener.open(top_level_url)

    # Install the opener
    urllib.request.install_opener(opener)

def results(data):

    # Use the json module to load the string data into a dictionary
    theJSON = json.loads(data)

    # Iterate through the resultset and display
    for i in theJSON:
        print(i + ":", theJSON[i])

def main():

    # Call authentication method
    auth()

    # Request URL
    url = urllib.request.urlopen(top_level_url)

    # If the request succeeds read data and output
    if(url.getcode() == 200):
        data = url.read()

        results(data)

    # Else return an error
    else:
        print ("Server error: " + str(url.getcode()))

if __name__ == "__main__":
    main()
