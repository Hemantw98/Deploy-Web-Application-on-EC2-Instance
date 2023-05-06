## Deploy Web Application on EC2 Instance (manually)

### Technologies used:

AWS, Docker, Linux

### Project Description:

Create and configure an EC2 Instance on AWS Install Docker on remote EC2 Instance

Deploy Docker image from private Docker repository on EC2 Instance

### Here are the steps to deploy a web application on an EC2 instance manually:

### 1. Create an EC2 Instance on AWS:

Log in to your AWS account and navigate to the EC2 dashboard.

Click on the "Launch Instance" button.

Select the appropriate Amazon Machine Image (AMI) and instance type.

Configure the instance details such as network, security, and storage.

Review and launch the instance.

### 2. Connect to the EC2 Instance:

Use an SSH client to connect to the EC2 instance using the instance's public IP address and the private key pair created during the instance launch.

### 3. Install Docker on the remote EC2 Instance:

Update the packages on the instance by running the following command:

    sudo apt-get update

Install Docker using the following command:

    sudo apt-get install docker.io

Verify the installation by running the following command:

    sudo docker --version

### 4. Configure Docker to access private Docker repository:

Log in to your private Docker repository using the following command:

    sudo docker login <repository-url>

Enter the credentials for your repository.

### 5. Deploy Docker image on EC2 Instance:

Pull the required Docker image from your private Docker repository using the following command:

    sudo docker pull <repository-url>/<image-name>:<tag>

Run the Docker container using the following command:

    sudo docker run -p 80:80 -d <repository-url>/<image-name>:<tag>

This command maps the container's port 80 to the host's port 80 and runs the container in the background.

### 6. Access the web application:

Open a web browser and enter the EC2 instance's public IP address.

The web application should now be accessible.

That's it! You have successfully deployed a web application on an EC2 instance manually.
























