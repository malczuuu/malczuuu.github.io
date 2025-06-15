# Damian Malczewski

## Table of Contents

- [Overview](#overview)
- [Projects](#projects)
    - [Taskbook](#taskbook)
    - [Problem4j](#problem4j)
    - [Micro Shadow](#micro-shadow)
    - [iEmu](#iemu)
    - [Multi-tenant Articles](#multi-tenant-articles)
- [Tools](#tools)
    - [Prototypes with Docker Compose](#prototypes-with-docker-compose)

## Overview

This website provides a summary of my after hours programming activities.

## Projects

Below is the list of personal projects. Most of these were brought to life as a form of learning
something new or as a proof of concept.

### Taskbook

A simple issue-tracker application, developed with Spring Boot and Angular frameworks at college. 
After finalization, this project is being used as a testing tool for what's new in next versions
of these frameworks.

See [the project's website][taskbook].

[taskbook]: https://malczuuu.github.io/taskbook

### Problem4j

A Java library implementing [RFC7807](https://tools.ietf.org/html/rfc7807). Integrates with Spring
Boot to provide responses in form of `application/problem+json` documents.

```json
{
  "type": "about:blank",
  "title": "Not Found",
  "status": 404,
  "detail": "User \"luke.skywalker@galaxy.example.org\" not found"
}
```

The library is available through `https://jitpack.io` Maven repository. It is used by most of Spring
Boot applications on my GitHub.

Library is decomposed into multiple repositories. See [main docs repository][problem4j] and navigate
to appropriate module.

[problem4j]: https://github.com/malczuuu/problem4j

### Micro Shadow

A simple IoT device shadow application, powered by Spring Boot and RabbitMQ. Explores the flow
of [Device State Replica][replica] pattern of IoT communication over MQTT topics. This is
a backend-only application and interactions should be made via REST API.

See [the project's repository][ushadow].

[replica]: https://iotatlas.net/en/patterns/device_state_replica/

[ushadow]: https://github.com/malczuuu/ushadow

### iEmu

Emulator application for an IoT device working with LwM2M (based on project [Leshan][leshan]).
Supports a bunch of LwM2M objects and provides a management WebUI, accessible on localhost. Requires
a working installation of LwM2M server like [Leshan Demo Server][leshan-demo-server].

See [the project's repository][iemu].

[leshan]: https://github.com/eclipse/leshan

[leshan-demo-server]: https://leshan.eclipseprojects.io/

[iemu]: https://github.com/malczuuu/iemu

### Multi-tenant Articles

A simple application for exploring multi-tenancy concepts.

Application gives the users a personal space for writing articles (quite simple CRUD application).
The application however is available from three different domains, each integrated with different
Keycloak realm. This creates a multi-tenant environment, where each tenant has its own set of users
and the application resources.

The most useful part of this project (and possibly reusable in the future) was creation of a
multi-realm Keycloak installation, defined in `docker-compose.yaml` file.

See [the project's website][articles-app].

[articles-app]: https://malczuuu.github.io/articles-app

## Tools

### Prototypes with Docker Compose

List of prototypes of `docker-compose.yaml` setups of various services for personal development.

- [`keycloak-compose`](https://github.com/malczuuu/keycloak-compose)
- [`mongo-compose`](https://github.com/malczuuu/mongo-compose)
- [`portainer-compose`](https://github.com/malczuuu/portainer-compose)
- [`rabbitmq-compose`](https://github.com/malczuuu/rabbitmq-compose)
- [`traefik-compose`](https://github.com/malczuuu/traefik-compose)
