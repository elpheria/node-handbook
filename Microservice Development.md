# Microservice Development

When starting to develop backend applications, there are certain things we should pay attention to:
* Node.js versions
* Boilerplate reuse
* 3rd party libraries

## Starting from scratch

We use only two versions of Node.js when developing: Current and LTS. For production uses, only LTS v6.x is considered.  
Since all of our microservices' base architecture should be nearly the same, we introduced a boilerplate application, [qaap-node-kickstart](https://github.com/qaap/node-kickstart). You can install it globally and create your application's skeleton with it.
