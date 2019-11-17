# Openshift - Lecutre by IBM


## What is it?
- Official name: Openshift container platform
- It is a container platform
    - **What are containers?**
        - Containers are easy to pass around, rather than having documentation 
        - This allows project environment to be preserved
            - includes programming language used
            - includes physical components
        - lighterweight than VMs
            - single container kernel
        - Multiple containers can be deployed within a single machine: they have a shared OS
        - Containers are optimized for agility as compared to VMs which are optimized for stability
            - IP Ops handles the Container host + infra
            - Developers handle Application and OS dependencies
            - Therefore, container development only dependent on developers
        - **!IMPORTANT!** Note that containers do not have access to filestorage. Once the ports are evicted, temporary file storage will be destroyed. (Upon restart, all data is gone)
        - VMs are not as easily portable as containers
            - with RHEL Containers + RHEL Host -> Guaranteed portability across machines
- Provides with some innate software support:
    - Jenkins (for automation)
    - enterprise grade security
- "Container as a service" (CaaS)
    - Deploy the container itself
    - base OS redhat enterprise linux
- cri-o is the runtime interface
    - lightweight, OCI-compliant container runtime
- **What are pods?**
    - Is all about YAMLs: will be transferred into objects from there
    - **How do pods interact with each other?**
        - *Wtf is kuberpip*
    - **Openshift SDN network rules**
        - Flat network (all pods can talk to each other)

- **Integrated Container registry**
- *what is this?*
    - Through Web, CLI, IDE, and API
    - This is on the physical machine layer
    - *How does this work?*
        - 1 master, multiple nodes
            - Master provides API/Authentication
            - Contains data store
            - Contains scheduler
            - Health and scaling
    - *How does scheduling work?*
        - Does deployment by talking to the master datastore (key-value pairing, non-persistent data storage)

## How can it be used? (Use cases)
- Source-to-image (S2I) 
    - Allows the developer to interact with openshift by pulling source code from github and the rest of the deployment is done automatically


## How is it relevant to me?
- Can be used for microservices and exposing endpoints 
- **Integration with VSCODE**
    - Kubernetes Extension
        - kloud-knative
- OpenShift container CodeReady Workspaces
    - Container workspaces would act as a web-based IDE for working on the source code
- **Quarkus**
    - Java JIT: Just In Time converts code to native code (runtime)
    - AOT (Ahead of time) converts code during build time instead of runtime.

## Are there any like it? What differentiates it?
- *?*


## Questions
- *What is RHEL*?
    - **Red Hat Enterprise Linux** (-.-|||)
- *More research needed into cri-o*
    - *what is runtime interface?*

- *What is a "pod"? In the context of a container*
    - *how do applications in pods interact with applications in other pods?*
    - *what is the difference between a pod and a container?*
    - **pods can be considered as their own nodes, while containers are just an instance of execution.**
        - **thus, if a single pod goes down, all the containers within the pod goes down as well**
        - **mutliple pods can be contained within a VM**

- *why do we need so many pods in an environment?*
    - *especially if each pod contains a container?*
    - **As above, each pod is a node. To ensure stability, each pod should only contain 1 container to ensure the microservice is isolated**
- *what is kafka?*
    - *by extension, wtf is EFK*
        - **LOG MANAGEMENT SYSTEM**
        - Elasticsearch: search and analytics engine to store logs
        - Kibana: web UI for elasticsearch
        - Fluentd: gathers logs and sends to Elasticsearch --> *what is this for?*
            - **lives in the VM layer, acts as a webserver**
- *What exactly constitutes an openShift cluster?*
- *what is a s3 bucket?* 
