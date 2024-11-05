# JenkinsAssignment
## Java Installation
- 3 instances(The master will be used as the developer machine while the remaining 2 instances will be used for production server and test server)  are created on AWS \
-Java 17 is installed on each of them. \
![Installing java](./img/1.aInstallJava.png)
## Jenkins Installaton 
- On the master Jenkins is installed, Jenkins installation documentation is saved on a sh file and ran as shown in the second diagram below.
![installing Jenkins](./img/1.binstallJenkins.png)
![Running Jenkin](./img/1.binstallJenkinsb.png)


- Check if Jenkins services is running
![installing Jenkins](./img/1.binstallJenkinsc.png)

- Access Jenkins Dashboard \
The Jenkins master public Ip is pasted in the browser to access the jenkins dashboard. The path on the Jenkins dashboard is copied back to the terminal to get the admin password  \
![AccessPassword](./img/1.binstall%20Jenkins.png)

## Assignment 1 and 2

### Git
Index.html page was created committed to git, the develop branch was also created, the aboutus.htm page was created.
#### Master Branch Commit
![Master Branch Commit](./img/6.pushng%20to%20github.png)

#### Develop Branch Commit
![Develop Branch Commit](./img/3.creatingdevelopbranch.png)

#### Created Nodes(s)
Here the ProdServer and TestServer Nodes were created. The  private IP of each of the servers where pasted under host in the under lunch method.
![Create Node](./img/5.createdNodes.png)

#### Create  Job
Created the TestJob and ProdJob, In the configuration of the TestJob, my git repository was specified and under branch i added the develop branch, under the build triggered, the GITScm polling was selected.
![Create Job](./img/testjob.png)
![Create Job](./img/createdjobs.png)

### Added GitHub Webhook
A webhook was added to my repository  by pasting my Jenkins IP address. See the img below
![Create Job](./img/webhook.png)

### Pushing Develop Branch To Github
The develop branch was pushed to git hub and this automatically triggered the test job  and automatically the files on the develop branch was pushed to the Test server
![Push Develop Branch](./img/6.pushng%20to%20github.png)
The TestServer after the push of develop branch
![Test Server After](./img/6TestServerAfterPush.png)
The Pushing Master branch
![Push Master Branch](./img/jenikinsassignment2terminal.png)
The ProdServer after the push of master branch
![Push Master Branch](./img/jenikinsassignmentProdterminal.png)
### Assignment 3
The img shows the configuration setting for the prodjob. This job runs after the the test job builds successfully

#### Configuration of jobs

TestJob Configuration
![TestJob Configuration](./img/postbuild.png)

ProdJob Configuration
![ProdJob Configuration](./img/prodjobpostbuild.png)

#### Test Server after a successfull Testjob Build
After a Successfull 
![ProdJob Configuration](./img/assignment3terminalaftertriggertestserver.png)


#### Prod Server after an automatic building of Prodjob after a successful testjob build

![TestJob Configuration](./img/assignment3terminalaftertriggerproductionserver.png)













