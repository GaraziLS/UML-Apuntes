### State machine diagrams

In state machine diagrams what is being visualized is what data looks like and actions at various stages of a software systems lifecycle. The elements are Entry points, Choices, Constraints, States and Transitions.

![state machine diagrams](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-13+at+10.40.54+AM.png)

What is our goal when we're building a state machine?

The name implies a lot and what we're essentially trying to do is visualize what our application (or what a feature of our application) will look like and how it can transition from one state to another state. This could be as low level as being able to represent what a button looks like or what actions can be performed on a button based on how the user's role is set up. It can be that low level or it can be a very high-level kind of concept where it's similar to an activity diagram. Where you can see where a user can go into one page and they can change into another.

Distinguishing state machines from activity diagrams: They both deal with behavior, however, there is a very subtle difference. That is that an activity diagram works a little bit more like a flow chart, you can have a user that goes to one page and they go to another page, they can be asked these questions and different behavior ensues. State machine cares more about the different actions that can change a user's state.

A great example would be if a user goes to a registration page and they fill it out, then the next state may be having a different type of role for the user or their user state change. They used to be a visitor and now they're a current user, it may seem similar and there definitely are similarities but that is a subtle difference between the two.

* ***Entry point***: Represented by a black-filled circle. Represents the start of a system.

![start point sm](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+1.41.46+PM.png)

* ***Choice***: Similar to branches in activity diagrams. Right here we have a choice on a visitor. If a visitor comes to the site and they check to see if the form was submitted or not. If the form was submitted, they are converted and they're no longer a visitor. Now they're a converted user. If the form is not submitted, their state does not change.

![choices sm](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+1.49.02+PM.png)

* ***Constraint***: In the diagram above, the constraints are the "Yes" and the "No." but not always. That is a way of being able to ask, in this case of the form was submitted or not. In other diagrams that we've worked through, the constraint was also called a "guard."

However, there are times and scenarios where you're going to have additional items, so it's not just going to be as easy as did they submit the form or not. It may be something where they logged in and the system checked to see what kind of user they are, if they're an admin then they're going to be shown this page if they're not an admin they're going to be showed shown a different dashboard.

Once again, you can see there are some similarities between the state machine diagram and an activity diagram. It's very important to keep on reminding yourself of what the main goal is, the main goal is to visualize the state of whatever object we're trying to follow.

* ***State***: Represented by rounded rectangles. In the diagram above, they're the Visitor and the Converted states. This leads to the transition.

* ***Transition***: The transition is how you get from one state to another, that's represented by a line with an arrow showing the direction of that transition. You can also have other items, like choices, that are placed in-between those.

### CRM state machine diagram

![state machine diagram](https://s3-us-west-2.amazonaws.com/devcamp-pictures/UML+images/Screen+Shot+2017-10-17+at+2.21.30+PM.png)

