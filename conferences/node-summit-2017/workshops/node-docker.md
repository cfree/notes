# Node & Docker

Container advs:
- Lower overhead
- Boot fast
- Run once, run anywhere
- Mirrored production and dev envs
- Scaling not tightly coupled to cloud provider

Use cases:
- Microservice or distrubuted arch
- A/B testing
    - Blue-green deployment
- Capturing services and infrastructure as code

Happy ops:
- Immutability
- Explicit depenedencies
- Fast boot & restart
- Scale at process level

Infrastructure as Code:
- Dialogue between Ops and Devs
- Pristine reference envs
- No config drift
- Kube/Compose etc. are to services what package.json is to node_modules

Kubernetes relies on Docker under the hood

- LXC (Linux Containers) and other Linux kernal magic
- A layered filesystem for shipping images
- Docker cotainers are easily linked to other containers
- Images are built using a Dockerfile

Docker cmds create new layers, which results in larger container sizes
Layers are cached if no changes are made (similar to git deltas)

Docker Hub:
- hub.docker.com
- Docker Hub is to Docker what GitHub is to git
- Create a login (if you don't have one already)
- Link Docker cli tool to hub account `docker login

Docker pull:
- Get images to work with

Docker Build
- `docker build {folder}`

Dockerfile:
```
FROM node:boron

ENV NODE_ENV production
ENV PORT 5000
WORKDIR /app

EXPOSE $PORT

ADD package.json /app
RUN npm install --production 

ADD . /app

EXTRYPOINT ["node", "app.js"]
```

Running:
`docker run nwhite/sample:v1`

Get container id
`docker ps`

Kill container
`docker kill xxxxxxx`

Map internal port to external port
`docker run -p 5000:5000 nwhite/sample:v1`

Docker tag. Allows to pull latest image
`docker tag {source_image}:{tag} {target}:{tag}`

Docker run:
`docker run {image}`
`docker run [OPTIONS] ...`

Docker push:
`docker push {image}:{tag}`

Cleaning up:
`docker rmi -f ${docker images -a}`
...

What goes into container?
- App and essential depedencies
- dumb-init
- Nothing else!

Yelp created [dumb-init](https://github.com/Yelp/dumb-init)
Small binary that can be dropped into container

`ENTRYPOINT ["/user/local/bin/dumb-init", "--", "node", "app.js"]`

====

Best practices:
- Define user and group - limit permissions
- Minimize layers
- Be aware of layer caches

Use && to concat scripts to only use one layer


## WHy Kubernetes?
Orchestration help. 
- Schedule containers to physical machines
- Restart containers if they stop
- Provide private container network
- Scale up and down
- Service doscivery
 
Features:
- Auto binpacking - smart enought to know how to use least amount of resources and balance out
- Horizontal scaling - set up rules for load scenarios
- Auto rollouts and rollbacks
- Storage orchestration
- Self-healing
- Device discovery and load balancing
- Secret and configuration management

Pods
- Mapping to a container
- Generally 1:1 or 1:many mapping. Treated as if on localhost, can share disk space
- Smallest atomic unit in Kubernetes

Services:

Nodes:
- Physical containers
- Worker machines
- May be a VM or physical machine
- Formerly known as miion
- 

Terminology:
- Smallest deployable unit of computing that can be created and managed by Kb

Replica set:

Namespaces:
- Virtual clusters

Labels and selectors:
- Labels are key/value pairs that attach to objs (pods)
- Labels are intended to specify indentifying attrs
- Labels must be unique
- Selectors are used to ID a set of objs
- Empty selectors, selects every obj

Deployments:
- Provides updates fo rpods and replicate sets
- Abstraction layer on top of Kb to control orchestration, how to roll out, when to switch things over

Networking - Docker model:
- Docker uses host-private networking
- Creates a virtual bridge-default `docker0`
- Allocates a subnet from one of the private addr blocks
- Each container is allocated a `veth` (virtual ethernet device)
- `veth` mapps to appear as `eth0` in container
- Docker containers can only talk to containers on the same machine/virtual bridge
- Communicating across nodes requires allocation of ports on machines, which are then forwards or proxied to containers

Docker Swarm:
- How to addr docker across multiple machines. Cluster, like Kb, changes networking model

Networking - Kb model
- All containers can communicate with all other containers without NAT
- All Nodes can communiate with all containers withotu NAT
- The IP that a containers see itself is the same IP that others see it as
- Less complex overall - easier to scale. Manages dynamic port allocation gracefully

Kubectl - command center

Create namespace via yaml file
Create secret for nginx
Create configmap for nginx configuration
Create services
Load deployment

Create objects

Stack (top to bottom):
NSolid - NodeSources commercial version of Nodejs. Enterprises wanting more information out of Nodejs apps
Deployment ("rubber hitting the road". Define ports, labels. Entire application)
Kubectl (CLI tool, talks to cluster, create YAML files. Define services, logical grouping of selectors)
Kubernetes (bunch of machines running Docker, runs it's own Docker engines, talk to each other as a cluster)
Docker (engine, running container)
