# Microservice Development

When starting to develop backend applications, there are certain things we should pay attention to:
* Node.js versions
* Boilerplate reuse
* 3rd party libraries
* Test-Driven Development

## Starting from scratch

We use only two versions of Node.js when developing: Current and LTS. For production uses, only LTS v6.x is considered.  
Since all of our microservices' base architecture should be nearly the same, we introduced a boilerplate application, [qaap-node-kickstart](https://github.com/qaap/node-kickstart). You can install it globally and create your application's skeleton with it.

## General purpose tools

The tools we use when developing a microservice, and those are mainly python and shell scripts,
are meant to be fetched from our [contrib](https://github.com/qaap/contrib) project.  
Once the application is *kickstarted*, we could add those tools via git submodule with the following command:

```git submodule add https://github.com/qaap/contrib tools```
