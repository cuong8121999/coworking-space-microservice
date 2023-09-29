## The README file serves as documentation for user to detail how deployment process works and how the user can deploy changes. 

### How deployment process works:

1. AWS CodeBuild will be triggered by push action of user to Github Repo.
2. AWS CodeBuild Service conducts pre-build, build, and post-build actions to rebuild the image and publish it to AWS ECR Repo
3. AWS EKS will use newly built image to deploy on application service

### How the user can deploy changes:

1. Modify and push changes of the application to the GitHub Repo
2. Check the latest tag of deployed image from AWS ECR Repo
3. Access into 'deployment' folder and modify the latest tag of image collect from step 2
4. Check the status of new deployment with some kubectl commands