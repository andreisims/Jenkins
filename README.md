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
