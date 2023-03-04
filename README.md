# AWS_Pipeline_demo
-----------------------------------------------------------------------------------------

## Description:
This is just a simple counter app which can be deploy using AWS pipeline.

## Somewhat about the background study:
* AWS CI/CD pipeline is a service offered by Amazon Web Services (AWS) that helps developers automate the continuous integration and continuous delivery/deployment (CI/CD) of their software applications. The pipeline is designed to help teams release high-quality software updates quickly and efficiently by automating the build, test, and deployment process.

![image](https://user-images.githubusercontent.com/49017322/222925185-3a180cbd-df53-4a78-96b6-0be48c3b6bed.png)

* CI/CD is a methodology used by development teams to deliver new software updates and features to users as quickly and efficiently as possible. Continuous integration refers to the practice of automatically building and testing software changes as they are made, while continuous delivery/deployment refers to the process of automatically deploying these changes to production environments once they have been tested and approved.

* The AWS CI/CD pipeline service provides a fully managed platform for teams to implement these practices using a variety of AWS services, including AWS CodeCommit for source control, AWS CodeBuild for building and testing, AWS CodeDeploy for deployment, and AWS CodePipeline for orchestrating the entire process.

* The pipeline service also includes features like automatic scaling, versioning, and release management to help teams streamline their software delivery processes and reduce the risk of errors and downtime.

* Overall, the AWS CI/CD pipeline is a powerful tool for development teams looking to automate their software delivery processes and improve their ability to release new updates and features quickly and efficiently.


## Instruction :
### 1. Make a github link & push your project to github.

### 2. Navigate to AWS Console Panel ---> Search for the CI/CD Pipeline 

![Screenshot from 2023-03-04 21-22-38](https://user-images.githubusercontent.com/49017322/222924959-19629e14-5744-4087-81fc-7ceb7e1d07a3.png)


[AWS MAnagement Console](https://us-east-2.console.aws.amazon.com/console/home?region=us-east-2)
[AWs CodePipeline](https://us-east-2.console.aws.amazon.com/codesuite/codepipeline/home?region=us-east-2)


### 3. Inside of the CodePipeline Panel: Click "Create Pipeline"

![Screenshot from 2023-03-04 21-22-38](https://user-images.githubusercontent.com/49017322/222925301-c15b88d0-2498-4961-80d5-5ace8a439592.png)


Then this will take us to the new "Pipeline setting pages"

![Screenshot from 2023-03-04 21-32-36](https://user-images.githubusercontent.com/49017322/222925355-0bba70e0-f947-45e4-b4d4-78cbfa85af0c.png)

### 4. PipeLine settings:
Make your own settings for this Pipeline. This is a example of how this would look like:

![Screenshot from 2023-03-04 21-38-08](https://user-images.githubusercontent.com/49017322/222925535-5a3c081e-d89a-4f32-975b-ebe363c2f228.png)

Click "Next" to continue the next step.
For the source code provider , let choose github for our connection.

![Screenshot from 2023-03-04 21-39-03](https://user-images.githubusercontent.com/49017322/222925599-bfea9e99-38ed-4b77-825c-709bcf5e92cf.png)


Then Click on "Connect to github". On the 2nd window.
Feel free to name this connection. Then Click "Connect to github".

![Screenshot from 2023-03-04 21-58-29](https://user-images.githubusercontent.com/49017322/222926258-195fee32-2567-411d-8ca9-75d0d0e8ba61.png)


So this will ask for connection from AWS Management Console to GitHub.
Just sign in with your github for the next Authentication step.

![Screenshot from 2023-03-04 21-41-30](https://user-images.githubusercontent.com/49017322/222925720-03782f2d-ad22-4c36-be6e-a01d13529d74.png)

Select "Authorize AWS Connector for GitHub" to confirm the connection.
Then, you should able to view the updated message on AWS Pipeline settings page && continue to fill out the rest of the form with your Giuthub links, the name of the github branch.

![Screenshot from 2023-03-04 22-01-41](https://user-images.githubusercontent.com/49017322/222926432-6d117bfd-b34d-48ff-9665-17ca36b25cbe.png)

Also select "Codepipepline default". When you done with this steps, just click on "Next".

ADD build stage

For the build provider : Just Select AWS codebuild

Then choose your country location for the next step.

Then Click on "Next" to confirm this set up.

![Screenshot from 2023-03-04 22-13-45](https://user-images.githubusercontent.com/49017322/222926825-91c071b7-9b84-4ba2-8fe1-b18193c7438c.png)


Add Deploy Stage
The deploy form should look like this:

![Screenshot from 2023-03-04 22-16-28](https://user-images.githubusercontent.com/49017322/222926869-edaf5fb3-e441-4903-aeed-d2100a7acf69.png)

Then open a new tab to search for AWS Bucket ---> Create  a new Bucket from that site.

![Screenshot from 2023-03-04 22-17-47](https://user-images.githubusercontent.com/49017322/222926929-2b901afd-2385-4a90-8671-6c133a6806dd.png)

![Screenshot from 2023-03-04 22-19-22](https://user-images.githubusercontent.com/49017322/222926980-d9c97f21-5733-456f-a94e-ec3aa95e9363.png)

![Screenshot from 2023-03-04 22-19-42](https://user-images.githubusercontent.com/49017322/222926987-ffefc074-72f1-4e21-8122-e81eb565da42.png)


Then come back to the Add Deploy Stage:
Fill up the rest of the form with:

![Screenshot from 2023-03-04 22-22-07](https://user-images.githubusercontent.com/49017322/222927076-678eb638-91f8-40fb-8eeb-2fc9bfc62b2f.png)


Then confirm the setting , and we should be able to review the contents of our set up.

![Screenshot from 2023-03-04 22-22-56](https://user-images.githubusercontent.com/49017322/222927159-0f8ae2f3-6973-4cf6-88ab-2d6c7a4e7b09.png)

![Screenshot from 2023-03-04 22-23-15](https://user-images.githubusercontent.com/49017322/222927168-8bf569a1-f4e7-453b-9906-0fb7d40320c5.png)

![Screenshot from 2023-03-04 22-23-20](https://user-images.githubusercontent.com/49017322/222927171-d70f02f1-fa45-48b7-a082-41b590dbaf93.png)

Finally, select "Create Pipeline " to confirm the final selection.

The sucessfully message will appear.

![Screenshot from 2023-03-04 22-25-21](https://user-images.githubusercontent.com/49017322/222927223-488a644d-1f42-4153-ac55-9a4d12d98b34.png)


Once the build && deploy has completed. Let make the 3S Bucket public.

Use the Static website Hosting mode, then specify the index.html for hosting website. Save that settings.

![Screenshot from 2023-03-04 22-31-50](https://user-images.githubusercontent.com/49017322/222927522-101c5a49-8ee8-43fc-a646-4a5b97674e1c.png)

Then Navigate to the "Permission" , and uncheck these options:

![Screenshot from 2023-03-04 22-35-23](https://user-images.githubusercontent.com/49017322/222927580-9be59cd6-d587-4974-902d-b5494f2ad3b0.png)

So that we could have the public access.

![Screenshot from 2023-03-04 22-36-28](https://user-images.githubusercontent.com/49017322/222927598-8a6037de-506a-4458-8713-4e37d6869fbb.png)
Confirm and save this settings.


Then navigate to the Bucket policy , and types in :

![Screenshot from 2023-03-04 22-37-19](https://user-images.githubusercontent.com/49017322/222927645-5f7bb612-c452-4b3f-bfa9-75f57bf5628b.png)
Replace the final line with your Bucket's name .
In my case, it is "pipelinecounterdemo". Then save it. 
When sucessfully saved it, we can go back to the Overview :

![Screenshot from 2023-03-04 22-39-36](https://user-images.githubusercontent.com/49017322/222927736-e7d5dbc8-8da4-4f3a-8385-f87abe58d843.png)

Then we can click on index.html, this will give us an object URL

![Screenshot from 2023-03-04 22-40-43](https://user-images.githubusercontent.com/49017322/222927766-89660be1-0a65-4214-9969-07eef652a120.png)

You can follow the URL to see the actual running app.

### Notes: This is just a demo of configuration for AWS CI/CD Pipeline Usage.

This settings is 100% validate, however, I might changes some configuration or delete this AWS at some point.

Therefore, the URL might not exist or available for public user to interact with.

-----------------------------THANK YOU SO MUCH FOR YOUR TIME---------------------------------


