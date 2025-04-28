# SmartCoopFinal
-------
The APIs available for this application are designed in a RESTful way. To interact with the API,
you must provide the requested information with the correct HTTP method.
The directory that houses the APIs is https://simplecoop.swollenhippo.com/
Endpoints:
coop.php
This endpoint (POST) should be called at the beginning of your project to get a CoopID that is
activated and registered. This is to simulate a customer having a CoopID printed on a label on
the side of their coop. You will use this newly created CoopID for all calls to create a new user.
Method: POST
Required Parameters:
Expected Returns:JSON Object with a key of CoopID
Method: PUT
Required Parameters: SessionID, Street1, Street2, City, State, ZIP
Expected Returns: JSON Object with a key of Outcome
Method: DELETE
Required Parameters: SessionID
Expected Returns: JSON Object with a key of Outcome
Method: GET
Required Parameters: SessionID
Expected Returns: An array of JSON objects with all Coop details
eggs.php
This endpoint can be used to keep a running count of the harvested eggs. For example, you
could have a button on your UI allowing you to enter the eggs harvested for the day. You could
then show an egg counter to the user or even graph the eggs using a library such as chartsjs
Method: POST
Required Parameters: SessionID, observationDateTime, eggs
Expected Returns: A JSON Object with a key of Outcome or LogID
Method: PUT
Required Parameters: SessionID, logID
Expected Returns:
Method: DELETE
Required Parameters: SessionID
Expected Returns: A JSON Object with a key of Outcome
Method: GET
Required Parameters: SessionID, days
Expected Returns: An array of JSON objects with all Egg record details
------------------
