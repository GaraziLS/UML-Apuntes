Composed by classes that have names, attributes and operations. It describes what elements do you have, how they associate and some core operations.

 ![class example](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+1.53.59+PM.png)

 ![detailed class breakdown](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+1.56.22+PM.png)

 The little plus sign means that the operation/method/function is available to outside classes. In other words, if we have a controller that calls topic, it creates a topic. It can then call top ten on that topic instance and bring back the top ten topics.

If we add a little minus sign, that would mean that it is an operation/method/function that is only available to the topic. For example, if we had some specialized algorithm that determined the top ten and we didn't want any other class to be able to call it, we would put a little minus sign right there to say this is private. It's visible only to the topic.

The name is the most self-explanatory piece, we have a topic which is the name for this class diagram. In a real-world scenario, you wouldn't add these specific types of notes like class name because it's self-explanatory.

Attributes have three different items at a minimum that you should include.

* Visibility (public/protected/private can be denoted with a plus/hash/minus)
* Name (Titles. Used in columns inside databases)
* Data Type

Operations are methods/functions. Add a plus if you want to call from outside of the topic or a minus if you do not want to call outside the topic. Also, operations are always followed by parentheses.

## Associations (also relationships), multiplicity and navigability

Associations/relationships: how one class is connected to another. Represented by lines.

In addition to associations there's also multiplicity and navigability, and everything is needed inside a class diagram.

![simple class diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+12.14.41+PM.png)

Using our current setup we can say:

* guide belongs to a topic
* topic has many guides
* guide has many and belongs to tags
* tag has many and belongs to guides

How do we know that a topic has many guides and not the other way around? When we talk about those things that may seem kind of intuitive, however, the numbers are what give it away. That leads to how we need to understand multiplicity.


* Unidirectional association - In a unidirectional association, two classes are related, but only one class knows that the relationship exists. A unidirectional association is drawn as a solid line with an open arrowhead pointing to the known class.

![unidirectional assoc](https://online.visual-paradigm.com/images/tutorials/class-diagram-tutorial/03-undirectional-association-example.png)

* Bidirectional (standard) association - An association is a linkage between two classes. Associations are always assumed to be bi-directional; this means that both classes are aware of each other and their relationship, unless you qualify the association as some other type. A bi-directional association is indicated by a solid line between the two classes.

### Multiplicity

Multiplicity is how we designate the direction of the relationship in regards to numbers. Right here we can see

* Topic can have 1 or more guides. The way that we can see this is, the line from topic to guide says 1...*, that means that a topic can have one or more guides.

* Going in the opposite direction, guide has an association line to topic. A guide is always going to have one topic. You see how we only have 1 by itself and there is no ...*, that means that a guide belongs to a topic. There is always going to be one topic for every guide.

* We have a guide and it can have 0 or more tags. That means, if you think about building a blogging engine, you can create a guide. If you have a tag class attached to it, you may want to be able to create this guide with no tags or create it with any number of tags. That's a pretty standard way of setting up that type relationship. You would denote it exactly like how we have here, we would say a guide can have 0 to many tags.

* There is always at least one guide for every tag. The tag, if you think about it in a blogging sense, are not going to live by itself. A tag has to have some guide that it was created for and added to in order to be alive, that's its dependency. It can also belong to many guides. Think of having multiple blog posts where you're talking about UML, you may add the tag UML, you would add that to the blog/guide. That means a tag can still have many guides, once we get into our detailed breakdown and go into how we would rebuild Twitter using a class diagram, we're going to see this type of relationship quite a bit.

Another more simplified way is, we can draw a line and put a star there. If we put a guide and connected it to tag, we could put a star where the tag is and most developers could see that we mean a guide can have many tags. That's another type of approach you will see often.

Place multiplicity notations near the ends of an association. These symbols indicate the number of instances of one class linked to one instance of the other class. For example, one company will have one or more employees, but each employee works for one company only.

![multiplicity](https://online.visual-paradigm.com/images/tutorials/class-diagram-tutorial/05-multiplicities-examples.png)


## Navigability

Navigability deals with is how you can have one class communicate with any other class. This sets the rules for knowing how that communication can take place.

* You can find all of the guides for each topic because topic is connected to guide
* You can find all of the tags for a topic through a guide. Imagine that we add a topic, like UML, and underneath that, we had any number of guides. if you traverse and go from topic to one of the guides, you could get access to see all of the tags that are associated with that guide. You can do that for each one of the other ones, you can find a guide topic, you can find all the tags associated with a guide, etc.

## Twitter class diagram 

![twitter use case diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+2.21.06+PM.png)