# Phoenixes Cloud Management System 
!(./images/Phoenix_detail_from_Aberdeen_Bestiary.jpg?raw=true)

The phoenix is bird from Greek mythology that would live a very long time, but eventually die by bursting into flames. From the ashes, a new bird would be born to start the 500 year cycle anew. 


The goal of this project to build a system that will help build web applications that are automatically resilient to failures and that will scale sensibly when needed.

## Background

In the early days of the internet, if your website needed surge or backup capacity you needed to purchase and maintatin those extra servers. This required a lot of extra expense. These extra physical servers required full time space and maintainence in datacenters and by staff for part-time use. For example, if you ran an e-commerce site like Amazon, you would experience a huge surge in traffic around Christmas. If you did not have these servers available, customers could not purchase from you. Even worse, they might find another online retailer whose infrastructure was able to provide them with service. A lot of effort and expense goes into finding new customers and building brand loyalty. 

Advances in computing and CPU capabilities provided a solution with the ability to virtualize machines. New [CPUs with special instructions](https://en.wikipedia.org/wiki/X86_virtualization)  were added that allowed a single physical machine to run multiple isolated virtual machines in a way that kept the secrets on the machine safe.

## The Art of Software Engineering

There is an art to engineering as well as a science. Computer Science is about constantly pushing the boundaries of what we know and can achive with comptuers. Engineering is different. The goal of engineering is to build reliable systems that will perform for the desired lifetime within the desired specifications.

For example, the Romans built roads, buildings and aquaducts that still are in use today without access to what we would consider essential tools like algebra, calculus or even what we would generally understand as scientific methods. They did have an excellent understanding of geometry from the Greeks 

In engineering, the best tools available are to used to build the most reliable system possible that will run for the desired lifetime. 


### Cheap, Fast, Right: Pick any Two

While there is always a desire to build the perfect system on a shoestring budget, in record time and done perfectly the real world does not work that way. Compromises are nescessary because no resource is infinate. 

A project can be done right, in record time but it will likely be expensive due to the level of expertise and oversight needed. Startup or less critical projects may be able to tolerate a loss of reliability in order to be done quickly and at a reduced cost. If time is not a factor, projects can be done right at low cost as many open source projects have shown that are labors of love. 

Beware, experince shows that getting funding and time for updating a flawed system that works is unlikely if not impossible. 

### The Security CIA Triad: Confidentiality, Integrity and Availablity

Security is a balance

## Evolution of Cloud Computing



### The Goal: 12 Factor Application

| Facctor | Description | Notes |
| ----- | ---------- | ------------------- |
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

Source: ![12factor.net](https://12factor.net)

## The Role of DevOps

Traditional software engineering has many similarities with constuction projects. For example, changes to requirements made early in a project have a much lower cost that grows over time. Making changes on a blueprint are much cheaper, often less than 1%, than later phases of construction. For example, lets say you were building a house and decided to move the location of a toilet. It may be a cosmetic change or it could be due to a bug - like a door not being able to swing properly due to the toilet being too close. If this change is caught early enough, it ight just require some changes to the blueprints. If this was found after the rough plumbing or framing was complete, the cost would likely be much higher but still much more managable than after the tile work, plumbing and carpentry were complete.

### Design, Build, Test, Improve

