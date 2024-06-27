# Jenkins


What is Jenkins:

Jenkins is an open source automation server runs on the Java Virtual Machine (JVM). Jenkins automates the tasks such as building, testing, and deploying or delivering the software projects through Continuous integration and Continuous delivery (CI/CD) pipelines.

Why use Jenkins:
we can use Jenkins because it automates the process of building, testing, and deploying code, which improves development efficiency and reduces errors. And it supports continuous integration and continuous delivery (CI/CD), allowing for faster and more reliable software releases.

➡ And Jenkins has a vast plugin ecosystem, offering a wide range of integrations for various tools and platforms and to avoid security issues by storing our credentials under manage credentials option.

What is pipeline:

pipeline is typically divided into multiple stages and steps, with each step representing a single task and each stage grouping together similar steps.

What is Continuous Integration:

Continuous Integration is the process of automatically building and testing of code whenever changes are committed by developer to the version control system.

What is Continuous Delivery:

Continuous delivery is a software development practice where code changes are automatically prepared for a release to the production. →And with continuous delivery every code change is built, test, and then pushed to the non-production testing or staging environment. And here can be multiple, parallel test stages before to a production deployment.

What is Continuous Deployment:

Continuous deployment is the process where code changes to an application are deploys automatically into the production environment.


Run the below commands to install Java and Jenkins

** Install java

sudo apt update

sudo apt install openjdk-11-jre

* Verify Java is Installed or not
  
java -version

** Now install jenkins : 

curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
  
   sudo apt-get update 

   
  sudo apt-get install jenkins

Insatll Docker :

sudo apt install docker.io

Grant permissions to jenkins user and ubuntu user to docker

sudo su - 

usermod -aG docker jenkins

usermod -aG docker ubuntu

systemctl restart docker


check docker status with (docker run hello-world) command


Switch to jenkins :

su - jenkins

-> Install docker-pipeline plugin

-> Restart jenkins whenever we installed jenkins plugins to pickup changes.And it is better practice to restart jenkins on everytime whenever we make any changes to reflect back to us.

-> After click on available plugins and search for the docker pipeline and do install after restart.

-> Now click on configure -> SCM(Source Code Management) -> Git -> Start

-> Finally click on the build ,now and it's starts process of building pipeline.After few seconds process finished.

-> Jenkins says to docker that when there is a request create a docker container as soon as process done or completed stop or delete that container.(This architecture saves time and cost).
