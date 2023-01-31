
# UI instructions

## Login to the UI  

The UI is available here: [https://mx01.neosdata.net](https://mx01.neosdata.net)

username: neosadmin
password: 

## Create a data product using spark to get data from a remote database

### Create data product  

1. click on 'create new data product'
2. set data product name to be 'learner_certifications'  (this has to match the name used in the spark file)
3. click on 'paste json' and copy the contents of the learner_certifications.json file into the data schema text box.  
4. set the engine to be 'postgresSQL' (this has to match the code in the spark file)
5. set the data product type to 'stored'  
6. click 'save and continue'

### metadata  

Note: It is possible to add tags for decorating data products here: [https://mx01.neosdata.net/tags](https://mx01.neosdata.net/tags)
These need to be created before you add them to the data product.  

1. to update the metadata on a data product click on 'metadata management'  
2. Now it is possible to update the description and PII settings for each field in the data product  
3. It is possible to extend the search key words be using any of the predefined tags (see note above)  

### Upload data  

This step is used to upload data into the data product using a spark job which the code can be uploaded. It is necessary to add secrets for the spark job to use to connect to the upstream database we have used defaults for everything except the database password.  

1. click on 'upload data'  
2. click on 'browse files'  
3. navigate to the learner_certifications.spark file
4. 'Add secret' enter key 'SC_PASSWORD' enter value: 'scpass'  and click save
5. click connect  
6. there is an issue with the redirect , click on 'upload data' and wait for the data to be uploaded.  
7. then click back to 'upload data' to see the upload has been successful and see a preview of the data 

### publish the data product  

1. click on 'preview and publish'  
2. click on 'publish'  
3. the data product is now published and ready to be consumed.  

## Create a data product using csv file

### create data product (csv flow)

1. navigate to 'my data products' and click on 'create data product'
2. set data product name to 'worker_safety'
3. click on 'upload csv' and navigate to the worker_saftey.csv file, this should then show you a schema from the csv file.  
4. set the engine to 'postgres'  
5. click 'save and continue'  

### metadata  

Note: It is possible to add tags for decorating data products here: [https://mx01.neosdata.net/tags](https://mx01.neosdata.net/tags)
These need to be created before you add them to the data product.  

1. to update the metadata on a data product click on 'metadata management'  
2. Now it is possible to update the description and PII settings for each field in the data product  
3. It is possible to extend the search key words be using any of the predefined tags (see note above)  

### upload data  

This process is automatic and the data in the chosen csv file will be ingested automatically into the data product, this will take 2 to 3 minutes to execute.  

### publish the data product 

1. click on 'preview and publish'  
2. click on 'publish'  
3. the data product is now published and ready to be consumed.  
