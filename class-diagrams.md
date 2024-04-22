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