# Testing Style Guide

## _TDD, Jest and RTL best practices_

This style guide provides best practices for testing application using Test-Driven Development, Jest, and React Testing Library.

### Test-Driven Development
Test-Driven Development (TDD) is a software development methodology in which tests are written before the actual implementation code.

#### **Developer** must follow such development steps:
1. Define the place of implementation in the existing application.
2. Create an empty React component file (check [Manual of Style](../react) if required).
3. Create a corresponding test file for the just created React component.
4. Put down as many tests as possible in the test file.
5. Add `throw Error` in an empty test so that it fails until the functionality is implemented in the component file.
6. Implement every test one by one: one test checks one piece of functionality of the component.
7. Add the missing functionality to the component and/or adjust the existing one accordingly.
8. Run the test again so that it gets passed.
9. Repeat testing like the steps above till all component test pass (are green).
10. Run the application and test manually that newly created component as its integral part.
11. Run all the tests present in the application to make sure nothing of previously delivered is broken and all tests pass.

### Jest
- Organize your test suites using `describe` blocks to group related tests, and use `it` blocks to define individual test cases.
```js
describe('MyFunction', () => {
    it('should do something', () => {
        // Test implementation
    });
});
```
- Utilize Jest mocking capabilities to isolate the code under test from external dependencies. This ensures that tests focus on the behavior of the unit being tested.
- Jest provides a wide range of matchers (`toEqual`, `toBeTruthy`, `toBeDefined`, etc.). Choose appropriate matchers to assert the expected behavior of your code.
- For asynchronous code, use `async`/`await` or return a `Promise` and ensure tests wait for asynchronous operations to complete.

### React Testing Library
- Write tests that interact with your components as a user would. Avoid testing implementation details.
- RTL provides a set of queries (`getBy`, `findBy`, `queryBy`, `getAllBy`, `findAllBy`, `queryAllBy`) to select elements. Choose the appropriate query based on your use case to interact with elements in your tests.
    - Use `getBy` selectors when you expect the element to be present in the DOM and you want your test to fail if the element cannot be found.
    - Use `queryBy` selectors when you're not sure whether the element will be present in the DOM or not, and you want your test to gracefully handle the absence of the element.
    - Use `findBy` selectors  you expect an element to appear in the DOM as a result of an asynchronous operation, such as data fetching, state updates, or component re-renders triggered by async events.
- Ensure your components are accessible by using RTL `getByRole`, `getByLabelText`, or `getByTestId` queries to test for accessible elements.

> You can find more detailed information about different kinds of selectors and their usages in the official [Jest][JestDocumentation] and [RTL][RTLDocumentation] documentation.

## Links
- [What is Test-Driven Development](https://www.browserstack.com/guide/what-is-test-driven-development)
- [Jest Documentation][JestDocumentation]
- [React Testing Library Documentation][RTLDocumentation]

[JestDocumentation]: https://www.browserstack.com/guide/what-is-test-driven-development
[RTLDocumentation]: https://jestjs.io/docs/getting-started