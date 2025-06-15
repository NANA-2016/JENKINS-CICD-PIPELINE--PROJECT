# JENKINS-CICD-PIPELINE--PROJECT

Located the key using the command cd Downloads as the key is located in the downloads file .
I made the key not to be accessed publicly by running the command "chmod 400 Nana.pem"
Used the command "ssh -i "Nana.pem" ubuntu@ec2-13-49-68-73.eu-north-1.compute.amazonaws.com" to connect to the instance .

![connecting privately to the ecs server using ssh](https://github.com/user-attachments/assets/0f2187d8-ecad-4dc0-a5bb-a35705606b84)

## INSTALLATION OF JENKINS.

Use the following commands to install jenkins and ensure it is up and running .

Install Java .
"sudo dnf install java-17-openjdk -y"

Run Jenkins repository.
"curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null"

Install Jenkins 
 " sudo apt update
sudo apt install -y jenkins"

Start and enable jenkins .
sudo systemctl start jenkins
sudo systemctl enable jenkins

Check Jenkins Status to ensure its enable and running .
"sudo systemctl status jenkins"

![jenkins status post installation](https://github.com/user-attachments/assets/8cbdd8ef-b9cc-4964-a7fe-aaa8f80004b6)

Activate port 8080 on the EC2 instance inbound rule to enable access OF Jenkins through the browser 

![port 8080 activation](https://github.com/user-attachments/assets/0a830340-c1b7-4fdd-8f2b-8cb7db4b6483)


