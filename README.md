# Docker Compose Library
A simple library that holds all of the docker compose files I used to deploy containers within my local infrastructure.

All compose files have had sensitive values redacted.

## Infrastructure Setup
I manage all of my containers through Portainer, which itself is installed on my TrueNAS system.  TrueNAS also holds all of the data for the containers in a persistent directory structure

`/mnt/main/apps/<appname>`

Each of these apps is hosted within a Portainer stack and are given a unique network name.  Containers are assigned each other's network access should they need to communicte with each other.

Each container itself runs as the TrueNAS "apps" user (UID 568) which is the primary user that Portainer itself runs as.  I won't cover dataset setup within TrueNAS here as that is outside the scope of this repositoy.