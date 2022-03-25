# BigDataProject

The above project implents a data engineering task using the big data system on Azure called Databricks. The project reads live streamed data into a blob storage, reads, explores and models that on Databricks and finally saves and registers the model so created. The workflow is as follows:

![image](https://user-images.githubusercontent.com/69780552/160043259-adc0e2e5-65d5-4c48-ae4c-98bc4df8ec9e.png)

The Demo_event.py randomly creates live streaming data. It randomly generates numbers for temp, humidity and uv. This data is captured using Event Hub. The event hub is connected to a storage container that stores all the values streamed. This data is then read, converted into csv and a compiled dataframe using the Notebook. Then the notebook generates some visualizations and stores back the same in the container storage for quick EDA. Then, MLflow is used to create and test a model. The final model is then saved in the DBFS and registered for future use/updation. 
