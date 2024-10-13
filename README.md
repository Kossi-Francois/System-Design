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

    3. Network
        1. Proxies: forward and reverse proxies
            Forward proxies are used to shield clients from external networks while Reverse proxy acts as a frontend Facade for backend Servers

            Users  {mobile, web, ..} → Forward/Outbound Proxy (client side) { Client Anonymity and Privacy,  Content Filtering and Caching, Security and Access Control} → Internet → Servers

            Users  {mobile, web, ..} → Internet → Reverse/Inbound Proxy(server side) { Server Anonymity, Load Balancing and Traffic Distribution, Caching, SSL Termination and Encryption, Content Delivery and Optimization } → Servers


    4. Scaling: Horizontal scaling vs Vertical Scaling


    | Left aligned Content      | Horizontal scaling(scale-out)                                                                      | Vertical Scaling(scale-up) |
    | :------------------------ | :-----------------------------------------------------------------------------------------:        | --------------------: |
    | How to                    | add more nodes, machines or servers                                                                | Increase processing speed, power and capacity |
    | Load balancing            | Requires the use of load balancers to distribute incoming requests across multiple servers         | Do not need Load Balancing     |
    | Maximum Scalability       | Achieve higher levels of scalability as the number of nodes can be increased almost indefinitely   | Limited by the maximum physical capacity of a single machine/server/node|
    | Architecture Preference   | distributed systems, more flexible, robust to failure                                              | monolithic systems |
    | Implementation Complexity | More complex, may introduce more overhead or communication delays                                  | Easier and less complex to implement        |
    | Workload Handling         | can handle unpredictable or varying loads, ressources can dynamically be allocated                 | steady, predictable and consistent workload |
 

















3. System design Tools

    - [excalidraw]( https://excalidraw.com/ )
    - [draw.io](http://draw.io/)



## Exemples of System Design QA

1. [Netflix System Design]()