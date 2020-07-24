# Select the Appropriate Forwarding Mode

When the Anti-DDoS Pro configures forwarding policy, multiple flexible forwarding modes are available to meet different requirements for business scenarios.
The selection of the forwarding mode is applicable to the case where multiple servers are available at the backend, and the Load Balancer is carried out by different policies.

## Specification of Forwarding Rules

- Non-web service rules support: round robin, weighted round robin, and source IP hash
- Web Service rules support: round robin, and weighted round robin

## Forwarding Mode Interpretation
1. Round robin
    - Definition: The request is sent in order to the server at the backend.
    - It treats each server at the backend in a balanced manner regardless of the number of actual connections to the server and the current system load.
  
2. Weighted round robin
    - Definition: The request will be assigned to the backend server based on the order of weight ratio of the source station configuration. The higher the weight value, the higher the number of times the server will go through round robin.　　
    - Because different backend servers may have differences between their configuration of the machine and the load of their current system, therefore their stress tolerance also varies. To configure high- and low-load machines with higher weights to handle more requests; Assign low-configuration high-load machines with lower weights to lower their system loads.
  
3. Source IP hash
    - Definition: The same request is always mapped to the same backend server if the backend server remains the same.
    - The algorithm of the source IP hash is to obtain the client IP address, then get a value by hash function calculation and use the value for modulo operation of the size of the server list, of which the result is the serial number of the server the customer is to visit.
