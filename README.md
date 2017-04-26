# React Explanation of Props, State, and Component Life Cycle


## Props

This is how information or data is passed from a parent to a child. It is a way for information to be transferred and used between different componenets. Props are always passed from the top component (parent) to the bottom component (child).

## State

This is how the component's data is at a specific time. In the beginning, a component's state is established and later it can be manipulated.

## Component Life Cycle

There are three phases: **Mounting**, **Updating**, and **Unmounting**. They can vary depending on what the application is doing. 

- Mounting: When the component is first created to when it is being rendered or when the application is first opened
- Updating: When the component is being used or when the application is being updated
- Unmounting: When the component is ready to finish being used


From the moment your component is born - when it's initially being rendered - it enters the Mounting Phase. Once your component is living a happy life and is being updated it enters the Updating Phase. Finally when it's time to end it's life it enters the Unmounting Phase.

1. Mounting
	- constructor() => This is called before it is mounted onto the page. This is also where state is first initialized.
	- componentWillMount() => This is called right before the component is mounted onto the page
	- render() => This is called right after componentWillMount()
	- componentDidMount() => This is called right after the component is mounted onto the page

2. Updating
	- componentWillReceiveProps() => This is called before the component that is mounted takes in new props
	- shouldComponentUpdate() => This is called if there is an update in the component or before rendering if there are new props or a new state. If this one returns false, then the following won't be called. But if it returns true, they they will. 
	- componentWillUpdate() => This is called right before new props or new state is being redered onto the page. This will only be called if shouldComponentUpdate() comes back true.
	- render() =>
	- componentDidUpdate() => This will be called right after an update happens in the component. 

3. Unmounting
	- componentWillUnmount() => This will be called right before the component is finished being used

