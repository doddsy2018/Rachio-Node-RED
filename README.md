# Rachio-Node-RED
Node-RED flow using Rachio API for sprinkler dashboard and control

Since the Rachio API has a daily call limit,  this flow builds and uses a config file to store personID, device ID, Zone ID's

Process to setup intial config file (Should only have to be done once at install time)
1) Import Flow into Node-RED
2) Set your API key in the Config node
3) Trigger the Step 1
4) Take the ID valuse from the step 1 payload and use that to set the person ID in the Config Node
5) Trigger Step 2 to build the config file
6) Triggert Step 3 to check the config file.

Limits
Setup to work with only 1 Device  (house with multiple devices will need to extend)
Config setup to support 8 or 16 zones.  Current version tested on 8 zone only

