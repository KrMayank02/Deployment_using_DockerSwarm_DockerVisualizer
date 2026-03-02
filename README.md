# Application Deployment using Docker Swarm and monitoring using Docker Visualizer

**Objective:** The Project is implemented to deploy a scalable, multi-service voting application on a Docker Swarm manager node, ensure efficient orchestration, fault tolerance, and seamless monitoring through Docker Visualizer.

**Real-time scenario:** John, a DevOps engineer, is tasked with deploying a voting application through multiple microservices. By creating a Docker compose file and deploying it on a manager node in a distributed system, they ensure that each service is efficiently orchestrated and fault-tolerant. 
To monitor the deployment, John integrates Docker Visualizer as a microservice, providing real-time insights. This setup simplifies the deployment process, enhances scalability, and ensures the application runs smoothly in a production environment.Major Tools, Environment Used in This Project:

**Major Tools, Environment Used in This Project:**

- Docker Swarm: The stack is deployed using Docker swarm, a container orchestration tool that allows you to manage a cluster of Docker nodes and deploy services across them.
- Docker Microservices: These are small and independent services that run in separate containers, each handling a specific function within an application. This architecture allows for modular development, scalability, and easier maintenance.
- Swarm Cluster: It is a group of Docker nodes working together as a single system to deploy and manage services. It provides built-in orchestration, ensuring high availability, scalability, and efficient load balancing across containers.
- Docker Compose: It is used to define and manage multi-container Docker applications. It specifies the services, networks, and volumes required for the application.

**High Level Diagram:**

-----------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="838" height="828" alt="image" src="https://github.com/user-attachments/assets/06025b57-7255-48a0-83b6-d5f1a32a9ab9" />

------------------------------------------------------------------------------------------------------------------------------------------------------------

**To Understand the architecture of Voting Application:**

-	Vote Service: A front-end web app in Python which lets you vote between two options. It communicates with the Redis server.
-	Redis Service: A Redis (in-memory database) which collects new votes from the vote service.
-	Worker Service: A .NET worker which consumes votes and stores them in database. It communicates with Redis service for vote collection and db service for vote storage.
-	DB Service: A Postgres database storing the votes backed by a Docker volume.
-	Result Service: A Node.js web app which shows the results of the voting in real time from db.

**High Level Project Tasks:**

- Create an EC2 Instance in AWS Cloud Infrastructure which we will be using as Swarm Manager (Host Machine).
- To create Docker Swarm Manager (Host).
- To create Docker Compose file for Application.
- To update the security group settings of Host Machine (EC2 Instance) to allow the traffic on specific ports on which app services 
(vote and results) are running.
- To verify the deployment of micro-services-application by accessing the application via public-ip of Host machine.
- To Monitor the Deployment, we need to integrate Docker Visualizer as a microservice, to providing real-time insights.
- 





