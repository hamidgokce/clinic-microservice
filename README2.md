In my recent project, I worked mainly on a micro-services application fully automated.
	It was a Dockerized Web Application developed in Java Springboot, Spring Cloud Frameworks and integrated with MySQL database. The code was developed in Java
The name of our project is Clinic. The clinic is a web page where customers can make an appointment for their pet online and enter information into the page. Also, they can search for veterinarian names on a website. 
    In This project, we as DevOps engineers aimed to create a full CI/CD Pipeline for microservice-based applications and deployment on a Kubernetes cluster with monitoring.
 
    
 I would like to inform you about which tools we used on the project and for what purpose.

	► We created all the infrastructure on AWS EC2 Service. 
	► We used Git as the version control system during the whole process. We prepared base branches namely master, dev, and release for the DevOps cycle.
	► Jenkins was used as the CI/CD automation tool.
	► Maven was used as the build tool. So I used Maven Wrapper for the testing, packaging, and installing phases.                                                                                             
	► We were able to store docker images and java jar files on the Nexus server.
	► We used Ansible to configure the instances and prepared some playbooks. Since we used the AWS Cloud platform, I prepared a dynamic inventory that includes EC2 instances. In addition, to be able to connect Ansible to our EC2 instances, I wrote an Ansible config file within the Jenkins pipeline. 
	► Our app is running on AWS, we used Terraform instead of AWS cloud formation as Infrastructure as a Code. Because Terraform is a cloud-agnostic tool. Also, I spun up the development server through a Terraform template.
	► Kubernetes cluster was created for deployment. Rancher was created to easily manage the Kubernetes cluster. For creating Rancher, I used Helm's existing repo for Rancher. With Rancher, we easily made changes in the cluster for staging and production environments via its dashboard, add nodes, delete nodes, edit configuration files, and used kubectl in its terminal. (A tool that allows us to manage the Kubernetes cluster more easily. Instead of using the CLI, it adds visuality.) 
	► For making switch easy we used some tools like Kompose and Kustomize tools. We converted the Docker-compose files to Kubernetes definition files by using the Kompose tool. We also used the Kustomize tool to add some customization to these definition files -like changing replica numbers or image tags.
	► We used Jenkins pipeline scripts to deploy the application to both staging and production environments. 
As monitoring tools: we monitored the applications in the cluster with Prometheus and Gra