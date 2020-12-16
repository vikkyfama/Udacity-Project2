### PROJECT OVERVIEW 
This is the second project of the Udacity Azure ML Nanodegree program. In this project, we continued working on the Bank Marketing Dataset. With the use of Azure we configured a cloud-based machine learning Model through an experiment using Automated ML, deployed the Best Model which will allow us to interact with the HTTP API service and interact with the model by sending data over POST requests, consumed the deployed model using Swagger, used the endpoint.py script to interact with the trained model and we concluded by creating, publishing and consuming a pipeline.  

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/ArchitecturalDiagram.png)

### PROJECT IMPROVEMENT
Standardization is the end goal of any machine learning operationalization. ONNX enables you to develop in your preferred framework without worrying about downstream inferencing implications. It enables you to use your preferred framework with your chosen inference engine.Also hardware vendors can optimize the model for the target rather than the specific environment through the use of ONNX. It makes it easier to access hardware optimizations and it's compatible runtimes and libraries are designed to maximize performance across hardware.

### PROJECT WORKFLOW
1. Registering the Bank Marketing dataset to be used for AutoML. Dataset is saved in the blobstore of the respective workspace.
![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Bankmarketingtrain.png)

2. A completed AutoML run of the Bank marketing dataset displaying the Best Model Achieved and a summary of the details.
![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/AutoMLcompleted.png)

3.Enabling Application Insight so as to visualize performance of the deployed model.
![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/ApplicationInsightEnabled.png)

4. The following screenshots show how logging was enabled by running the provided logs.py script:

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript1.png)

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript2.png)

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript3.png)


![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Swaggerresponsemodel.png)

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/EndpointOutput.png)
