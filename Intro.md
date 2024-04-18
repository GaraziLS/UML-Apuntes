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