---
layout: post
title:  "A Short Introduction to Docker & Kubernetes"
date:   2019-06-19 18:42:04 +0100
---

## What is Docker

Docker is perhaps the worlds most famous containerisation product. It allows you to run many pieces of software that might have different requirements on the same machine. Before containerisation, applications with different requirements would have to be run on different machines. For example your database might require version 1 of some system library, and your load balancer might require version 2. This can be very costly, in both money and time, and can lead towards [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).

Docker allows you to segregate all aspects of an applications runtime requirements, all the way down to the OS level.

## What is Kubernetes

Kubernetes "is an open-source system for automating deployment, scaling, and management of containerized applications". Putting your application components into conatiners is all well and good, but there is still a piece of the puzzle missing. How do you decide *where* to run these containers? Without a tool like Kubernetes, you have to decide manually which could lead to under utilised hardware, or worse, resource contention. Kubernetes lets us take a Docker container, and ask for it to be run with a certain amount of CPU and RAM, but leaves the descision of where to run it to Kubernetes. This lets us make the most efficient use of our hardware as possible, and also lets us scale up very easily. If we need more machines to run our application, we can just change the configuration and Kubernetes will handle the rest!