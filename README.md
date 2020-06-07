# DockerWars


What is DockerWars?

An Educational Game

Docker wars is (hopefully) global, it consists of a game, fought between two sides (Team Red & Team Blue). Each side needs units & resources. These are gained by deploying different docker images that add more of that unit type or resource. Calculations are then carried out centrally (hourly), based on the resources and units on each side (provisioning a container, you add ENV variables for which side, and a unique username), a winner is declared. Units on the losing side breakdown, the docker image needs to be deleted and recreated before the next battle for it to be counted.

Steps are injected to promote the benefits of containerisation, orchestration and security best practices.

If a member of a team has the code running on a baremetal server, the entire server would need to restart (or app -reinstalled). If they have 10 containers on a docker host, they may only need to restart the frontline containers. (promoting some benefits of docker, in addition to micro server architecture).

This also raises the case for orchestration, where the docker images could fail a healthcheck and be automatically restarted etc.

Additionally, units will receive (updates) that increase their stats (regular and linear). They will be available from dockerhub a few days after the code is published to github. Promoting the use of CI/CD pipelines to be able to quickly and automatically pull the changes, build the container and have an advantage over those that simply wait for the dockerhub build.

Additionally, some containers will have built in (but actually harmless) vulnerabilities, such as an API on port 80 that can trigger the shut-down that normally happens when losing a battle. Well organised teams could find and exploit these, if the other side has simply followed instructions without asking why (Why is port 80 left open for inbound traffic etc). This could also promote learning around not using public IP's for outbound only apps etc.

The containers have to use up resources so that someone does not deploy thousands of conatiners on weak hardware. However I feel uncomfortable just using processing power, and therefore energy for a global game. So instead, the containers must prove they are online and ready for battle 30 minutes before (and until the battle starts) by doing a social good and processing folding@home workloads (for example). (need to find a way to measure the compute and set a minimum.

The main site will be built out with support forums, useful tutorials (install docker, run a container, setup Kubernetes, doing it via Azure, AWS, OCI etc), news and general stats & metrics.

The aim is to meet the goal of promoting the use of modern technologies, having some fun and giving real life skills and use cases for people to utilise in their job or to take their career further if they enjoy it.

Ideally the open source project could call on vendors such as Digital Ocean or Docker to provide short term discounts etc. (Need to check whether this is allowed within the terms of Azure starter credit, or OCI always free services.)

The containers themselves could be deployed to Azure, AWS, GCP, OCI, at home, laptops raspberry pi's.

Potential Architecture (Rough Copy)

![Potential Architecture](https://github.com/djh82uk/DockerWars/blob/master/DockerWarsArchitecture.png)
