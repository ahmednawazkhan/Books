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

### Chapter 5: OOP
#### Polymorphism

Polymorphism is an application of pointers to functions. So OOP does not provide something new in this regard as the concept exists before it but for sure it provides safety and makes polymorphism trivial

* Dynamic Polymorphism
  * Run-Time polymorphism
  * Dynamic binding
  * Run-Time binding
  * Late binding
  * Method overriding
* Static Polymorphism
  * Compile-Time polymorphism
  * Static binding
  * Compile-Time binding
  * Early binding
  * Method overloading

##### Dependency Inversion

Without polymorphism a typical program will have a calling tree where High level functions calls mid level functions that ultimately call lower level functions creating a tree. So source code dependencies ( main function has a dependency of Hight level component/class ) follows the flow of control. And programer had to use `import` in java and `include` in C to call that function from `main`. So flow of control was dictated by the behaviour of the system and source code dependencies were dictated by flow of control

In an example where `HL1` a module, calls function `F()` of `ML1` another module through an interface is source code contrivance. At runtime that interface will not exist. and `HL1` simply calls `F()` on `ML1`.

:::image type="content" source="dependency-inversion.png" alt-text="Dependency Inversion":::

### Chapter 18: Boundry Anatomy
<ins>
When a high-level client needs to invoke a lower-level service, dynamic polymorphism is used to invert the dependency against the flow of control. The runtime dependency opposes the compile-time dependency
</ins>

###