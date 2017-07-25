# Tensfor For Poets

This lab is based on https://codelabs.developers.google.com/codelabs/tensorflow-for-poets

## Provision VM

You will need to Ubuntu 16.04 VM with at least 2x2 GHz CPUs, 4GB of RAM, and a 20GB local disk.
Please note the IP address of your VM once it is provisioned.  

## Setup TensorFlow

We will use Docker to run TensorFlow; you may install TensforFlow if wish (see https://www.tensorflow.org/install/) but for 
this exercise, Docker is simplier.  

The following steps assume you are running as root.

We'll start by installing Docker, see see https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/#install-using-the-repository for more details.

Update your apt package index with the following command 

    apt-get update
     
2. Install packages to allow apt to use a repository over HTTPS:

 sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common
    
3. Add Docker’s official GPG key:

 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
 
Optional: See detailed instructions on how to verify the key.

4. Configure repository:

 add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
   
5. Update the apt package index:

 apt-get update 
 
6. Install Docker:

 apt-get install docker-ce
 
7. Verify install:
 
 docker run hello-world
 
 This command downloads a test image and runs it in a container. When the container runs, it prints an informational message and exits.