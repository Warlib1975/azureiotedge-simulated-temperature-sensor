# Azure IoT Edge simulated temperature and humidity sensor module
IoT Edge module originally were developed by Microsoft as a IoT Edge module sample (C#). The project was located here: https://github.com/Azure/iot-edge-v1/tree/master/v2/samples/azureiotedge-simulated-temperature-sensor Now, the sources are moved somewhere, so 404 error occurred when going to the URI. 
It's not so easy to build module from the Microsoft sources. You need to change some files. Here is adapted version of the sources to simplify the simple module building.
Some description available in Russian at the page http://www.bizkit.ru/2018/11/12/5737/ 

To build module you need to do some changes in files:
1. Create in Microsoft Azure IoT Hub new Continers Registry. Get username and password to push compiled module. 
2. Create file with name ".env" filled with created Container Registry authorization data:   
	CONTAINER_REGISTRY_USERNAME_docker=
	CONTAINER_REGISTRY_PASSWORD_docker=
3. Change the property "repository" in the file module.json for your repository URI. Example: 
	"repository": "warlibregistry.azurecr.io/iotedge-simulated-temperature-sensor"
