# Writing-API-Endpoints

-What does this application do?

You can provide information about your location and the food you want to eat and this application will return the relevant restaurant nearest to your location. You can interact with this application by sending HTTP (GET, POST, PUT, DELETE) requests.

-How does this application work?

This flask application leverages Google Maps geocoding API and Four square place API. When you make a post request with your location and the food type, it will use the geocoding API to generate the latitude and longitude for your location. This coordinates information will be sent as parameters while calling the Four square API that will in return fetch the restaurant name with an address. The result will be saved in the database and also returned to you as a json object.

-What are the requirements/changes to be made for running this app?

Since this application uses Google's geocoding API and Four Square's places API, you will need to create a developers account for the both the cases and generate the API Key (for geocoding API) and client_key and client_secret (for places API). Once you have these keys, populate them in their respective placeholders in findRestaurants.py
