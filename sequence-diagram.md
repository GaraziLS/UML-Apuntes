 ### (Interaction) Sequence diagrams
 
 This diagram speaks directly to the implementation. They speak to how the code needs to operate. If done well, it will make the implementation of the project much easier to build. It's composed by Class Roles or Participants, Activation or Execution Occurrence, Messages and Lifelines. They allow you as a developer to completely dissect not just the activities or the data and the relationships, it also allows you to visualize all of the messages that are being passed between the various components of your system. 

 Sequence diagrams, commonly used by developers, model the interactions between objects in a single use case. They illustrate how the different parts of a system interact with each other to carry out a function, and the order in which the interactions occur when a particular use case is executed.

In simpler words, a sequence diagram shows how different parts of a system work in a ‘sequence’ to get something done.

![sequence diagrams](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+11.29.33+AM.png)


* ***Class roles/participants***: The large boxes on the top are class roles or participants. One of the nice things about sequence diagrams is they allow you to isolate all of the different communication occurrences that will happen to a participant.

Once we get into the full demo and analyze a full system, you're going to see that the user dashboard is going to receive responses, it's going to send these requests, we can isolate that and know what that participant is in charge of from a communication and from a message sending point.

![class roles sd](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+10.25.21+AM.png)

* ***Activation or execution occurrence***: The activation bar is the box placed on the lifeline.  It is used to indicate that an object is active (or instantiated) during an interaction between two objects. The length of the rectangle indicates the duration of the objects staying active. Activation or Execution Occurrence is the sending or recieving of a message.

In a sequence diagram, an interaction between two objects occurs when one object sends a message to another. The use of the activation bar on the lifelines of the Message Caller (the object that sends the message) and the Message Receiver (the object that receives the message) indicates that both are active/ are instantiated during the exchange of the message.

![activation or executon occurrence sequence diagrams](https://creately.com/static/assets/guides/sequence-diagram-tutorial/image6.webp)

* ***Messages***: You could think of a message as being a method that has the ability to take in some kind of input send output and in some cases it can receive output back. The messages are represented by lines with arrows going in the direction that the message is being sent. They also can have names.

An arrow from the Message Caller to the Message Receiver specifies a message in a sequence diagram. A message can flow in any direction; from left to right, right to left, or back to the Message Caller itself. While you can describe the message being sent from one object to the other on the arrow, with different arrowheads you can indicate the type of message being sent or received.

As shown in the activation bars example, a synchronous message is used when the sender waits for the receiver to process the message and return before carrying on with another message.  The arrowhead used to indicate this type of message is a solid one, like the one below.

![solid arrow](https://creately.com/static/assets/guides/sequence-diagram-tutorial/image7.webp)

An asynchronous message is used when the message caller does not wait for the receiver to process the message and return before sending other messages to other objects within the system. The arrowhead used to show this type of message is a line arrow as shown in the example below.

![line arrow](https://creately.com/static/assets/guides/sequence-diagram-tutorial/image8.webp)


* ***Lifelines***: A sequence diagram is made up of several of these lifeline notations that should be arranged horizontally across the top of the diagram. No two lifeline notations should overlap each other. They represent the different objects or parts that interact with each other in the system during the sequence. 

Lifelines are those dotted lines that go from the participant all the way down for the entire diagram. What they really represent is to make it easier for us to see each one of the stages and to give a spot where the messages can be sent. They don't actually do anything, they're more there so we can know at what stage a message is going to be sent to one of the participants and so on and so forth.

![lifelines sd](https://creately.com/static/assets/guides/sequence-diagram-tutorial/image1.webp)

A lifeline notation with an actor element symbol is used when the particular sequence diagram is owned by a use case.

![lifeline actor sd](https://creately.com/static/assets/guides/sequence-diagram-tutorial/image2.webp)

### CRM Comission engine sequence diagram

![sequence diagram example](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+11.34.52+AM.png)

Starting with the user dashboard, the first thing that happens is they're going to be asked if they want to select or create a user. This is self-referential and this is one of the action executions, so they can choose to select or create a user. All of that is going to happen in the user dashboard, which means the message is being sent internally. For example, if we had a user dashboard class it is going to communicate with itself in order to process that request.

Then it's going to move down the line and it's going to check to see if that user has the setting permission in order to move forward. Once again that's self-referential. The message gets sent back, It starts with the user dashboard level and it gets sent back to whatever module is working with that. 

One thing that I want to make sure that is understood, we wouldn't create a entire system into a sequence diagram. That would just be so massive, it would not be a fun thing to do. What I personally like to do, is break my systems into tiny little pieces and then I will build sequence diagrams for those. I might create a entire sequence diagram just for that little process we see with selecting or creating a user. 

Moving down the lifeline of the user dashboard, you can see the first time where it communicates with an outside system, it sends the render form message to the commission setting participant.

![sd interconnection](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+11.50.35+AM.png)