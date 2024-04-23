### Deployment diagrams

Composed by nodes, deployments, artifacts, links, artifacts, dependencies, and associations. This diagram is used to model how an entire system architecture should be configured.

 ![Deployment diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+2.41.43+PM.png)

 This is a deployment diagram for an assessment engine, starting at the top, it has what is called the CI server. In the CI server we have: Staging environment, Pre-production environment, and Production environment. The large boxes are called nodes, and inside them we have components.

* ***Nodes***: Every part of the diagram is a node. 

![nodes deployment diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+2.57.46+PM.png)

* ***Components***: Can be an app, an API, a web service, a database... represented by rounded rectabgles or 3d cubes. The symbols aren't that important, being consistent to represent the systems is.

![component](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+3.07.22+PM.png)

![components](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+3.10.43+PM.png)

* ***Artifacts***: They're put inside << >>. When analyzing a deployment diagram, if I want to see what type of server I'm going to deploy or the type of application that I'm going to configure, these are the items that I look at.

![artifacts deployment diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+3.38.29+PM.png)

* ***Links and Dependencies***: Lines connect nodes. Dependencies are represented by dotted arrows in the direction of the node they're tied to.

![dp links](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+3.45.33+PM.png)

![dp dependencies](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+4.09.59+PM.png)

* ***Associations***: The association element is very similar to the link and the dependency. It is a way of connecting all of the nodes and showing how they're associated. (Child nodes connected to a parent node). In this case, we have an entire system that represents how a user and an API can connect with a web application that leverages a load balancer. We're not going to focus on how load balancers work, however, by looking at this system you can tell that a load balancer can take in a request from the Internet and then maps that to various applications servers.

![dp associations](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+3.58.01+PM.png)

## Song request deployment diagram

![Song request deployment diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-16+at+4.18.05+PM.png)

Let's start off with the very top left node, we have a regular web service, this is going to be the user interface for the entire system. We can see that it needs to be on some type of device, that's the artifact. I added some additional details so we have an operating system of Linux and then we have a component inside that's going to leverage angular.

This has a few dependencies. It has a dependency on the API itself, which is going to be the backend that manages all of the data and the majority of the business logic, then it also has a dependency on the authentication system.

So it's going to connect to two different systems

* One manages the process of logging in, checking if a user is registered and if they're allowed to be on the system

* One manages the backend and I placed a couple of other artifacts that are protocols (JSON and restful API)

If you were to show this to me, I could see that you had an angular front end communicating with a Rails API and an authentication system. I'd then have some clues on how to build the system.

Talking about dependencies, this is a great example to analyze how dependencies work in software. We have Angular front end (we've covered its dependencies) but the authentication system technically has no set of dependencies. The reason for that is because of the way dependencies work in general. Dependency really means the system would not be able to function properly without whatever it's depending on.

The Angular front end needs dependencies, imagine if you went to it and it had no data, you couldn't log in. The authentication system, on the other hand, does not care about the angular front end, you could swap it out with a re-act front end and it would not care in the least. It simply takes in requests and gives responses, it does not depend on those other systems.

A system between node is the rails API. Technically it doesn't care or depend on the front end either. It simply is an API that takes in requests and then gives responses. However, it does have a dependency on the authentication system, the reason is that sometimes the responses are coming in and it is going to communicate with that auth system to ensure that it was a valid request.

That is a very common pattern you'll see where you'll have a javascript front end with a rails back end, many times between the two there will be some type of authentication system.

Each of these nodes is very similar in regards to its structure. It has a set of artifacts and components inside. You can use notes and comments to give more description for the developers, I noted that this is going to use JWT tokens for auth communication.

If I hand this to a Rails developer, this will give them a set of instructions on what to build.
