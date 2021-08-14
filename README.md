### <span id="q-0">React Interview</span>

| No  | Question                                                                                                   |
| --- | ---------------------------------------------------------------------------------------------------------- |
| 1   | [What are forward refs?](#q-1)                                                                             |
| 2   | [Why fragments are better than container divs?](#q-2)                                                      |
| 3   | [What are portals in React?](#q-3)                                                                         |
| 4   | [What are error boundaries in React?](#q-4)                                                                |
| 5   | [How to use innerHTML in React?](#q-5)                                                                     |
| 6   | [Can you force a component to re-render without calling setState?](#q-6)                                   |
| 7   | [How React Router is different from history library?](#q-7)                                                |
| 8   | [What are the differences between call() and put() in redux-saga?](#q-8)                                   |
| 9   | [In which scenarios error boundaries do not catch errors?](#q-9)                                           |
| 10  | [What is the difference between useCallBack and useMemo?](#q-10)                                           |
| 11  | [What's the difference between fork and spawn in redux-saga?](#q-11)                                       |
| 12  | [[JS] - What are the differences between undeclared and undefined variables?](#q-12)                       |
| 13  | [[JS] - How do you test for an empty object?](#q-13)                                                       |
| 14  | [[JS] - How do you compare two date objects?](#q-14)                                                       |
| 15  | [[JS] - What are the difference between ( for… in ), ( for… of ) and forEach statements?](#q-15)           |
| 16  | [[JS] - How to track javascript error from client side?](#q-16)                                            |
| 17  | [[JS] - How to differentiate between deep and shallow copies? How to deep copy javascript object ?](#q-17) |
| 18  | [[JS] - What are the difference between `call`, `bind`, `apply`?](#q-18)                                   |
| 19  | [[JS] - What is the `arguments javascript`?](#q-19)                                                        |
| 20  | [ [JS] - What is the `Array-like`?](#q-20)                                                                 |
| 21  | [When to choose useReducer over useState?](#q-21)                                                          |
| 22  | [How to increase performance of react app?](#q-22)                                                         |
| 23  | [[JS] - What are the difference between `Event delegation` and `Event bubbling`](#q-23)                    |
| 24  | [How to use innerHTML in React?](#q-24)                                                                    |
| 25  | [Is it possible to use react without JSX?](#q-25)                                                          |
| 26  | [How to prevent a function from being called multiple times, onClick, onScroll?](#q-26)                    |
| 27  | [How to prevent unnecessary updates using setState?](#q-27)                                                |

### <span id="q-1">1. What are forward refs?</span>

Ref forwarding is a feature that lets some components take a ref they receive, and pass it further down to a child.

### <span id="q-2">2. Why fragments are better than container divs?</span>

<ul>
    <li>Fragments are a bit faster and use less memory by not creating an extra DOM node. This only has a real benefit on very large and deep trees.</li>
    <li>Some CSS mechanisms like Flexbox and CSS Grid have a special parent-child relationships, and adding divs in the middle makes it hard to keep the desired layout.</li>
    <li>The DOM Inspector is less cluttered.</li>
</ul>

### <span id="q-3">3. What are portals in React?</span>

Portal is a recommended way to render children into a DOM node that exists outside the DOM hierarchy of the parent component.

> ReactDOM.createPortal(child, container)

The first argument is any render-able React child, such as an element, string, or fragment. The second argument is a DOM element.
<br>
[↥ back to top](#q-0)

### <span id="q-4">4. What are error boundaries in React?</span>

Error boundaries are components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.
<br>
[↥ back to top](#q-0)

### <span id="q-5">5. How to use innerHTML in React?</span>

The `dangerouslySetInnerHTML` attribute is React's replacement for using `innerHTML` in the browser DOM. <br>
Just like `innerHTML`, it is **risky** to use this attribute considering cross-site scripting (XSS) attacks. <br>
You just need to pass a `__html` object as key and HTML text as value.
<br>
[↥ back to top](#q-0)

### <span id="q-6">6. Can you force a component to re-render without calling setState?</span>

you can tell React that the component needs re-rendering by calling forceUpdate()
<br>
[↥ back to top](#q-0)

### <span id="q-7">7. How React Router is different from history library?</span>

It also provides memory history which is useful for environments that don't have global history, such as mobile app development (React Native) and unit testing with Node.
<br>
[↥ back to top](#q-0)

### <span id="q-8">8. What are the differences between call() and put() in redux-saga?</span>

<ul>
    <li>call() function is used to create effect description, which instructs middleware to call the promise.</li>
    <li>put() function creates an effect, which instructs middleware to dispatch an action to the store.
    </li>
</ul>

[↥ back to top](#q-0)

### <span id="q-9">9. In which scenarios error boundaries do not catch errors?</span>

<ul>
    <li>Inside Event handlers</li>
     <li>Asynchronous code using setTimeout or requestAnimationFrame callbacks</li>
      <li>During Server side rendering</li>
       <li>When errors thrown in the error boundary code itself</li>
</ul>

[↥ back to top](#q-0)

### <span id="q-10">10. What is the difference between useCallBack and useMemo?</span>

`useCallback` returns its function uncalled so you can call it later, while `useMemo` calls its function and returns the result.

[↥ back to top](#q-0)

### <span id="q-11">11. What's the difference between fork and spawn in redux-saga??</span>

-   **fork** creates a child from the calling process.
-   **spawn** creates a new child from the calling process.

[↥ back to top](#q-0)

### <span id="q-12">12. What are the differences between undeclared and undefined variables? <span>

| undeclared                                                                                  | undefined                                                                              |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| These variables do not exist in a program and are not declared                              | These variables declared in the program but have not assigned any value                |
| If you try to read the value of an undeclared variable, then a runtime error is encountered | If you try to read the value of an undefined variable, an undefined value is returned. |

[↥ back to top](#q-0)

### <span id="q-13">13. [JS] - How do you test for an empty object? </span>

```
Object.keys(obj).length === 0 && obj.constructor === Object
```

Since date object length is 0, you need to check constructor check as well

[↥ back to top](#q-0)

### <span id="q-14">14. [JS] - How do you compare two date objects? </span>

You need to use date.getTime() method to compare date values **instead of** comparison operators (==, !=, ===, and !== operators)
<br>
[↥ back to top](#q-0)

### <span id="q-15">15. [JS] - What are the difference between ( for… in ), ( for… of ) and forEach statements? </span>

-   `for in` allows you to access the index of the array rather than the actual element, so you need to use `array[i]` to get the value
-   `for of` allows you to access the value of the array
-   `forEach` allows you to access the both of value and index
-   `for in` allows you to access the element with the key is not a number
-   `for in` and `forEach` ignore empty elements, `for of` is not:
-   The scope of this inside `for in`, and `for of` is the scope outside of these iterative constructs, `forEach` is not, unless you use arrow function
-   Can not use the `await` and `yield` inside the `forEach` statement
    <br>
    [↥ back to top](#q-0)

### <span id="q-16">16. [JS] - How to track javascript error from client side? </span>

`Window: error event`
<br>
[↥ back to top](#q-0)

### <span id="q-17">17. [JS] - How to differentiate between deep and shallow copies? How to deep copy javascript object ?</span>

-   A deep copy: all of the values of the new variable are copied and **disconnected** from the original variable
-   A shallow copy: that certain (sub-)values are still **connected** to the original variable
-   Deep copy method: `JSON.parse()`, `lodash`, `recursion`

[↥ back to top](#q-0)

### <span id="q-18">18. [JS] - What are the difference between `call`, `bind`, `apply`? </span>

-   `call`, `apply` and `bind` are used to invoke functions and the first parameter will be used as the value of this within the function
-   `call` takes in comma-separated arguments as the next arguments
-   `apply` takes in an array of arguments as the next argument
-   `bind` return a new function
    <br>
    [↥ back to top](#q-0)

### <span id="q-19">19. [JS] - What is the arguments javascript? </span>

`Arguments` is an `Array-like` object You can use arguments instead of parameterized functions. the arguments are like an array but not really an array
<br>
[↥ back to top](#q-0)

### <span id="q-20">20. [JS] - What is the `Array-like`? </span>

`Array-like` means that arguments has a `length` property and properties `indexed` from zero, but it doesn't have Array's built-in methods like `forEach()` or `map()`, ....
<br>
[↥ back to top](#q-0)

### <span id="q-21">21. When to choose useReducer over useState? </span>

-   If there are many states dependent on each other.
-   If the state is a complex object.

[↥ back to top](#q-0)

### <span id="q-22">22. How to increase performance of react app?</span>

-   **Use Dynamic Imports/ Code-Splitting**: Lets your application download only the chunk required to run the current page, and later request back to the server for chunks required on page transition.
-   **Don't add Unnecessary Div's**: use React.Fragment instead
-   **Avoid using Index as key to Map Function**
-   **Avoid Inline Function Definition in the Render Function**: because the inline function will always fail the prop diff when React does a diff check.`({} !== {} // true)`
-   **Use React.Suspense and React.Lazy for Lazy Loading Components**
    <br>
    [↥ back to top](#q-0)

### <span id="q-23">23. [JS] - What are the difference between `Event delegation` and `Event bubbling`? </span>

| Event delegation                                                                                                                                                                                                            | Event bubbling                                                                                                                                |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Event delegation allows us to attach a single event listener, to a **parent element** , that will fire for all **descendants** matching a selector, whether those descendants exist **now** or are added in the **future**. | Event Bubbling is how events are **propagated** from the **child** DOM to the _parent_ DOM. Using `stopPropagation` to prevent this happening |

[↥ back to top](#q-0)

### <span id="q-24">24. How to use innerHTML in React? </span>

The **dangerouslySetInnerHTML** attribute is React's replacement for using **innerHTML** in the browser DOM
Note: **cross-site scripting (XSS)** attacks

`dangerouslySetInnerHTML={ __html: 'First &middot; Second' }`

[↥ back to top](#q-0)

### <span id="q-25">25. Is it possible to use react without JSX? </span>

`` React.createElement('div', null, `Hello ${message}`) ``

[↥ back to top](#q-0)

### <span id="q-26">26.How to prevent a function from being called multiple times, onClick, onScroll? </span>

-   **Throttling**: Changes based on a time based frequency.
-   **Debouncing**: Publish changes after a period of inactivity.

[↥ back to top](#q-0)

### <span id="q-27">27.How to prevent unnecessary updates using setState? </span>

If the values are same then you need to return **null** to stop re-rendering otherwise return the **latest** state value.

[↥ back to top](#q-0)
