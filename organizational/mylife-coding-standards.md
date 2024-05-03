# MyLife Coding Standards

## Naming Conventions

- No offensive names
- No ownership language direct or insinuated
  - `enum: ['parent', 'progeny', 'provider', 'provisioner']`

## Code Structure

### Using `String.prototype.includes()` for String Search in JavaScript

The `includes()` method is a built-in JavaScript function that checks if a string contains a specified substring. It returns a boolean value - `true` if the substring is found, and `false` otherwise.

#### Syntax

```javascript
str.includes(searchString[, position])
```

- `searchString`: The substring to search for.
- `position` (optional): The position within the string at which to begin searching. Default is `0`.

#### Example

```javascript
const str = 'Hello, world!';
console.log(str.includes('world')); // Outputs: true
```

#### Use Case in Event Handling

In event handling, `includes()` can be used to check if the `id` or `class` of the event target contains a specific string. This is useful when you have multiple elements that share a common part in their `id` or `class` and you want to handle them in a similar way.

For example:

```javascript
element.addEventListener('click', function(event) {
    if (event.target.id.includes('my-prefix')) {
        // Handle the event
    }
});
```

In this example, any element whose `id` contains `'my-prefix'` will trigger the event handling code when clicked.

#### Why It's Useful

The `includes()` method is a simple and readable way to check if a string contains a substring. It's more intuitive and easier to understand than using a regular expression or the `indexOf()` method, especially for beginners or non-technical people reading the code.

#### Notes

Remember, `includes()` is case-sensitive, so 'Hello' and 'hello' would be considered different strings. If you need a case-insensitive search, you might need to convert your strings to the same case before using `includes()`.

### Modular Code Definition Standard

- **Objective**: Ensure that the majority of functionality, especially beyond simple logic, is defined in modular server-side code, not within session-specific scripts.
- **Rationale**: This approach promotes code reuse, simplifies maintenance, enhances testability, and improves the separation of concerns within the application architecture.
- **Implementation**:
  - **Modularization**: Functions, classes, and utilities that provide reusable logic or interact with external services should be encapsulated in separate modules.
  - **Session Logic**: Keep session-side logic minimal, focused on session management and direct interaction handling. Complex operations should delegate to server-side modules.
  - **Code Structuring**: Organize modular code into a coherent directory structure that reflects functional areas of the application.
  - **Documentation**: Document each module's purpose, inputs, outputs, and side effects to facilitate easier integration and debugging.

## API Design Principles

### PATCH Method

#### Patch Method Usage for Experience Management

The `PATCH` method is designated for managing interactive experiences within our platform. It allows for incremental updates to an experience's state, ensuring efficient and precise modifications without the need for transmitting the entire resource state. When an experience is active, all client-side events that result in a change of state from one member input point to another are aggregated and sent as a `PATCH` request.

This approach minimizes network load and optimizes responsiveness. The server, in turn, processes these `PATCH` requests to update the experience state and returns only the necessary data to reflect these updates on the client side. This method fosters a dynamic and interactive user experience, ensuring that data transmission is strictly relevant to the ongoing changes within the experience.

All MyLife Experiences go through this standard, regardless of whether or not it is API-based or the provided front-end.

## Security Practices

## Documentation Standards
