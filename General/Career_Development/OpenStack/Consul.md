Content-Type: text/x-zim-wiki
Wiki-Format: zim 0.4
Creation-Date: 2017-01-03T13:58:58+00:00

###### Consul ######
Created Tuesday 03 January 2017

"Service Discovery & configuration made easy. Distributed, highy available & datacenter aware"

Makes it easy for services to register themselves
and to discover other services via a DNS or Http Interface
Can also register external services

//Can it be accessed externally to see all the services?//

Failure Detection & Health checks
Key/Value Store

master / agent setup (Like puppet)
	agent runs on node and reports to master
	There can be multiple "master" servers but one is the only true master

//Looks like the only useful information is address and ip, I only see a single "interface". Will all the interfaces be present in the cloud deployments?//

//Could the K/V Store be used to store the missing host information?//
