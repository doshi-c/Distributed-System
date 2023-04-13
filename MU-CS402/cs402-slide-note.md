# Introduction

## Definition, Overview and Foundations

A Distributed System is composed of a collection of <u>independent physically (and geographically) separated computer</u><u>s</u> that do not share physical memory or a clock.

Each computer has its own <u>local memory and clock</u>. The nodes of a distributed system may be heterogeneous. 

Components of the system communicate and coordinate their actions using <u>message passing</u> over Local and Wide Area Networks. 

Components of a distributed system, including processors and networks, may <u>execute concurrently and fail independently.</u> 

## Motivation and Design Approach

The origin and main motivation for this type of system architecture is to <u>facilitate user mobility and sharing of resources</u> at geographically remote locations from the user such as processing power, storage facilities, specialised hardware, software services or data stores. 

A distributed system, consisting of a distributed hardware platform hosting a core operating system, communication suite and other middleware provide the environment in which computation takes place. This computational framework endeavours to make the complexities of the underlying architecture seamless, transparent and convenient to use.

## Benefits

### More Concurrency and Sharing

Substantial portions of the application and its resources may be hosted remotely and accessible concurrently to many remote users through simple interfaces. 

### Higher Performance

The availability of multiple processing nodes means that system load can be shared or balanced across a number of independent components with the objective of increasing throughput and resource efficiency

### Fault Tolerance and Availability

Data and/or processes can be replicated at a number of different sites to compensate for failure of some nodes or to eliminate bottlenecks.

### Scalability

A well-designed system will be able to facilitate more economical phased growth in scale by providing adaptive mechanisms for management and control rather than requiring complete hardware upgrade.

## Design Challenges

### Distributed Coordination and Component Failure

How to manage large-scale concurrent remote operations in the absence of a common global clock and in the presence of random component failure. 

Distributed Algorithms are more complex than centralised ones. What mechanisms do we need to make it easier to write distributed algorithms?

### Program Testing and Correctness

Difficult to repeat a sequence of events for debugging purposes as communication and execution of the application components occur asynchronously at different sites, so other techniques and programming mechanisms must be used to be able to reason about the correctness of algorithms. 

### Ordering and Agreement

Deterministic reasoning requires knowledge about the order in which various events happen and being able to depend on certain properties of mechanisms used. 

Ordering events requires some common representation for time to mark the events or the employment of <u>algorithms for reaching agreement</u> on order among separate components.

### Hardware Complexity and Usability

The principle of transparency is used at many levels in the design of a distributed system to mask implementation details and complexities from the user. 

This ranges from providing the ability to access local and remote devices in a uniform way, independent of location to automated data and process replication, load balancing and recovery.

## Design Characteristics

### Access

Hide differences in data representation and resource access

### Location

Hide physical locations

### Migration & Relocation

Hide dynamic reorganisation and relocation of resources

### Replication

Mask complexities of managing data and or process duplication

### Concurrency

Automatically manage side effects of resourees shared concurrently by multiple users.

### Failure

Overcome system faults maintaining seamless operation

### Openness

Interoperability of software components, reuse of services and the provision of easy access to services and data stores is of key commercial value. 

Openness is a design attribute where well known international standards for protocols and publicly available interfaces are used for communicating with the software components of a distributed system and not proprietary technologies.

### Fast, Reliable Communication Mechanisms

Communication is a central issue for distributed systems as all process interaction and control ultimately depends on this mechanism

Exchanging messages between different components of the system incurs delays due to data propagation, execution of communication protocols and scheduling times of message protocol processes on different hosts. 

Communication delays can lead to inconsistencies arising between different parts of the system at a given instant in time making it difficult to gather global information for decision making and making it difficult to distinguish between what may be a delay and what may be a failure.

### Use of Redundancy - Capable of Tolerating Faults 

Fault tolerance is an important issue for distributed systems. Faults are more likely to occur in distributed systems than centralized ones because of the presence of communication links and a greater number of processing elements, any of which can fail in different ways. 

The system must be capable of preserving the integrity of data and the state of ongoing computation, ideally with only some possible performance degradation.

## Engineering Perspective

During the requirements analysis phase of the development, a number of system properties will be identified. These properties may be classified as functional and non-functional components of the design. 

The functional requirements are further refined and grouped into related functions which are then localised in particular components or modules of the system.

Non-functional requirements are concerned with the quality of the system and are more difficult to attribute to particular parts of the system. These requirements are of a more global nature. 

Examples of such non-functional requirements might be Scalability, Openness, Heterogeneity perhaps in the hardware platform or software language, Resource Sharing, User Mobility and Fault Tolerance.

It is the non-functional requirements of this kind that lead to the adoption of a distributed architecture. 

Remember that centralised systems are simpler and cheaper to build, so preference would be given to a centralised system if a distributed architecture can be avoided. 

However, many of the non-functional requirements listed earlier cannot be achieved properly in a centralised system.

## Summary of Introduction

A heterogeneous distributed architecture with the complexity problems alluded to so far is a potentially very complex and unfriendly platform for a developer.

Many of the underlying problems are overcome with standard design patterns, trusted protocols and technologies and the use of suitable middleware integrating standard components and reliable infrastructure services.

# 2. Distributed Architecture

## Client/Server Architectures

### Two-Tier Client Server Architecture

## Service Oriented Architecture

## Distributed Broker Architecture

## Peer to Peer Architecture

## Event Driven Architecture

## Tuple Space Architecture

# 12. Group Communication, Network Assisted and Overlay Multicast