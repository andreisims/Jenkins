# Learning Jenkins
I'm sharing my journey of learning Jenkins and how it’s helping me grow in DevOps! This will be the general outline for my progression:
<li>Jenkins Pipelines: What they are and how they are used</li>
<li>Parameterized jobs: Pass information between the different jobs</li>
<li>Integration with GitHub: Jenkins and GitHub go hand-in-hand</li>
<li>Breakdown of how to use Jenkinsfiles: From the ground up and for a complete beginner</li>
<li>Jenkinsfiles and Declarative Pipelines</li>
<li>Scripting your CI/CD solution</li>
<li>Functions in your Jenkins pipelines</li>
<li>Multistage Pipelines in Code</li>
<li>Declarative Pipeline Language</li>

<h2>Install Java</h2>
<h3>Create EC2 instance in AWS</h3>

 <li>name it (Jenkins-Server)</li>
 <li>select Ubuntu image</li>
 <li>t2.micro (may need to increase size depending on job)</li>
 <li>create keypair (Jenkins-serverkey)</li>
 <li>create security group (name Jenkins-sg), SSH, source type (My IP), custom TCP port 8080, source type (MY IP), keep other defaults. launch instance</li>
 <li>SSH into the instance from Git bash (ssh -i Downloads/Jenkins-serverkey.pem ubuntu@'instance publice IP</li>
 
 ![ssh to instance](https://github.com/user-attachments/assets/e2ea096b-7234-4614-b6d1-66c92845a209)

 <li>become the root user (sudo -i)> then enter "sudo apt update"</li>
 <li>Install JDK (sudo apt install openjdk-21-jdk -y)> then enter "java -version" to display the current version</li>

 ![installs](https://github.com/user-attachments/assets/83af0298-f879-4d70-be2e-87dc3d664370)
 ![java version](https://github.com/user-attachments/assets/5ba98da4-2b18-4ecd-b180-7e876fd830c2)

 <li>download repository key (Jenkins.txt file)</li>
 <li>create repository file (Jenkins.txt file). then enter "sudo apt update"</li>

 ![repository file](https://github.com/user-attachments/assets/5a08c780-7aa4-4f39-b051-8b0b0578104f)

 <h2>Install Jenkins</h2>
 <li>sudo apt-get install jenkins -y</li>
 <li>check Jenkins status (systemctl status jenkins)</li>

 ![jenkins status](https://github.com/user-attachments/assets/9c6a8cd6-4bfa-41a6-b777-ccd3a4884f22)

 <li>view Jenkins home directory (ls /var/lib/jenkins). The Jenkins home directory is the backbone of the Jenkins setup. Losing this directory can mean losing all jobs, configurations, and build histories. Best practice is to back up regularly</li>

 ![jenkins directory](https://github.com/user-attachments/assets/647db191-b8c8-4fdf-92ad-22867d504d69)

 <li>access Jenkins from Browser (public IP of Jenkins-Server in AWS and port 8080)</li>

 ![jenkins browser](https://github.com/user-attachments/assets/1b2b80c1-41c7-4845-a5ca-dd432f677b14)

 <li>signin with the provided password. copy/paste password (cat /var/lib/jenkins/secrets/initialAdminPassword)this is the initial password that you will change once logged in</li>

 ![password](https://github.com/user-attachments/assets/418f8a47-bc83-46bb-8a73-3185b4cda0b5)

 <li>click "select plugins to install" (check nodejs> select install)</li>

 ![plugins](https://github.com/user-attachments/assets/b417dc60-6511-47d9-bb3b-3d2d3f054e88)
