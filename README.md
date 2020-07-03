# Rachio-Node-RED
Node-RED flow using Rachio API for sprinkler dashboard and control

Since the Rachio API has a daily call limit,  this flow builds and uses a config file to store personID, device ID, Zone ID's

The following required Nodes Need to be installed
1) node-red-dashboard
2) node-red-contrib-config
3) node-red-node-ui-table

Process to setup intial config file (Should only have to be done once at install time)
1) Import Flow into Node-RED
2) Set your API key in the Config Node
3) Trigger the Step 1
4) Take the ID value from the Step 1 payload and use that to set the personID in the Config Node
5) Trigger Step 2 to build the config file
6) Triggert Step 3 to check the config file.

Limits
1) Current version assumes only 1 Device (Homes with multiple devices will need to extend logic)
2) Config setup to support 8 or 16 zones.  Current version tested on 8 zone only
3) Zone Control wired to one zone for now.  Need to explore mulitple zone on/off logic before adding other zones.

