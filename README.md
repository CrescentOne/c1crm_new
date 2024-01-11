Installation Guide c1crm
==================
---
## Project discription
The c1crm is a node-red solution to syncronise contact and company data from HubSpot to FreshDesk and the Glovia database.

## Installation
In this section we will discuss how we can install and deploy the c1crm.

**Dependencies**
* [Git](https://www.git-scm.com/downloads)
* [NodeJS](https://nodejs.org/en/download)
* [Node-red](https://nodered.org/) (`npm install -g node-red`)

>Make sure to have projects enabled in Node-Red
---
**Cloning the project**
Clone the main branch of the project with `git clone https://YourPersonalAccessToken@github.com/CrescentOne/c1crm.git` 
to `C:\Users\yourUser\.node-red\projects`.

**Opening the project**
Run `node-red` in a cli and open `http://localhost:1880/` in a browser.

Open the project by clicking the hamburger icon in the top right and by selecting `project -> open`.
Now select `HubspotToFreshdesk`

Install the missing dependencies.

## Running the project
Make sure the flow is deployed by checking if the deploy button is gray in thr top right of the screen.

Starting the project can be done on 2 ways.

**Starting from the flow**
In the `Detect changes` flow in the `Start Stop integration` click the blue box on the left of the `Start integration` node. In the debug window you will now see `Starting intergration!`. 

**Starting from CLI** 
To start the flow from CLI you can make a `GET` request to `http://127.0.0.1:1880/startintegration`, you should new get a 200 respose with `Starting intergration!`.

**Stopping the flow**
Stopping the flow is the same as starting the flow but by either clicking the `Stop integration` node or making a `GET` request to `http://127.0.0.1:1880/stopintegration`. You should now get a message with `Stopping intergration! !!Any syncs running will be completed.`