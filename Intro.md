# UML (Unified Modeling Language)

In short: diagrams that illustrate code workflow, without a single line of code. Visual tool to understand how the code works.

## UML components

### Frames

**Frames** encapsulate components and provide context. A series of shorthand notations indicate what type of frame is being used. The type of frame is indicated inside a box in the upper part of the diagram.

![Frame explanation](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-11+at+2.39.43+PM.png)

### Frame types (shorthands)

* **act**: activity
* **class**: class
* **cmp**: component
* **dep**: deployment
* **sd**: interaction (sequence diagram)
* **pkg**: package
* **stm**: state machine
* **uc**: use case

 ![Frame example](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-11+at+3.08.36+PM.png)

 ### Classifiers

 **Classifiers** identify components. They're abstract and not directly implemented. They classify items.

 Components that use classifiers: 

 * ***Classes***
 * ***Interfaces***
 * ***Associations***
 * ***DataTypes***
 * ***Actors***
 * ***Use cases***
 * ***Artifacts***
 * ***Components***
 * ***Signals***

 ![Classifiers explanation](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-11+at+3.50.07+PM.png)
 
 *Topic* (right rectangle) is the class, not the classifier. The items inside the topic are the classifiers.

 ### Comments/Notes

 ***Comments***, also called notes, cñarify things (but it's better to be crystal clear on the diagrams). They're represented by dotted lines.

 Comments are in rectangular boxes and they have a dotted line to the element they describe.

 ![Comment explanation](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+10.14.02+AM.png)

 ### Dependencies

 ***Dependencies*** denote coupling, aka related components, bi or unidirectionally. They're represented by dotted lines with open arrows.

 ![Dependencies explanation](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+11.02.32+AM.png)

 If the arrow is removed the SongRequest will no longer work.

 ### Features and Properties

 They represent attributes of an element, such as name or what kind of protection they have. They serve as an implementation guide. Usually accompanied by comments.

 ![Features and properties explanation](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+11.25.11+AM.png)

 ## Structural diagrams

 Structural diagrams are any type of diagrams that model the way a system is architected. In other words, a class diagram is one of the most popular structural diagrams out there. It's a way of defining the different class names, attributes, and method names that belong inside of a system that you're building.

 **Types**

 * *** Class ***: Composed by classes that have names, attributes and operations. It describes what elements do you have, how they associate and some core operations.

 ![class example](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+1.53.59+PM.png)

 ![detailed class breakdown](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+1.56.22+PM.png)

 The little plus sign means that the operation/method/function is available to outside classes. In other words, if we have a controller that calls topic, it creates a topic. It can then call top ten on that topic instance and bring back the top ten topics.

If we add a little minus sign, that would mean that it is an operation/method/function that is only available to the topic. For example, if we had some specialized algorithm that determined the top ten and we didn't want any other class to be able to call it, we would put a little minus sign right there to say this is private. It's visible only to the topic.

 * *** Deployment ***: Composed by nodes, deployments, artifacts, links, artifacts, dependencies, and associations. This diagram is used to model how an entire system architecture should be configured.

 ![Deployment diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+2.41.43+PM.png)

 This is a deployment diagram for an assessment engine, starting at the top, it has what is called the CI server. In the CI server we have: Staging environment, Pre-production environment, and Production environment. The large boxes are called nodes, and inside them we have components.

 * *** Package ***: Composed by Types, classifiers, classes, use cases components, packages, constraints, dependencies and events. 

 ![package diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+4.09.39+PM.png)

 We have a phone parser and this has a few elements: Number, Country code and Digit length validator.

 right there in between we have a dependency. Remember dependencies are those elements that have the dotted lines connected to an open arrow.

A dependency to country codes, which is another code library all wrapped inside of the phone parser package. Inside of there, we have some data collections and we have some other operations. The nice thing about a package diagram like this, we have the ability to, at a glance, see that we have these two modules that make up the package. We know that one of the modules depends on the other and we can see all of the attributes and operations at a glance.

This makes it easy when you have these types of diagrams, you can organize your code and it also makes it a bit easier to think through things.

## Behavioral diagrams

Behavioral diagrams are much different, behavioral diagrams care about how your system behaves. It cares about different things like what type of messages does one system send to another or what types of permissions does user A have versus User B. Those are the types of questions that you're going to model out inside of behavioral systems.

Here we can find these types of diagrams:

* *** Activity ***: Activity diagrams are to behavioral diagrams the same as class diagrams to structural ones. It shows the workflow of a client's decisions, showing all the possible outcomes. It's composed by these elements: Initial state or start point, Activity/action state, action flow, decisions and branching, guards, final state or end points, and swim lanes.

![activity diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+10.18.53+AM.png)

* *** Use case ***: They show everything that a user has access to (won't be the same for regular users and game developers for example). It's composed by use cases, actors, subsystems, and relationships.

![use case diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+10.22.01+AM.png)

* *** State machine ***: Here, what is being visualized is what data looks like and actions at various stages of a software systems lifecycle. The elements are Entry points, Choices, Constraints, States and Transitions.

![state machine diagrams](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+10.40.54+AM.png)

* *** Sequence diagrams ***: This diagram speaks directly to the implementation. They speak to how the code needs to operate. If done well, it will make the implementation of the project much easier to build. It's composed by Class Roles or Participants, Activation or Execution Occurrence, Messages and Lifelines.

![sequence diagrams](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+11.29.33+AM.png)


