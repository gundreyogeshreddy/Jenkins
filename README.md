# Jenkins

What is Jenkins : 

Jenkins is self-contained, open source automation server which can be used to automate all sorts of tasks related to building, testing, delivering or deploying software. And jenkins is written in Java programming language.





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
