# Creating CI Pipeline for React App and host it using Amazon S3
Step 1: Create ReactApp 
Step 2: Push the code to Github repo "https://github.com/LeelaRajan/ReactPipeline"
Step 3: Create the IAM user in AWS cloud with provided policies [AmazonS3FullAccess & IAMUserChangePassword]
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/2376e7a8-628f-4df3-b508-d38aafe05fc6)
Step 4: Create an Access key from the security credential section of the newly created user
Download .csv file for accesskey 
Step 5:  Create an S3 bucket 
Give a name to the bucket and enable ACLs.
Untick Block all public access and tick the warning after reading it.
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/588eca9c-f339-426b-96d3-14127e57891f)
After this hit create bucket button and you are done with creating a new user and storage.
Step 6: Go to the settings of your repo and select the secrets from the left section.
Provide three secret key with their provided access keys.
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/b17b010c-3c13-4011-b58a-4629c22c8c47)
Step 7: Add one folder “.github\workflows” and add a new file in it and name it “main.yaml”. 
Step 8: Go to the Action section and see the process
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/0959d45c-5f01-4929-a187-cdd48ce6d2d7)
Step 9:  All process is finished and the build file is uploaded to the given bucket name in aws.
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/8a7c4b2e-8ae1-4606-bafe-4093a58a2e93)
Step 10: Configure S3 for web hosting
Now go to the Properties section and scroll down to the end. You can see the Static website hosting option. Click on edit and enable it and write index.html in the index document section. Then save changes.
Now you can see a link in the static website hosting section. Open it in a new tab.
![image](https://github.com/LeelaRajan/ReactPipeline/assets/46046284/db3cb4a9-5f5a-4287-8e54-88e6fdbdad89)
