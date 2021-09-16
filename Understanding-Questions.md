# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
* 
* the onClick calls the handleClick function that receives the event
* the handleClick function calls dispatch, which takes the action as a parameter (in this case the action passed through is the addOne action creator)
* addOne is called and receives the clicked button's value (1) as a parameter and returns an object with a type key that has a value of ADD_ONE
* dispatch has access to the current state because it's within the scope of useReducer; it has access to the reducer function that was passed into useReducer
* the reducer function takes the ADD_ONE action and the current state to run switch
* the case(ADD_ONE) returns the state object, adding 1 to state.total. It is then rendered to the calculator because the state was updated
...

* TotalDisplay shows the total plus 1.
