# simple-gateway

This is a simple gateway service built on Zuul. It has the following dependencies:

**config-client**<br/>
**service-registry**

The service can be deployed to cloud foundry as long as there is a service registry and a config server available (see **manifest.yml** for details). The config file **simple-gateway-dev.yml** needs to be pushed to the config server. The **application.yml** has a reference to URL in zuul routes which need to be commented and the **serviceId** has to be uncommented when deploying to PCF.

When run locally, It routes requests to the simple-service at port 8081. Once the gateway is up and running, the simple-service can be accessed at **http://localhost:9090/api/simple/** that returns "hello".
