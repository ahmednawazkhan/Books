# Clean Architecture

## By Robert Cecil Martin


### Chapter 15: What is Architecture
### Chapter 16: Independence
### Chapter 17: Boundries: Drawing Lines


An application should be architected keeping in mind development, deployment, operations and maintaince (costly). Operations being the least important as it can be achieved by increasing the hardware

The goal of the architect is to create a shape for the system that recognizes policy as the most essential element of the system while making the details irrelevant to that policy

Beware of TRUE DUPLICATION vs FALSE DUPLICATION when it comes to sharing code. Change code for TRUE DUPLICATION where a change in one component should be reflected in all the components. A FALSE DUPLICATION between 2 components may lead to 2 different timelines when u look at them after a couple of years


#### Decoupling modes
* Source code level
* Deployment level
* Service level ( microservices )

A good architecture will allow a system to be born as a monolith, deployed in a single file, but then to grow into a set of independently deployable units, and then all the way to independent services and/or micro-services

Decoupling mode of a system is one of those things that is likely to change with time, and a good architect foresees and appropriately facilitates those changes
