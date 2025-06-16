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

## ACCESSING JENKINS 

![port 8080 activation](https://github.com/user-attachments/assets/0a830340-c1b7-4fdd-8f2b-8cb7db4b6483)

Access the the jenkins file fron the browser using "http://<public-ip-adress>:8080

Coppy the file higlighted below to get jenkins password .

![jenkins page and file ](https://github.com/user-attachments/assets/a5e22b34-6eaf-4847-b75c-023b85af3f8f)

Use the comnand "sudo cat /var/lib/jenkins/secrets/initialAdminPassword" and the outpot will be your pasword to access jenkins 

![image](https://github.com/user-attachments/assets/2e93de4a-50b2-4138-85c9-16b2cdd435fd)

install provided plugings 

![install plugings provided by jenkins for start ](https://github.com/user-attachments/assets/ce964689-2da5-4066-98fe-a86655b0f870)

## Security measures on Jenkins server .

Dont log as an admin but use your own credentials with a password to log in so that not everyone can access jenkins .

![log in as a user ](https://github.com/user-attachments/assets/1d16b501-95e3-4f04-8544-33fae71c4)

further configurations 

![Screenshot 2025-06-16 165435](https://github.com/user-attachments/assets/6bebbaea-5b5e-48cd-a554-71dfaa482121)
 







