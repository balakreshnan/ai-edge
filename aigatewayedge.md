# AI at Edge - AI at Edge Gateway Architecture

## Use Case

Leverage AI models in closer to Edge. For Example if we have to do people count, Face detection, Safety gear detection, Face mask, Contact tracing, Social distancing, Vest, Hard hats, Safety glass and other human based health and safety and other use case based model to a building, Factory floor, manufacturing facility or construction site or home or park or any where.

In manufacturing we can also use for quality detection use case, product count.
Also in Smart Building and Smart construction and lot more.

Ability to run custom vision based or sound based models built for vairous use cases and ability to deploy across multiple devices on the facility. Also able to scale that across multiple faciity. Capable of deploying different models in different facility. 

Manage and maintain model and it's deployment through docker containers from cloud or central location.

## Architecture

![alt text](https://github.com/balakreshnan/ai-edge/blob/master/images/aiedgeiot.jpg "Architecture")

## Architecture explaine

- Camera's in facility
- Microphone or other sound dectection device in facility
- Azure Stack Edge 1U Rack server one or many based on usuage
- Azure IoT Hub 
- Azure Data Explorer
- Dashboard to display what is getting predicted and stats
- Azure Cognitive services - Custom Vision, LUIS, Speech to Text and Others.
- Azure Machine Learning Services 
- Azure Container Registry 
- Azure Data Lake Store

Camera:
We need some camera's may be ai inferencing camera or regular camera with out wide angle. Options can be wither infra red or thermal depending on use cases. Camera can be hardened or military specification to withstand harsh condition

Microphone or Sound Detection device:
To get Voice or other sound to either detect voice and also sounds like cough, sneeze and other distress signals.

Azure Stack Edge:
This is our AI Gateway device with FPGA or GPU with power to inference few frames per second for example 50fps or more like 200fps. Also ability to add stack to scale as 1U rack server as needed. Services based so no inevst in hardware and can be cancelled when needed. This is the compute power we need to inference frames from video camer feeds from multiple camera's in a facility. 

Ability to bring in multiple feed like RTSP stream and then process multiple streams for real world scenario. The device form factor can change and also as the power of compute can change based on silicon innovation.

Azure IoT Hub:
To Configure, Manage and Maintain Azure Stack Edge devices. Also manage and maintain dockers modules deployed to azure stack edge. Cloud interface to manage all the facilities.

Azure Data Explorer:
Time Series data store used to store the detected data set for reporting or dashboarding purpose.

Azure Cognitive Services:
To build models using prebuilt functionality. For most vision based Custom vision service can be used and for languag understanding LUIS can be used.

Azure machine learning services:
To build you own custon deep learning or machine learning model azure machine learning services can be used. Options to build code using jupyter or drag and drop and build machine learning or automated machine learning as another option. Machine learning service has option to store secrets in Keyvault and also containers in Azure Container registry. Deployable as docker container using Azure Kubernetes service.

Azure Container Registry:
To Store docker images and containers.

Azure Data Lake Store:
Long term storage of data for data lake and other analytical use.

Conclusion
Now we have a AI@Edge platform scable.