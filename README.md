# Cloud Native Demo 

This is a cloud native demo from [OpenShift Cloud Native Labs](https://github.com/openshift-labs/cloud-native-labs).
This demo has been updated to OpenShift 4.x and remove wildfly-swarm due to incompatibility with maven 3.6.x. 

This demo showcase Cloud Native applications using Red Hat OpenShift Application Runtimes 
(Spring Boot 1.x and 2.x,  Eclipse Vert.x and Node.js) utilizing a microservices architecture.

The following repositories are reference for this demo:
- [cart-spring-boot](https://github.com/jeejeejango/cart-spring-boot)
- [catalog-spring-boot](https://github.com/jeejeejango/catalog-spring-boot)
- [gateway-vertx](https://github.com/jeejeejango/gateway-vertx)
- [inventory-spring-boot](https://github.com/jeejeejango/inventory-spring-boot)
- [web-nodejs](https://github.com/jeejeejango/web-nodejs)

## CoolStore Online Store App

CoolStore is an online store web application built using Spring Boot, WildFly Swarm, Eclipse Vert.x, 
Node.js and AngularJS adopting the microservices architecture.

* **Web**: A Node.js/Angular front-end
* **API Gateway**: aggregates API calls to back-end services and provides a condenses REST API for front-end
* **Catalog**: a REST API for the product catalog and product information
* **Inventory**: a REST API for product's inventory status
* **Cart**: a REST API for managing shopping cart for each customer

```
                    +-------------+
                    |             |
                    |     Web     |
                    |             |
                    |   Node.js   |
                    |  AngularJS  |
                    +------+------+
                          |
                          v
                    +------+------+
                    |             |
                    | API Gateway |
                    |             |
                    |   Vert.x    |
                    |             |
                    +------+------+
                          |
       +---------+---------+---------+---------+
       v                   v                   v
 +------+------+     +------+------+     +------+------+
 |             |     |             |     |             |
 |   Catalog   |     |  Inventory  |     |     Cart    |
 |             |     |             |     |             |
 | Spring Boot |     | Spring Boot |     | Spring Boot |
 |     1.x     |     |     2.x     |     |     1.x     |
 +-------------+     +-------------+     +-------------+
```
