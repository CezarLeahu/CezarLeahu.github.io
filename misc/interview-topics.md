---
date: 2021-06-01
title: Interview Questions & Topics
permalink: misc/interview-topics
---

Hints & Tips
===
* Research what the company does, what kind of product do they build, how it works overall, who are the company's (or the project's) clients? etc.
* Anything in your CV can become an interview subject.
  - This doesn't mean you should know every technology subject in-depth, but you should be able to explain how you've made use of that technology (in your past projects).
* You will be asked to describe at least one of your past projects (usually the most recent one)
  - Describe not only the project(s), but maybe also what the company does/sells & to whom it sells its product (typical
    clients - the world? a specific geographical area? large organizations? etc.)
  - In the context of the company and overall product, what does your project/feature handle? What is its purpose?
  - What technologies have been used in the project? Why/How have they been used?
* You might be asked to actually write some code - usually something simple (short) like a search, a sort, or some linked-list work.


Potential Questions
===
* A thing you're really good at? One of your strong points? Maybe two?
* You weakness(es) (work-related)? Something you're uncomfortable with? Maybe a technology/activity you haven't had much practice with?
* A feature/project you've worked on and you're quite proud of? Maybe one where you've learned a lot implementing it?
* Anything outside your main area of expertise or your daily routine that you also enjoy working with or you're interested in - e.g. maybe another programming language, maybe UI (web/mobile) work, maybe scripting work, machine learning, CI work, Helm/Terraform deployment work, embedded system, any topic from faculty that you've liked, etc.
* Conflicts you've had and how you've resolved them?
* Any hobby you enjoy outside work?


Technical Questions and Topics
===

## OOP
* Basic concepts: encapsulation, abstraction, inheritance, polymorphism
* SOLID (whatever that means)
* Design Patterns (the classic GoF patterns) - it's not enough to be able to describe these patterns, but you must also be able to recognize these patterns from code, UML diagram or just from description

## Algorithms
* (!) ALGORITHM COMPLEXITY - for all algorithms and data structures
* Common search & sorting algorithms
* Data Structures
  - Dictionaries: how hashtables works, how important is the hash function, etc.
  - Linked lists, static lists
  - Trees, Binary Trees, Red-Black trees
  - Heap structure: what's so special about it? why is it also called a Priority queue?
* Dijkstra

## Programming
* Static typing vs dynamic typing
* Strong typing vs weak typing
* Categories of programming languages: compiled (C, C++, Go, Rust), managed (Java, C#.NET), interpreted (PHP, Python,
  Pearl, Bash)
* Why can Java be considered both a compiled and an interpreted language?
* Multithreading
  - race conditions, deadlocks, producer-consumer problem, starvation
  - mutexes & locks vs semaphores
  - multithreding with *Message Passing* vs mutithreading with *Shared Memory*
* Basic RegEx
* Types of Serialization: text & binary
* TCP/IP protocol stack
  - layers: Data Link (MAC), Network (IP), Transport (TCP, UDP), Application (HTTP, FTP, SMTP, DNS, etc.)
  - common protocols 
  - TCP vs UDP
* coding questions:
  - code optimization:
    + for speed
    + for memory
  - identify a bug in a piece of code
  - identify a design pattern in a piece of code
  - calculate the O complexity of a code routine

## Java
* Sets & Maps (dictionaries, hashes):
  - common implementations and characteristics: HashTable, HashSet, HashMap, 
  - what happens if you don't implement the `hashCode()` method on the elements you insert into a Set/Map? How will the
    hash structure look like (in-memory)?
  - LinkedHashMap vs TreeMap - order of elements?
  - When to use HashMap/HashSet, when to use TreeMap/TreeSet, when to use LinkedHashMap/LinkedHashSet
* How can you do Message-passing multithreading in Java?
  - BlockingQueues
  - wait(), notify(), notifyAll()
* final, finally, finalize
* try-with-resources & the AutoCloseable interface
* basic knowledge of AOP
* synchronized methods vs code blocks synchronized on a specific object (potential disadvantages with the former?)
* Synchronized collections
* Concurrent collections (How do they work? What do you need to be aware of when using them?)
* ThreadLocal variables in Java. How would you implement a ThreadLocal type from scratch?
* Java 8+ 
  - streams
  - default methods in interfaces
  - Optional
* Nested classes
  - static nested classes
* why it's important to implement the `equals()` and `hashCode()` methods for POJOs & DTOs?
* Project Lombook? (& its annotations @Data, @Slf4j)
* what happens if you call `System.exit()` in a _try-catch-finally_ block?
* JVM/Java Garbage Collection (Mark-and-Sweep algorithm)
* JVM string cache
* Strong, Soft, Weak & Phantom references in Java (what they can be used for - cache implementations, control over
  object cleanup)
* JVM Profiling/monitoring (e.g. with JConsole)
  
## JEE
* What is JEE? Who implements the JEE specification?
* What is an Application Server?
  - JEE implementation
  - Can it be described as a JVM OS?
  - Examples of fully-fledged JEE Application Servers: GlassFish, JBoss/Wildfly, WebSphere
  - What are Web Containers (Servlet Container)?
    - Partial JEE implementations (only implement Java Servlet APIs)
    - Examples: Tomcat (Apache), Undertow (JBoss/RedHat), Jetty (Eclipse/IBM)
    - Why they're popular with Spring applications? Spring already provides its own Bean containers & APIs. A spring
      application often doesn't need/use most of what a JEE Application Server has to offer
* What is a Servlet?
* What are Servlet Filters? What they can be used for (e.g. Authentication filter)
  - filters are organised in a Chain-of-responsibility pattern

## Spring
* What is the Spring Context?
* Spring Beans
  - what they are - instances of objects, usually Proxies/Decorators to the actual bean class type
  - scope: Singleton vs Prototype scopes
  - declaration:
    + in application-context XML files
    + with the @Bean annotation in @Configuration classes
    + @Component/@Repository/@Service annotations and Spring classpath scanning
* Spring Dependency Injection (Inversion of Control) - basically the @Autowired annotation
* Spring Data Repositories (JDBC, JPA, LDAP, Cassandra, MongoDB, Redis, REST, Elasticsearch, etc.)
  - high-level abstractions over the actual implementations
* REST with Spring (Controllers)
* Spring AOP
* SpringBoot
  - purpose, advantages

## DBs
* ACID: atomicity, consistency, isolation, durability & what each of them means ([https://en.wikipedia.org/wiki/ACID](https://en.wikipedia.org/wiki/ACID#Characteristics))
* DDL vs DML instructions
* constraints, types of constraints,
* what's an index; advantages & disadvantages
* primary-keys, foreign-keys, composite primary-keys, cascades, triggers
* Basic SQL, basic PL/SQL (& what DBs support PL/SQL)
* transactions with SQL: SAVEPOINT, ROLLBACK TO, ROLLBACK, COMMIT
* table partitioning, DB sharding
* DB Server replication (master/read-replicas)
* Two-phase commit protocol (distributed transactions)
* ORMs? You might be asked to model a relationship between two or more model Entity classes in Java into SQL Tables (what are the resulting tables)
* NoSQL DBs - what they can offer, what they don't ensure (e.g. ACID), some examples (Cassandra, MongoDB)

## Caches
* Hibernate L1 & L2 caches
* Distributed caches
  - when to use them, where to use them (e.g. for scalable services; for reducing load on the DB server)
  - examples: Redis, Memcache, Hazelcast

## Messaging
* JMS
* Kafka
  - general overview: events, streams, topics
  - topic partitioning & linear scalability/performance
  - event-driven systems / event-driven architecture

## Web
* DNS protocol
* HTTP protocol
  - type of protocol (stateless, synchronious request-response)
  - how do the messages look like (what they contain)
  - HTTP methods
  - REST services and HTTP method mapping to CRUD operations
    - what [method] do you use to retrieve a resource
    - what do you use to create a resource
    - what do you use to alter a resource (or a sub-resource)
    - what do you use to replace an existing resource
    - can you alter a resource through the GET method?
      - No? Is that something enforced by the protocol or just a convention?
    - parameters (path, query, header)
    - HTTP 2
    - HTTP 3
* GraphQL - pupose, main goal
* What is a Webhook, how you set it up, how it works?
* What is a Websocket, what is it useful for?
* SWAGGER & OpenAPI & how you generate code from the swagger specs? How you use the endpoint, etc.
* Feign clients, RESTEasy, etc.
* Stateless vs Stateful protocols
* Stateless vs Stateful applications
* Cookies & Session (and how they work with a Stateless protocol as HTTP)
* Basic (or advanced) HTML, CSS, JS
* Single-Page-Applications:
  - How do they work (an overview)?
  - How they compare with a classic application (where is the HTML rendered, how cookie/session mechanism works, how AJAX queries are used, etc.)
  - How do you mimic a *Session*/*Session variables* in a single-page application?
  - JWT Authentication
  - How do they handle navigation
  - Popular frameworks: ReactJS, Vue, BackboneCSS,
* NodeJS
  - what it is? how it came to be?
  - what is npm?
  - how it's helpful for building SPAs
  - Server-side NodeJS applications
* HTTP CORS - basic rules & headers
* OAUTH 2
* What ensures encryption of communication between clients (web browsers) and servers? (HTTPS)
* HTTPS/SSL handshake
* Cross-site attacks (XSS, CSRF)
* OWASP Top 10

## Mobile
* iOS & Android
* Cross-platform frameworks:
  - ReactNative (JavaScript-based)
  - Flutter (actually native - i.e. compiled)

## Cloud & Co
* IaaS vs PaaS vs FaaS vs SaaS
* Containers
  - Docker
  - containers vs VMs
* Container orchestration
  - Kubernetes, OpenShift, Helm
* Cloud provisioning
  - Terraform
* Serverless Architecture (Cloud Functions, e.g. AWS "Lambdas")
* AWS:
  - provisioning: CloudFormation
  - virtual networking: VPC
  - VMs: EC2
  - object storage: S3
  - DNS: Route53
  - API Gateway
  - DB: RDS, DynamoDB
  - access control: IAM

## Enterprise applications and patterns
* Enterprise Integration Patterns - [https://www.enterpriseintegrationpatterns.com/](https://www.enterpriseintegrationpatterns.com/patterns/messaging/toc.html)
  - synchronous vs. asynchronous communication
  - message queues
    - types
    - communication patterns
    - advantages vs disadvantages
* DDD, BDD...
  - what is a "bounded context"?
  - Onion/Hexagonal/Clean Architecture
  - Vertical Slice/Comands&Queries/Circular Architecture
  - Event Sourcing


Methodologies
===
* Agile
  - Scrum
  - Kanban
  - Extreme Programming (i.e. "The Scrum that actually works"), pair programming
  - advantages over Waterfall
  - Epics, Stories, Tasks
    + What is an "Acceptance Criteria"
    + What is a "Definition of Done"


Resources
===
* Programmer Competency Matrix, by Sijin Joseph: [https://sijinjoseph.com/programmer-competency-matrix/](https://sijinjoseph.com/programmer-competency-matrix/)
* Various programming questions: [http://www.ardendertat.com/2012/01/09/programming-interview-questions/](http://www.ardendertat.com/2012/01/09/programming-interview-questions/)
* DDD-related: [http://www.slideshare.net/jeppec/agile-ddd-cqrs](http://www.slideshare.net/jeppec/agile-ddd-cqrs)

