# Internet of Things Consumption

Modified SAPUI5 (HTML5) app for the built-in MMS OData API from the SAP Cloud Platform Internet of Things (IoT).

If you want to get more and detailed information read my [SAP blog post](https://blogs.sap.com/2017/09/02/sapui5-app-for-the-built-in-mms-odata-api-from-the-sap-cloud-iot-for-your-weather-station/).

The original SAPUI5 app is part of the Starter Kit for the [SAP Cloud Platform Internet of Things](https://github.com/SAP/iot-starterkit).

## Prerequisites

Setup SAP Cloud Platform Internet of Things and your Weather Station. 
See more details in the article:
https://blogs.sap.com/2017/08/15/create-your-own-weather-station-with-sap-cloud-platform-internet-of-things/

### Create Destinations

Open the SAP Cloud Platform Cockpit in a browser and go to `Connectivity > Destinations`.

Choose `New Destination` and create two new destination.

#### iotmms

* Name: `iotmms`
* Type: `HTTP`
* Description: `IoT MMS API`
* URL: `https://iotmms<ACCOUNT>trial.hanatrial.ondemand.com/com.sap.iotservices.mms`
* Proxy Type: `Internet`
* Authentication: `BasicAuthentication`
	* Enter your SAP Cloud Platform User and Password
	* User: `<ACCOUNT>`
	* Password: `<PASSWORD>`

#### iotrdms

* Name: `iotrdms`
* Type: `HTTP`
* Description: `IoT RDMS API`
* URL: `https://iotmms<ACCOUNT>trial.hanatrial.ondemand.com/com.sap.iotservices.dms`
* Proxy Type: `Internet`
* Authentication: `BasicAuthentication`
	* Enter your SAP Cloud Platform User and Password
	* User: `<ACCOUNT>`
	* Password: `<PASSWORD>`

### Import the Application in SAP Web IDE

Open the SAP Cloud Platform Cockpit,
go to `Services` and click on the tile `SAP Web IDE`.
If you have never used the Web IDE before, you may need to enable it first.
Click `Go to Service`.

In the Web IDE click `File > Git > Clone Repository`. Enter URL `https://github.com/Cyclenerd/iot-consumption.git` and click `Clone`.

The application is now available in your workspace.

### Deploy the Application to SAP Cloud Platform

If you want to run the application directly from the SAP Cloud Platform Cockpit, you need to deploy it into your SAP Cloud Platform account.

Right click your project folder in SAP Web IDE and choose `Deploy > Deploy to SAP Cloud Platform`.
Follow the instructions of the wizard.
Ignore the step for registering the application in the Fiori Launchpad.
After the deployment you find the application in the SAP Cloud Platform Cockpit under `Applications > HTML5 Applications`.

## Demo

https://iotconsumption-s0009028968trial.dispatcher.hanatrial.ondemand.com/