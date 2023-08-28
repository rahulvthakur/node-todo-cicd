Below are the steps to follow in Jenkins - 

- Create a new project in Jenkins
- Add the GitHub URL of this project in the Source Code Management section.
- Select 'GitHub hook trigger for GITScm polling' in 'Build Trigger' section
- Add the build steps to start the container and the save the project

Below are the steps in this GitHub project -

- Go to the settings of this project and go to webhooks section and click 'Add webhook'
- In the payload URL, add the public IP address with the port on which you are accessing Jenkins and 'github-webhook'
- So, it will look like - 'http://1.1.1.1:8080/github-webhook/'
- Select just the push event in next option and click on 'Add-webhook'
- Now make any changes in this project and commit them.

- In Jenkins, auto build will happen as and when we commit some changes to GitHub. It is happening because of GitHub Webhooks that we added in rep settings.
  So whenever user commits to the project it triggers the added webhook and make changes on Jenkins.
