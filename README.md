


# Abstract

To create an API backend system that is hosted inside a Kubernetes orchastration. 

This will then mimik a system that is split up into numerous backend microservices and accessed via a single public gateway.


# Requirements

- [Traefik](https://www.Traefik.io) as the reverse proxy / load balancer between the backend services. (This is the public endpoint to access everything.)
- Two different websites behind the Traefik RP.
- Each website requires a database (or some dependency).
- Each website and database are considered a single 'microservice'.
- All of this managed and handled via Kubernetes (locally on Docker Desktop or in a Cloud Provider).


# Images to use
- [RP/LB] Traefik : [traefik](https://hub.docker.com/_/traefik)
- [Web API] Some simple website: [radumatei/private-api](https://hub.docker.com/r/radumatei/private-api)
- [Some Db] Some simple db/store: [redis](https://hub.docker.com/_/redis)


# Sample urls/domains (for localhost testing)

### Public endpoints
- api.localtest.me/accounts
- api.localtest.me/orders

### Private, admin endpoints 
- api.localtest.me/traefik-admin
- api.localtest.me/accounts-db


# Overall picture

![](https://i.imgur.com/oXKvB4l.png)

---

-end of readme-