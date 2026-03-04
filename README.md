# Application Deployment using Docker Swarm and monitoring using Docker Visualizer

**Objective:** The Project is implemented to deploy a scalable, multi-service voting application on a Docker Swarm manager node, ensure efficient orchestration, fault tolerance, and seamless monitoring through Docker Visualizer.

**Real-time Scenario:** John, a DevOps engineer, is tasked with deploying a voting application through multiple microservices. By creating a Docker compose file and deploying it on a manager node in a distributed system, they ensure that each service is efficiently orchestrated and fault-tolerant. 
To monitor the deployment, John integrates Docker Visualizer as a microservice, providing real-time insights. This setup simplifies the deployment process, enhances scalability, and ensures the application runs smoothly in a production environment.

---------------------------------------------------------------------------------------------------------------------------------------------------

## Major Tools, Environment Used in This Project:

- Docker Swarm
- Voting App Microservices (Run under Containers)
- Swarm Cluster
- Docker Compose

-------------------------------------------------------------------------------------------------------------------------------------------------------

## High Level Project Diagram:

<img width="838" height="828" alt="image" src="https://github.com/user-attachments/assets/06025b57-7255-48a0-83b6-d5f1a32a9ab9" />

------------------------------------------------------------------------------------------------------------------------------------------------------------

## To Understand the architecture of Voting Application:

-	Vote Service: A front-end web app in Python which lets you vote between two options. It communicates with the Redis server.
-	Redis Service: A Redis (in-memory database) which collects new votes from the vote service.
-	Worker Service: A .NET worker which consumes votes and stores them in database. It communicates with Redis service for vote collection and db service for vote storage.
-	DB Service: A Postgres database storing the votes backed by a Docker volume.
-	Result Service: A Node.js web app which shows the results of the voting in real time from db.

-----------------------------------------------------------------------------------------------------------------------------------------------------------

## High Level Project Tasks:

- Create an EC2 Instance in AWS Cloud Infrastructure which we will be using as Swarm Manager (Host Machine).
- To create Docker Swarm Manager (Host).
- To create Docker Compose file for Application.
- To update the security group settings of Host Machine (EC2 Instance) to allow the traffic on specific ports on which app services 
(vote and results) are running.
- To verify the deployment of micro-services-application by accessing the application via public-ip of Host machine.
- To Monitor the Deployment, we need to integrate Docker Visualizer as a microservice, to providing real-time insights.

-------------------------------------------------------------------------------------------------------------------------------------------------------------

# Output Result Screenshots:

<img width="948" height="227" alt="image" src="https://github.com/user-attachments/assets/b5d7414d-1174-4d8a-a9ed-c101e0336c2d" />

----------------------------------------------------------------------------------------------------------------------------------------------

<img width="938" height="203" alt="image" src="https://github.com/user-attachments/assets/a0c384f5-08f2-4772-973d-f46cc4713f3a" />

--------------------------------------------------------------------------------------------------------------------------------------------

<img width="928" height="244" alt="image" src="https://github.com/user-attachments/assets/173e9916-9cbd-496a-b8a5-729fa272837c" />

----------------------------------------------------------------------------------------------------------------------------------------

<img width="1009" height="820" alt="image" src="https://github.com/user-attachments/assets/604f59c9-31fd-40d0-9e41-e74ed09fcf23" />

-----------------------------------------------------------------------------------------------------------------------------------------

<img width="943" height="415" alt="image" src="https://github.com/user-attachments/assets/d1e4ef70-ff18-4b68-b572-8acd97a1e7f2" />

-----------------------------------------------------------------------------------------------------------------------------------------------

<img width="941" height="530" alt="image" src="https://github.com/user-attachments/assets/b90f5cff-7124-4169-9149-b1d043d50525" />

--------------------------------------------------------------------------------------------------------------------------------------

On any web browser, hit the URL for vote:

http://54.164.61.71:1000/

Now the Application is accessible, please find below the screenshot:

<img width="787" height="594" alt="image" src="https://github.com/user-attachments/assets/67025be0-aee1-4173-85d2-d531a540b005" />

------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="933" height="550" alt="image" src="https://github.com/user-attachments/assets/92b44be5-995e-496b-a42f-261d2ea63d51" />

-------------------------------------------------------------------------------------------------------------------------------------------------------------

Docker Visualizer page is getting opened with correct Swarm manager private-ip and all the app-services containers details. 

PFB the screenshot:

<img width="950" height="586" alt="image" src="https://github.com/user-attachments/assets/6805a8fb-611e-4224-a418-46c75c87517f" />

----------------------------------------------------------------------------------------------------------------------------------------

**The Deployment of multi-service voting application on a Swarm manager node has been done successfully using Stack deploy and docker-compose file.
The Docker Visualizer has been integrated as microservice to monitor the deployment and provide real-time insights.
Also, the security group rules were set correctly at machine level.
As a result, the micro-services (vote, redis, worker, db, result) are communicating properly and the website is being accessible on the browser with all the data populating correctly after the voting is done.**


