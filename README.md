## Cloud Run For Google Translate API            
***Yunlong Liu***

### 1. Create project
   - Specify the project name.
   - Get Project ID.

### 2. Enable Cloud translation API
   -  Specify App name.
   - OAuth Client: "Web application".
   - Get your Client ID.
   - Download the credentials.
   
### 3. Get the "Google Translate" source code from this [repository](https://github.com/googlecodelabs/cloud-nebulous-serverless)

### 4. Switch setup between PyThon 2 and PyThon 3
   - Find Dockerfile In the resource folder .
   - Use ```FROM python:3-slim``` or ```FROM python:2-slim```.
	
### 5. Upload source code in order to use cloud build and deploy.

### 6. Deploy the application
   - Use command ```gcloud run deploy translate --allow-unauthenticated --platform managed```
   - Then you will be asked to provide the path to the source folder.
   - Select region.
   - (Optiona) If any required API is not enabled, you will be informed, type ```y``` to enable it. 

### 7. Confirm the status of your container
   - After receiving following output, the deployment is done:
   ```
Building using Dockerfile and deploying container to Cloud Run service [translate] in project [my-project-cloud-run-348804] region [us-central1]
OK Building and deploying new service... Done.                                                   
  OK Uploading sources...
  OK Building Container... Logs are available at [https://console.cloud.google.com/cloud-build/builds/2875772e-058c-4a4a-a06b-e03f2dcbd9df?project=266176326620].
  OK Creating Revision...                    
  OK Routing traffic...
  OK Setting IAM Policy...
Done.
Service [translate] revision [translate-00001-duz] has been deployed and is serving 100 percent of traffic.
Service URL: https://translate-vnkgeyrjqa-uc.a.run.app
```

- [x] Now the application is running on: <mark>https://translate-vnkgeyrjqa-uc.a.run.app/</mark>
   
   
   
   
   
   
   