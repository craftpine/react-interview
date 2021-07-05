| No  | Question                                                                 |
| --- | ------------------------------------------------------------------------ |
| 1   | [What are forward refs?](#q-1)                                           |
| 2   | [Why fragments are better than container divs?](#q-2)                    |
| 3   | [What are portals in React?](#q-3)                                       |
| 4   | [What are error boundaries in React?](#q-4)                              |
| 5   | [How to use innerHTML in React?](#q-5)                                   |
| 6   | [Can you force a component to re-render without calling setState?](#q-6) |
| 7   | [How React Router is different from history library?](#q-7)              |
| 8   | [What are the differences between call() and put() in redux-saga?](#q-8) |
| 9   | [In which scenarios error boundaries do not catch errors?](#q-9)         |

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

### <span id="q-4">4. What are error boundaries in React?</span>

Error boundaries are components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.

### <span id="q-5">5. How to use innerHTML in React?</span>

The `dangerouslySetInnerHTML` attribute is React's replacement for using `innerHTML` in the browser DOM. <br>
Just like `innerHTML`, it is **risky** to use this attribute considering cross-site scripting (XSS) attacks. <br>
You just need to pass a `__html` object as key and HTML text as value.

### <span id="q-6">6. Can you force a component to re-render without calling setState?</span>

you can tell React that the component needs re-rendering by calling forceUpdate()

### <span id="q-7">7. How React Router is different from history library?</span>

It also provides memory history which is useful for environments that don't have global history, such as mobile app development (React Native) and unit testing with Node.

### <span id="q-8">8. What are the differences between call() and put() in redux-saga?</span>

<ul>
    <li>call() function is used to create effect description, which instructs middleware to call the promise.</li>
    <li>put() function creates an effect, which instructs middleware to dispatch an action to the store.
    </li>
</ul>

### <span id="q-9">9. In which scenarios error boundaries do not catch errors?</span>

<ul>
    <li>Inside Event handlers</li>
     <li>Asynchronous code using setTimeout or requestAnimationFrame callbacks</li>
      <li>During Server side rendering</li>
       <li>When errors thrown in the error boundary code itself</li>
</ul>
