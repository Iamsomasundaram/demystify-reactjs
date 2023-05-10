# Demystify ReactJS
You must have heard about the buzzword ReactJS or simply React, and want to explore more about React, and that is why you are here. I have done my best to collate information from different websites, videos and books to explain all various concepts in React.

My Demystify series is to help job seekers and developers by proividing the relevant content.  Syncfusion's succinctly

# Basics

	1. React is a JavaScript library for building user interfaces.
	2. JSX is a syntax extension to JavaScript. 
		a. JSX produces React “elements”. React elements are the building blocks of a React application. 
		b. React elements are plain JS objects and immutable, meaning once you create you can’t change its children or attributes. 
		c. ReactDOM takes care of updating the DOM to match the React elements.
		d.  One might confuse elements with a more widely known concept of “components”. An element describes what you want to see on the screen. 
	3. Components 
		a. They are like JavaScript functions, they accept arbitrary inputs (called “props”) and return React elements. 
		b. Basically they are small, reusable pieces of code that return a React element or other component to be rendered to the page
		c. A good thumb rule is that if a part of your UI is repeated several times (Button, Panel, Avatar), or is complex enough on its own (App, FeedStory, Comment), it is a good candidate to be created as a separate component.
		d. Types of components - Function and Class Components
		e. Component names should also always start with a capital letter
		f. In class components a common pattern is for an event handler to be a method on the class
	4. What are props? 
		a. props are inputs to a React component. They are data passed down from a parent component to a child component.
		b. Props are Read-Only and we should not try to modify it in any way
		c. props.children contains the content between the opening and closing tags of a component.
		d. React elements like <Contacts /> and <Chat /> are just objects, so you can pass them as props like any other data.
	5. What is state?
		a. State is similar to props, but it is private and fully controlled by the component.
		b. An important difference between state and props is that props are passed from a parent component, but state is managed by the component itself. 
		c. A component cannot change its props, but it can change its state
		d. Do Not Modify State Directly - Constructor is the only place where you should assign this.state directly. In all other place, we need to call this.setState() to schedule updates to the component local state
		e. State updates may be Asynchronous - Because of this nature, this.props and this.state may be updated asynchronously, you should not rely on their values for calculating the next state. To fix it, use overloaded version on this.setstate where it accepts a function as param instead of an object. That function receives two params, previous state and the props at that time the update is applied
		f. State updates are shallow merged
	6. List and Key - A key is a special attribute that needs to be added when working on lists of elements for a stable identity. Keys help React to identify which items have changed, are added, or are removed. 
	7. Controlled Components
		a. An input form element whose value is controlled by React is called a “controlled component”.
		b. Generally Input form elements maintain their own state and update it based on user input. 
		c. In React, mutable state is typically kept in the state property of components, and only updated with setState(). We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. 
		d. Specifying the value prop on a controlled component prevents the user from changing the input 
	8. Uncontrolled component
		a. In a uncontrolled component, form data is handled by a DOM itself.
		b. use a ref to get form values from the DOM.
	9. Lifting State Up - In React, sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called “lifting state up”. This allows us to more easily share state among all of these components that need rely upon it. 
		a. Lifting the state prevents sharing too much or too little state in your component tree. Basically, it is a refactoring that you have to do once in a while to keep your components maintainable and focused on only consuming the state that they need to consume.
		b. Lifting state should be used to give components access to all the state they need, but not to more state than they need.
		c. lifting state allows you to keep your local state management maintainable
	10. Composition vs Inheritance - using composition instead of inheritance to reuse code between components. Props and composition give you all the flexibility you need to customize a component’s look and behavior
		a. "has an" vs "is a"
		b. A car is a vehicle can be modeled with inheritance and A car has an engine can be modeled with composition

