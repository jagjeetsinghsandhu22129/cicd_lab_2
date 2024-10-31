In this lab2 i set up an automated CI/CD pipeline using Jenkins integrated with GitHub. 

Steps:
-   Set the Jenkins Integration with GitHub
-   Connect Jenkins to GitHub by generation a Personal Access Token on GitHub for the Authentication and add on the Jenkins under the Credentials.
-   Configure the Repository with URl and also provided the PAT to access the repository.
-   Than set Jenkins to monitor the specific branch which is main

  
-   Create the Jenkins Pipeline Job
-   Defined the Jenkins pipeline job with the Checkout, Build, Test and Notificatio stages.

-   Trigger Method:
-   I used Polling Based Approach
-   Configure Jenkins to poll the GitHub repository at regular intervals of every 5 minutes.
-   Use the pollSCM option in the Jenkins pipeline to specify polling frequency.


-   I did a code change in GitHub. 
-   Confirmed that Jenkins detects the change and triggers a build.
-   Verify that each pipeline stage (checkout, build, test, notification) executes successfully.
