# jenkinsApps

To Install jenkins - > open a terminal window and ensure you do a <Brew update/upgrade>
Then run the following command <docker pull jenkins/jenkins>
Create a Docker Vol to persist Jenkins Data to avoid losing the config <docker volume create jenkins-data>
Run the data Container - this starts jenkins and mounts the VOL created to persist data <docker run -p 8080:8080 -p 50000:50000 -v jenkins-data:/var/jenkins_home --name jenkins-master jenkins/jenkins>
-p 8080:8080 This publishes the Jenkins web interface on port 8080.
-p 50000:50000 This is used for Jenkins agent communication.
-v jenkins-data:/var/jenkins_home: This mounts the Docker volume to persist Jenkins data.
--name jenkins-master: This assigns a name to the container (you can choose any name


4. Access Jenkins: Open a web browser and navigate to http://localhost:8080.


5. To obtain the password < docker exec -it jenkins-master cat /var/jenkins_home/secrets/initialAdminPassword>


6. Complete the Jenkins setup
7 . create admin user after the pluggins installations
8 You can start using jenkins -
