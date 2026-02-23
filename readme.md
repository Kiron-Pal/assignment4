1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Ans - The primary difference lies in the specificity and the type of object returned. getElementById is the most restrictive but fastest, targeting a unique ID and returning a single Element. while, getElementsByClassName searches for all elements with a specific class and returns a live HTMLCollection, which automatically updates if the DOM changes.

QuerySelector and QuerySelectorAll are the "Swiss Army Knives" of the group; they use CSS selector syntax (e.g., .class, #id, div > p), making them the most versatile. While
QuerySelector returns only the first match, querySelectorAll returns a static NodeList. Unlike the live collection from the class name method, a static NodeList does not update when elements are added or removed from the document after the search is performed.


2. How do you create and insert a new element into the DOM?

Ans- Use document.createElement() to generate the node in memory. At this stage, the element exists but is not yet visible on the page.


we must attach the created element to a parent node already present in the DOM using one of the following methods:

appendChild(): Adds the element as the last child of the parent.

prepend(): Adds the element as the first child of the parent.

before() / after(): Inserts the element relative to a specific sibling element.

insertAdjacentElement(): Offers precise control ('afterbegin', 'beforeend').


3. What is Event Bubbling? And how does it work?



Ans- In DOM manipulation, Event Bubbling is a type of event propagation where an event starts at the specific element that triggered it (the "target") and then flows upward through its ancestors in the DOM tree.

How It Works:

(1)Trigger: An action (like a click) occurs on a child element (e.g., a <button>).

(2)Ascension: The event handler for that button fires first.

(3)Propagation: The event "bubbles" up to the parent <div>, then the <body>, the <html> element, and finally the window object.


 4. What is Event Delegation in JavaScript? Why is it useful?

Ans- Event Delegation is a design pattern in JavaScript where you attach a single event listener to a parent element instead of attaching multiple listeners to individual child elements. It relies entirely on the principle of Event Bubbling. In addition, it is useful due to is memory efficiency, dynamic elements, cleaner code .




5. What is the difference between preventDefault() and stopPropagation() methods?
