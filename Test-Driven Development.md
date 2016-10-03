# Test-Driven Development

*A work-in-progress article*

[Mocha](https://mochajs.org) is our *de-facto* choice of a testing framework when it comes to testing our applications.  
We also chose [Chai](http://chaijs.com) for assertions.

## Environment-dependent testing

There are a few test environments we should commence:
 * unit tests
 * isolated tests
 * integration tests

### Unit tests

Unit tests are the ones we use to test libraries when developing with [TDD](https://en.wikipedia.org/wiki/Test-driven_development)/[BDD](https://en.wikipedia.org/wiki/Behavior-driven_development).  
Each library should be throughly tested for correct and incorrect behaviour.

### Isolated tests

We mostly develop each application in a separated, isolated environment,
meaning each of those should pass a minimal set of tests predefined to assert a needed behaviour.

Most importantly, if a certain test is meant to be executed in an environment we do not have access to
(ie. a behavior tested depends on a different application we are developing separately),
we should check up on the ```process.env.NODE_ENV variable``` and make sure it's not set to ```integration```.  
More of that in the next subsection.

### Integration tests

Integration tests are a separate type of tests where we include one or more external application that is a
dependency to the currently developed application.  
Before starting those type of tests, we *must* set an environment variable called ```NODE_ENV``` to a value ```integration```.

Once we have that, we can insert a portion of code at the beginning of each test that is meant to be used for integrations like so:
```js
if (process.env.NODE_ENV !== "integration")
    return this.skip()
```
