# Docker
## Before docker
## Monolithic Application
 Monolithic Application describes single tired application. Here all the functionalities like user-interface, code and data access are combined into a single program from a single platform.
![Monolithic Architecture](https://github.com/javahometech/Docker/blob/master/images/Monolithic.png "Monolithic")
#### Drawbacks of Monolithic Application
- Here we wanna do any operation like search we have to run all the application so the performance of monolithic application is low
- Developers take lots of time to understand the system because it’s big
- Scaling Problem, if you wanna scale only specific module in application it is not feasible
- Deployment challenges, It is highly risky to deploy monolithic applications deployment time is also more
- We can’t use different technologies in monolithic. For example in your application you wanna use elasticsearch, mongodb and relational db for scaling your app it is very difficult to use multiple technologies in single application
- on each update you have to redeploy all the application
- Another problem with monolithic applications is reliability. Bug in any module (e.g. memory leak) can potentially bring down the entire process

### Service Oriented Application:
A Service oriented architecture is essentially a collection of services. These services communicate with each
other. The communication can involve either simple data passing or it could involve two or more services coordinating some activity. Some means of connecting services to each other needed.
- Monolithic Application is divided into multiple projects
- Every application project can have its own application stack
- The services communicate using webservices (RESTful/SOAP)

### Microservice Architecture:
-	It is fine grained version of SOA
- Every microservice must be small enough such that it should be handled by 2 developers
- It's drastically improve the developers productivity
- you can use different technologies in different microservices
- we can scale a specfic service
- If a specfic service is down, Even though customers can use other services, It not make your whole application down
- The challenges with microservice is we get too many services to deploy and maintain

## Docker
#### What is Docker?
- Docker is tool to create, deploy and run applications by using containers
- Here the application is packaged with all the libraries and other dependencies which are rquired to run application
#### Different types of Docker
Docker is available in two editions:
- Community Edition(CE)
- Enterprise Edition(EE)

**Community Edition:** It is for individual developers and small teams looking to get started with docker and
experimenting with container based apps

**Enterprise Edition:** It is for enterprise development and IT teams who build, ship and run bussiness critical applications in productions

#### What are the benefits of Docker?
**Rapid application deployment:** containers include the minimal runtime requirements of the application, reducing their size and allowing them to be deployed quickly

**Portability:** an application and all its dependencies can be bundled into a single container that is independent from the host version of Linux kernel, platform distribution This container can be transferred to another machine that runs **Docker**, and executed there without compatibility issues

**Version and Component reuse:**  you can track successive versions of a container, inspect differences, or roll-back to previous versions. Containers reuse components from the preceding layers, which makes them noticeably lightweight

**Sharing:** you can use a remote repository to share your images with others. it is also possible to configure your own private repository.

**lightweight and minimal overhead:** Docker images are very small, which facilitates rapid delivery and reduce the time to deploy new application containers

**Simplified maintenance:**  Docker reduces effort and risk of problems with application dependencies.

## VMS vs Docker

![VMS vs Docker](https://github.com/javahometech/Docker/blob/master/images/vmdocker.jpg "vmdocker")

**VM:** A virtual machine (VM) is a software program or operating system that not only exhibits the behavior of a separate computer, but is also capable of performing tasks such as running applications and programs like a separate computer

- Every VM has its own OS, That consumes lot of resources
- VM takes minutes to start
- Applications on VMs are not portable
- It allocates required memory and Heavyweight
- It is Fully isolated and Hence more secured

**Docker container:** Docker container is a runtime of Docker image. With containers, instead of virtulizing the underlaying computers like a virtual machine(VM), just the OS is virtualized

Containers sit on top of a physical server and its host OS — typically Linux or Windows. Each container shares the host OS kernel and, usually, the binaries and libraries, too.

-	Containers will not have its own OS, It consumes very less compute resources.
- containers start time within seconds.
-	Applications deploy on container are highly portable your application and its dependencies are bundled together when you move to different server it will definitely works
-	Application running on docker performs better than application on VM
- Containers are process-level isolation and less secured compared to VM


### Architecture of Docker
