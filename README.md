# Load Balancer Analysis Readme

---

## Introduction

In this project, we conduct an analysis of a load balancer implemented using consistent hashing. Our goal is to understand the load balancing performance and explore potential improvements to the algorithm.

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
3. **Experimentation Approach**: We opted for a systematic experimentation approach, varying parameters such as the number of server containers and hash functions to analyze their impact on load balancing performance.

---

## Tasks

1. **Experiment 1: Distribution of Requests**
   - **Description**: Send a fixed number of requests to the load balancer and observe the distribution among server containers.
   - **Observations**: Analyze the distribution patterns and assess the load balancing effectiveness.
   - **Points for Images**: Include bar charts showing the request distribution among server containers. [Example Image](./images/distribution_chart.png)

2. **Experiment 2: Hash Function Modification**
   - **Description**: Modify the hash function used for request mapping and test different alternatives.
   - **Observations**: Compare the load balancing performance with different hash functions and evaluate their effectiveness.
   - **Points for Images**: Include comparison charts showing the performance with different hash functions. [Example Image](./images/hash_function_comparison.png)

3. **Experiment 3: Load Balancer Scalability**
   - **Description**: Test the load balancer's scalability by varying the number of server containers.
   - **Observations**: Analyze the average load of servers as the number of containers increases and assess scalability.
   - **Points for Images**: Include line charts showing the average load of servers against the number of server containers. [Example Image](./images/scalability_analysis.png)

4. **Experiment 4: Fault Tolerance and Recovery**
   - **Description**: Simulate server failure and observe the load balancer's response.
   - **Observations**: Assess the load balancer's ability to handle failures and recover by spawning new instances.
   - **Points for Images**: Include screenshots or logs demonstrating the load balancer's behavior during failure and recovery. [Example Image](./images/failure_recovery_logs.png)

---

## Conclusion

In conclusion, this analysis provides insights into the load balancing performance of the consistent hashing-based load balancer. By systematically testing different scenarios and parameters, we gain a better understanding of the algorithm's strengths and weaknesses. The findings from these experiments can inform future improvements and optimizations to enhance the load balancer's effectiveness in real-world scenarios.
