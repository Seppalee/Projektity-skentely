# Assignment 4

**What is the purpose of environmental variables?**

Environmental variables are a practical way of externalizing a containerized app configuration. When they are included in a Docker image, they become available to app containers created based on image. ARG variables are used to store high-level configuration parameters, such as the version of the OS. Their only purpose is to assist in building a Docker image. ENV variables store values such as API keys and database URLs. Unlike ARG variables, these persists in the image. 

**What is DCT, and what does it stand for?**

Through DCT, image publisher can sign the images and image consumers can ensure the images are signed and official versions. It stands for Docker Content Trust.

**How can you monitor the docker in production?**

Docker states and Docker events are used for monitoring docker in production environments.