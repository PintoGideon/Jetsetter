# Logic Workflow

a. Create an list of default items to display (Items Components ->Item Component)

b. The items is in the application state. It is immutable and I can't pass
them down to the component AddItem. I will instead pass down a function
which Add Item can call to manipulate the state.

# Add an Item to the list

a. This component will provide an input field to the user to add an item. This will be a form with a onSubmit function and the input
field will have an onChange to allow the user to type in the textbox.

b. The Add Item component will have it's own state which will change as the user types. We will then send the item up to the application to modify the items list.

# Remove an Item from the list

a. The item list is in the application level state. So we pass down on a function
to the Item component through props which will have an onClick function which will bubble
the event all the way up to Application and delete the item.
Application----> Items---->Item

# Toggle an Item

a. The main goal here is to move the checked item from the between the lists. The function will be passed down two levels.
Application-->Items-->Item

# State Architecture Patterns

React state is stored in a component and passed down as props to it's children

a. Identify every component that renders
something based on that state
b. Find a common owner component ( a single
component above all the com)
c. If you can't find a component where it makes
sense to own the state, create a new component simply for holding the state and add it somewhere in the hierarchy above the owner component
d. As you start to build large libraries of components, you'll appreciate this explicitness and modularity, and with code reuse, your lines
of code will start to shrink


# Container Patterns

Lifting state with the container pattern
Draw a line between state and presentation


Presentational components receive props and
render UI


