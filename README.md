### PROJECT OVERVIEW 
This is the second project of the Udacity Azure ML Nanodegree program. In this project, we continued working on the Bank Marketing Dataset. With the use of Azure we configured a cloud-based machine learning Model through an experiment using Automated ML, deployed the Best Model which will allow us to interact with the HTTP API service and interact with the model by sending data over POST requests, consumed the deployed model using Swagger, used the endpoint.py script to interact with the trained model and we concluded by creating, publishing and consuming a pipeline.  

![alt text](https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/ArchitecturalDiagram.png)

### PROJECT IMPROVEMENT
1. Standardization is the end goal of any machine learning operationalization. ONNX enables you to develop in your preferred framework without worrying about downstream inferencing implications. It enables you to use your preferred framework with your chosen inference engine.Also hardware vendors can optimize the model for the target rather than the specific environment through the use of ONNX. It makes it easier to access hardware optimizations and it's compatible runtimes and libraries are designed to maximize performance across hardware.
2. Resampling to even the class imbalance, either by up-sampling the smaller classes or down-sampling the larger classes. These methods require expertise to process and analyze.
3. Review performance metrics for imbalanced data. For example, the F1 score is the harmonic mean of precision and recall. Precision measures a classifier's exactness, where higher precision indicates fewer false positives, while recall measures a classifier's completeness, where higher recall indicates fewer false negatives.

### PROJECT WORKFLOW
1.Registering the Bank Marketing dataset to be used for AutoML:
  i. Create a dataset by selecting the bank marketing dataset from local files.
  ii. The basic info page is displayed to be filled with the name, dataset type and dataset description.
  iii. The default datastore(workspaceblobstore)and supported file type were selected on the datastore and file selection page.
  iv. On the settings and preview page, the settings were automatically created and the selections were cross-checked to be correct.
  v. Details were confirmed and the Registered Bank Marketing Dataset was created.  
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Bankmarketingtrain.png

2. A completed AutoML run of the Bank marketing dataset shown as completed:
  i. A new autoML run was selected
  ii. The Registered bank marketing dataset was select
  iii. On the configure run page, a new experiment was created, target column was selected and a new compute was created with details of specification in mind.
  iv. On the Task type and settings page, Classification was selected as the task type and settings were checked to be satisfactory.
  v. AutoML run was successfully completed. 
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/AutoMLcompleted.png

3.Enabling Application Insight so as to visualize performance of the deployed model:
  i. On the logs.py script, the config was first downloaded to my current working directory.
  ii. deployment name was set to the name of my deployed model (bankmarketing-model)
  iii. An existing web service (service) was loaded using both the name and workspace.
  iv. service was updated to enable app insight(True)
  v. On Endpoint module, Application Insights enabled is set to true.
   https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/ApplicationInsightEnabled.png

4. The following screenshots show how logging was enabled by running the provided logs.py script:

    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript1.png

    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript2.png

    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Logscript3.png

5. Swagger running on locahost showing the HTTP API methods:
  i. On the Endpoint module, clicked on the swagger URL which takes us to a JSON Page
  ii. The page is save in the same directory as the swagger.sh and serve.py script
  iii. Ran the swagger.sh on a command prompt so as to download the latest swagger container and ran it on port 9000.
  iv. Ran the serve.py script so as to start a python server on port 8000 making such both files(swagger.json and serve.py)are in the same folder.
  v. Results is swagger runs on the localhost showing the HTTP API methods and responses for the model. 
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Swaggerresponsemodel.png

6. The endpoint.py script runs against the API producing JSON output from the model:
  i. On the Endpoint.py script, the scoring_uri and the key were updated with the key and URL generated after deployment.
  ii. The data on the script was also updated to fit the data on the bank marketing dataset.
  iii.After execution of the endpoint.py script results generated were as expected. 
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Swaggerresponsemodel.png
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/EndpointOutput.png

7. The following screenshots show the Apache Benchmark runs against the HTTP API using authentication keys in other to retrieve performance results:
  i. Apache Benchmark was installed and made available on my path.
  ii. The scoring_uri and the key were updated with the key and URL generated after deployment.
  iii. Ran the endpoint.py script to generate a data.json file.
  iv. Ran the benchmark.sh file and the output displayed were as expected.
  v. Apache Benchmark successfully runs against the HTTP API.
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Benchmarksh1.png
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Benchmarksh2.png
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Benchmarksh3.png
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Benchmarksh4.png
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Benchmarksh5.png

8.RunDetails Widget showing step runs
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/RunDetailsWidget2.png

9. Pipeline Created 
    https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Pipelinecreated2.png

10. Bankmarketing Dataset with the AutoML module
https://github.com/vikkyfama/Udacity-Project2/blob/toriabranch/Registered%20Bankmarketing%20Dataset2.jpg

11. 


### PROJECT DEMONSTRATION
  https://www.youtube.com/watch?v=faXQvcOkluQ
