# REST (Representational State Transfer)
- Representational State Transfer is a software architectural style that was created to guide the design and development of the architecture for the WWW.

# What iss the principle behind the REST?
- The term **representational state transfer** was introduced and defined in 2000 by *Roy Fielding* 
- It means that a server will respond with the representation of a resource(mainly, HTML, XML or JSON) and that resource  will contain some hypermedia links that can be folowed to make the state of the system change. 
- Any such request will in turn receive a representation of resource, and so on.
- **NOTE**: An important consequence is that only ideintifier that needs to be known is the identifier of the first resource, and all other identifiers will be discovered. 
    - This means that those indentifiers that needs to inform the client beforehand and that there can be only **lose coupling** between client and server.
    - **NOTE** : loss coupling means that the in which components are weakly associated with each other, and so changes in one component least affect existence/performance of another component.

# Architectural properties
-  The *REST* architectural style is designed for network-based applications, specifically client-server app. 
- But more thant that, it is designed for internet-scale usage, so the coupling between the user(client) and the server is very loose.
- Constraints of the REST architectural style affect the following architectural properties:
    - performance, in component interactions, which is very important for UIs.
    - scalability, allow the support of large numbers of components and interactions among components.
    - simplicity, which is important for the ease of use of the system.
    - modifiability, which is important for the ability to change the system over time.
    - visibillity of communication between components by service agents.
    - portability, which is important for the ability of components to move to new destinations in order to support load balancing or to recover from failures.
    - reliability, which is important for the ability of the system to recover from failures. 

# Architectural constraints
- The Formal REST constraints are:
    1.Client-server architecture : 
    2. Statelessness : A stateless protocol is a communication protocol in which no session information is retained by the receiver, usually a server.
        - Relevent session data is sent to the receiver by the client in such a way that every packet of information transferred can be understood in isolation, without context information from previous packets in the session.
    3. Chacheablility : Clients and intermediaries can cache responses. Responses must, implicitly or explicitly, define themselves as either cacheable or non-cacheabl to prevetn clients from providing state or inappropriate data in response to further requests.
        - Well-managed caching partially or completely eliminates some client-server interactions, further improving scalability and performance.
    4. Layered system : 

# Miscellenous
1. [Read](https://www.ics.uci.edu/~fielding/pubs/dissertation/software_arch.htm) about RESTful APIs
