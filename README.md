# Phoenixes Cloud Management System 

<img align="right" src="./images/Phoenix_detail_from_Aberdeen_Bestiary.jpg?raw=true" width=
"150">The phoenix is bird from Greek mythology that would live a very long time, but eventually die by bursting into flames. From the ashes, a new bird would be born to start the 500 year cycle anew. 

The goal of this project to build a system that will help build web applications that are automatically resilient to failures and that will scale sensibly when needed.

## Background

In the early days of the internet, if your website needed surge or backup capacity you needed to purchase and maintatin those extra servers. This required a lot of extra expense. These extra physical servers required full time space and maintainence in datacenters and by staff for part-time use. For example, if you ran an e-commerce site like Amazon, you would experience a huge surge in traffic around Christmas. If you did not have these servers available, customers could not purchase from you. Even worse, they might find another online retailer whose infrastructure was able to provide them with service. A lot of effort and expense goes into finding new customers and building brand loyalty. 

Advances in computing and CPU capabilities provided a solution with the ability to virtualize machines. New [CPUs with special instructions](https://en.wikipedia.org/wiki/X86_virtualization)  were added that allowed a single physical machine to run multiple isolated virtual machines in a way that kept the secrets on the machine safe.

## The Art of Software Engineering

There is an art to engineering as well as a science. Computer Science is about constantly pushing the boundaries of what we know and can achive with comptuers. Engineering is different. The goal of engineering is to build reliable systems that will perform for the desired lifetime and within the desired specifications. It is possible to create engineered systems that will run for decades or more. Ask poor enginer who has been asked to maintain a 4GL or COBOL system.

As an example of engineering, the Romans built roads, buildings and aquaducts that still are in use today without access at the time to what we would consider essential tools like algebra, calculus or even what we would generally understand as scientific methods. They did have an excellent understanding of geometry from the Greeks and developed exceptional concrete formulas through trial and error. Some of these formulas have only been finally reproduced in the modern era.

In engineering, the best tools available are to used to build the most reliable system possible that will run for the desired lifetime. 

Traditional software engineering has many similarities with constuction projects. Changes to requirements made early in a project have a much lower cost that grows over time. Making changes on a blueprint are much cheaper, often less than 1%, than making the same changs in later phases of construction. For example, lets say you were building a house and decided to move the location of a toilet. It may be a cosmetic change or it could be due to a bug - like a door not being able to swing properly due to the toilet being too close. If this change is caught early enough, it ight just require some changes to the blueprints. If this was found after the rough plumbing or framing was complete, the cost would likely be much higher but still much more managable than after the tile work, plumbing and carpentry were complete.

### Design, Build, Test, Improve

Part of the art of engineering is to constantly improve designs while verifyin that they meet specifications. This is known by many names like Plan-Do-Check-Act (PDCA).

<img align="center" src="./images/PDCA-Multi-Loop.png" width=
"250">

This will be modified partly for the purposes of this discussion on software engineering:

| Step | Description |
| ---- | ----------- |
| **Design** | |
| **Build** | |
| **Test** | |
| **Improve** | |

### Cheap, Fast, Right: Pick any Two

While there is always a desire to build the perfect system on a shoestring budget, in record time and done perfectly the real world does not work that way. Compromises are nescessary because no resource is infinate. 

A project can be done right, in record time but it will likely be expensive due to the level of expertise and oversight needed. Startup or less critical projects may be able to tolerate a loss of reliability in order to be done quickly and at a reduced cost. If time is not a factor, projects can be done right at low cost as many open source projects have shown that are labors of love. 

Beware, experince shows that getting funding and time for updating a flawed system that works is unlikely if not impossible. 

### The Security CIA Triad: Confidentiality, Integrity and Availablity

<img align="right" src="./images/TRIAD.png?raw=true" width=
"250"> Security is a balance between different elements. There are different methods used to evaluate this balance but the two most common are the parkerian hexad and the CIA triad. We will consider the CIA triad. 

When one of these elements is missing or out of balance we are left with an insecure system. It is tempting to consider the information secure if it is simply encrypted, and this is an important step. If we keep our information safely encrypted and use a hashing function we may be able to sucessfully ensure that it is both confidential and has integrity maintained but availablity would be lost if the key goes missing. This means that we cannot use it when needed. Permanent loss of a key is called cryto shredding and is an effective way to securly destroy data. A less permanent way to lose availability might be a DDoS (Distributed Denial of Service) type attack. A similar failure would be a simple surge in demand that may be entirely innocent like an unexpected popularity of a social media post or sudden surge in demand to a little used government website like one that displays details of emergency messages. The system would need to be able to scale quickly and unexpectedly. Afterwards as the demand wanes, the system can automatically scale back down to minimize costs.

| Triad Element | Description |
| --- | ----------- |
| Confidentiality | The information should only be available to authorized users. |
| Integrity | Information shoule be protected from modification by unauthorized users. |
| Availability | The system should be available when needed. |

With the additon of security as part of the design and operations processes, DevOps becomes DevSecOps. This includes security by design features such as encryption of data at rest, including automatic code scanning tools in the build process, securing of the computing instances using elements of 12 factor design and use of encryption while transmitting data.

Data should be encrypted at rest, in motion and in use. We will attempt to do that in our design by using secure key storage for encryption, using encryption to store and transmit data and by using instances that are as isolated and as secure as possible to process the data.

## The Role of DevOps / DevSecOps

The velocity of software engineering has changed. With the speed of innovation that exists today, taking weeks or months to make changes using traditional waterfall development methodologies means that companies will be producing obsolete solutions by the time they are released while the competition may be innovating daily. For example, Google, Amazon and Netflix are reported to [make thousands of changes and deployments a day](https://services.google.com/fh/files/misc/state-of-devops-2019.pdf).

## Evolution of Cloud Computing

### Physical Servers

In the early days of the internet, you had to purchase a physical server or servers to host your website. 

### Virtual Servers

### Containers

### Serverless Functions

### Service Mesh

## Microservices

### The Goal: A 12 Factor Application

| Factor | Description | Notes |
| ------ | ----------- | ----- |
| I. Codebase | One codebase tracked in revision control, many deploys |  |
| II. Dependencies | Explicitly declare and isolate dependencies |  |
| III. Config | Store config in the environment |  |
| IV. Backing services | Treat backing services as attached resources |  |
| V. Build, release, run | Strictly separate build and run stages |  |
| VI. Processes | Execute the app as one or more stateless processes |  |
| VII. Port binding | Export services via port binding |  |
| VIII. Concurrency | Scale out via the process model |  |
| IX. Disposability | Maximize robustness with fast startup and graceful shutdown |  |
| X. Dev/prod parity | Keep development, staging, and production as similar as possible |  |
| XI. Logs | Treat logs as event streams |  |
| XII. Admin processes | Run admin/management tasks as one-off processes |  |

Within the microserice application, each level or layer should ideal conform to a 12 factor design, if applicable.

Source: [12factor.net](https://12factor.net)

## I. Codebase

All code should be stored and managed using a version control system, such as git or svn. 

## II. Dependencies

## III. Config

## IV. Backing services

## V. Build, release, run

## VI. Processes

## VII. Port binding

## VIII. Concurrency

## IX. Disposability

New instances can be created and terminated at any time to meet the demands of scaling and recovery.

## X. Development / Production parity

## XI. Logs

Any logs should not be stored local to the instance as it could be terminated at any time. By using a logging library the error messages can be redirected to the standard error output and gathered for collection and analysis. 

## XII. Admin processes 


https://services.google.com/fh/files/misc/state-of-devops-2019.pdf
