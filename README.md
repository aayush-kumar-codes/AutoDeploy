# DevEnv/ProductionEnv Deployment Automation

![](images/CI:CD.png)


In this Project I have created an Automated System for deployment of application in Docker Container. The GitHub Repo for this project will have two branches, one for developer ie, <b>deploy</b> & another for main ie, <b>main</b>. The developer will commit to deploy branch and main will commit to main branch. As soon as the developer will commit, it will check for the website/application and if it is working properly then it will merge it with the production/main branch and will deploy it.

# Working Architecture and Use-Cases
In the above image you can see we have two persons sitting with Laptops and a Source Repository and then a CI Server from which the result is going back to one of the person sitting with Laptop. Let's assume one person is a developer of an organisation and another person is client. The Source Repository is GitHub in our case and CI Server is Jenkins.<br>
The working mechanism of this project is something like this. When I will push the code to github, it will be uplaoded to deploy branch as it is for developer branch. As soon as he will push the code, code from Jenkins will get triggered. If it is pushed in deploybranch then Docker Container for developer/testing environment will be launched and if it is pushed to main branch which is our production branch then Docker container for production environment will be launched. In this Project I made the testing part manually for deploy. If the testing of the developer environment is successfull and the new code doesn't give any error then, a Job is created which will automatically merge the deploy branch to production branch and deploy the application.
