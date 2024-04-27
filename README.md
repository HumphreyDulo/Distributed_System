# Load Balancer Analysis 

---

## Introduction

In this project, we conduct an analysis of a load balancer implemented using consistent hashing. 
---

## Assumptions and Design Choices

### Assumptions
1. **Uniform Distribution**: We assume that incoming requests are uniformly distributed across the request space.
2. **Fault Tolerance**: We assume that the load balancer can handle server failures and spawn new instances as needed.
3. **Scalability**: We assume that the load balancer can scale effectively with an increase in the number of server containers.
4. **Hash Function**: We assume that the hash function used for request mapping produces evenly distributed hash values.

### Design Choices
1. **Consistent Hashing**: We chose consistent hashing for load balancing due to its ability to minimize disruption when servers are added or removed.
2. **Virtual Server Mapping**: We implemented virtual server mapping to improve load distribution by introducing multiple virtual servers per physical server.
3. **Experimentation Approach**: We opted for a systematic experimentation approach, varying parameters such as the number of server containers to analyze their impact on load balancing performance.

---

## Tasks

1. **1: Distribution of Requests**
   - Ability to send requests to /home and /heartbeat and receive Json response
   - [Example Image](./images/home.png)
   - [Example Image](./images/heartbeat.png)

2. **2: Hash Function**
   - This block of code defines the hash functions and implements the Consistent Hashing class, which is responsible for mapping requests to server containers based on their hash values and maintaining the virtual server mappings to ensure balanced load distribution.

3. **3: Load Balancer Scalability**
   - **Server replicas**: request the replica endpoint to view number of replica servers.
   - **Observations**:
   - [Example Image](./images/replicas.png)
   
   - **Add new server instance**:Endpoint /add will add new server instances in the load balancer
   - [Example Image](./images/add.png)


4. **4: Analysis**
   - **Description**: Test the load balancer's scalability by varying the number of server containers.
   - [Example Image](./images/n=3.png)
   - [Example Image](./images/n=2-6.png)
   - **Observations**: The server load is more likely to distributed when there are a greater number of server containers.
   - N=2-6[Example Image](./images/Graph_n=2-6.png)
   - [Example Image](./images/Graph_n=3.png)
   - 
   - **Response to server failure**: In case of server failure, a new instance should be created to handle the load. 
   - Trigger failure using the server failure endpoint
   - [Example Image](./images/serverfailure1.png)
   - [Example Image](./images/serverfailure2.png)
---

## Conclusion


