Stage I

Goal is to install Ansible Tower on a VM of your choice and configure it completely.
 
1.       Signup for a GCP cloud account that will give you free $300 cloud credit for this exercise. 
https://cloud.google.com/free
2.       You can decide which VM will work for this exercise after reading through the instructions. Install open source Ansible Tower v 17.0.1 on this Linux instance from the following URL. Use  Kubernetes to install and build the AWX instance. Hint: use K8 provider of your choice.
                https://github.com/ansible/awx/blob/17.0.1/INSTALL.md#kubernetes
3.       After you make sure that AWX is installed properly, bring up the AWX console. Once successfully installed, The AWX web interface is running in the AWX pod behind the awx-web-svc Ingress service. Please attach a public IP/Load balancer to this this Ingress service address.
Make sure you can access the AWX running instance using PublicIP/Load balancer URL.
4.       Create a free GitHub account and clone the following repo into this GitHub account and name it ‘Panzura’. Add a folder named ‘Screenshots’ to this repo. Add another folder ‘Scripts’ to this repo. Add another folder ‘Output’ to this repo.
                https://github.com/ansible/ansible-tower-samples
5.       Please add a screenshot showing that AWX is installed properly and running to the ‘Screenshots’ folder of your GitHub repo.
6.       Using an editor of your choice, create one consolidated Ansible playbook(create_resources.yml) that will provision the following resources in your free GCP account.
a.       Create a GCP project named 'Panzura'
b.       Under this project, create 1 Google Cloud Redis instance
c.       Under this project, create 1 Google Storage bucket
d.       Under this project, create 1 Google Cloud SQL database
 
7.       Create a new AWX project, credential , template and job in Ansible Tower (You will need to figure out how all these work and interact with each other).
               Hint: Read through https://docs.ansible.com/ansible-tower/latest/pdf/AnsibleTowerUserGuide.pdf
8.       Point the new Ansible playbook you created to the newly created template/job in step 7
9.       Run the create_resources.yml playbook to provision step 6
10.   Please add a screenshot to the ‘Screenshots’ folder of your GitHub repo indicating successful run of playbook from Ansible Tower
11.   Also upload this Ansible create_resources.yml  playbook to ‘Scripts’ folder of your GitHub repo
12.   Add the output of this creation playbook to your 'Output' folder of GitHub repo
13.   Now create a Ansible playbook destroy_resources.yml to destroy everything created in step 6
14.   Add this playbook destroy_resources.yml  to the ‘Scripts’ folder of your GitHub repo as well
15.   Add the output of destruction playbook to your 'Output' folder of GitHub repo
 
  
Stage II
 
1.       Create a free tier AWS account and create a free tier VM of your choice.
2.       Create an AWS Lambda function using Python runtime to check if an input string is a Palindrome or not. Upload the output of this function to the 'Output' folder in your GitHub repo.
3.       Install Jenkins container on the AWS Virtual Machine that you provisioned using Docker's latest version (download whatever required) and bind it to host port 8080.
4.       Browse to the Jenkins instance you created from your PC (port 8080)
5.       Create a declarative dummy Jenkins Job that prints "Hello Panzura!". Upload the Jenkins file to Scripts folder of GitHub repo
6.       On the Virtual Machine write a bash or python script that reads the last line of Jenkins log and output it to another file. The script shall be scheduled with crontab to run every minute. Upload this script to 'Scripts' folder of the GitHub repo.
7.       Output of ‘docker ps’  to show the running Jenkins container. Name it as ‘Container_status_Jenkins.txt’ and upload it to 'Output' folder of GitHub repo.
     
