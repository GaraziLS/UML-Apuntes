### Package diagrams

Package diagrams are omposed by Types, classifiers, classes, use cases components, packages, constraints, dependencies and events. In sum, they're componed by other diagrams. Your package diagram is something that allows you to take your other different components inside of your system and show how they relate to each other and you can show dependencies and some different elements like that. 

![package diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+9.49.23+AM.png)

 ![package diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-12+at+4.09.39+PM.png)

 We have a phone parser and this has a few elements: Number, Country code and Digit length validator.

 right there in between we have a dependency. Remember dependencies are those elements that have the dotted lines connected to an open arrow.

A dependency to country codes, which is another code library all wrapped inside of the phone parser package. Inside of there, we have some data collections and we have some other operations. The nice thing about a package diagram like this, we have the ability to, at a glance, see that we have these two modules that make up the package. We know that one of the modules depends on the other and we can see all of the attributes and operations at a glance.

This makes it easy when you have these types of diagrams, you can organize your code and it also makes it a bit easier to think through things.