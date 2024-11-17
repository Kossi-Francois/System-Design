# System-Design

## General information

1. What is Systems Design ?

    System design is the process of establishing a system's architecture, components, modules, interfaces, and data in order to meet specific requirements. It entails converting user needs into a precise blueprint that will guide the implementation process. The goal is to develop a well-organized and efficient structure that serves its intended function while taking into account scalability, maintainability, and performance. 

2. How to Answer a System Design Question ?

    1. Clarify requirements
        1. Functional requirements:  define Features for users.
            1. System Design Diagram, Architecture
            2. Don’t make any assumption about the problem

        2. Non Functional requirements: Engineering limits:  ask about scale, throughputs, security, privacy, web and mobile support.
            1. Outcome: Choices and N° of resource, capacity estimation

    2. Define system APIs - towards parts that are out of scope.It can be towards the front-end or from 3rd party services.

    ---

    3. Network
        1. Proxies: forward and reverse proxies
            Forward proxies are used to shield clients from external networks while Reverse proxy acts as a frontend Facade for backend Servers

            - Users  {mobile, web, ..} → Forward/Outbound Proxy (client side) { Client Anonymity and Privacy,  Content Filtering and Caching, Security and Access Control} → Internet → Servers

            - Users  {mobile, web, ..} → Internet → Reverse/Inbound Proxy(server side) { Server Anonymity, Load Balancing and Traffic Distribution, Caching, SSL Termination and Encryption, Content Delivery and Optimization } → Servers


                ===========================================
       
        2. API Gateway and Load Balancer

            - API Gateway: a middleware between clients and backend providing a centralized entry point for accessing various endpoints and functionalities
                - API Management: authentication, authorization, rate limiting, and caching
                - Protocol Transformation: can handle different protocols or message formats
                - Routing and Versioning: requests routing based on predefined rules/config
                - Analytics and Monitoring: API usage, performance metrics, and error tracking
            
            
            - Load Balancer: distributing incoming requests across multiple backend, optimize resource
                - Traffic Distribution: across multiple nodes based on predefined algorithms such as round-robin, least connections, or weighted distribution
                - High Availability: routing traffic away from unhealthy/overloaded servers; health checks to monitor node status and dynamically adjust traffic routing
                - Session Persistence: sticky session, ensuring that subsequent requests from the same client are directed to the same backend server.
                - SSL Termination: can offload SSL/TLS encryption and decryption
                - Algo: 
            	

                     ===========================================
                  
        3. APIs
            - REST (Representational State Transfer)
            - RPC (Remote Procedure Call)
            - GraphQL

    ---

    4. Scaling: Horizontal scaling vs Vertical Scaling


    | Left aligned Content      | Horizontal scaling(scale-out)                                                                      | Vertical Scaling(scale-up) |
    | :------------------------ | :-----------------------------------------------------------------------------------------:        | --------------------: |
    | How to                    | add more nodes, machines or servers                                                                | Increase processing speed, power and capacity |
    | Load balancing            | Requires the use of load balancers to distribute incoming requests across multiple servers         | Do not need Load Balancing     |
    | Maximum Scalability       | Achieve higher levels of scalability as the number of nodes can be increased almost indefinitely   | Limited by the maximum physical capacity of a single machine/server/node|
    | Architecture Preference   | distributed systems, more flexible, robust to failure                                              | monolithic systems |
    | Implementation Complexity | More complex, may introduce more overhead or communication delays                                  | Easier and less complex to implement        |
    | Workload Handling         | can handle unpredictable or varying loads, ressources can dynamically be allocated                 | steady, predictable and consistent workload |
 


    ---

   5. Estimate and calculate

        - Scale - how many concurrent users the system will support.
        - Storage - how much space do we need in case we store data.
        - Network bandwidth 
        - Bottlenecks
        - Database connections or throughput
        - Hard disk reading/writing
        - Utility that encrypts/decrypts data at high volumes
        - Loadbalancer
        - API call to 3rd party service that's rate throttled


    	- Approximation
             - Average: 1 million == 1e6 (if N° user ⇒ X N° transactions per user)
    			- ~42k per hour
                - ~700 per minute
                - ~12 per second
        
            - Peak: 10 % of 1 million = 100 k per Hour => 100 K / 30s
        		- ~1m/day app @ 10% peak for 1 hour: 100k rule = 30/second.
                - ~1m/day app @ 30% peak for 1 hour: 100k rule = 90/second.




    ---

    
    6. Design Data model
        - Identify entities and interactions in the system.

          | Logical Entities          | Tangible Entities                           | 
          | :------------------------ | :------------------------------------------:|
          | Data                      | Text, Image, Video, files, ...              |
          | Database                  | MongoDB, MySQL, Cassandra                   |
          | Applications              | Java, Golang, Python, React,                |
          | Cache                     | Redis, MemeCache                            |
          | Infra                     | Cloud(AWS, GCP, Azure) , On-Premises        |
          | Communication             | APIs, RPCs, Messages                        |
          

























2. System design Tools

    - [excalidraw]( https://excalidraw.com/ )
    - [draw.io](http://draw.io/)



## Exemples of System Design QA

1. [Netflix System Design]()
