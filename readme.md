1/ What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Ans - The primary difference lies in the specificity and the type of object returned. getElementById is the most restrictive but fastest, targeting a unique ID and returning a single Element. while, getElementsByClassName searches for all elements with a specific class and returns a live HTMLCollection, which automatically updates if the DOM changes.

QuerySelector and QuerySelectorAll are the "Swiss Army Knives" of the group; they use CSS selector syntax (e.g., .class, #id, div > p), making them the most versatile. While
QuerySelector returns only the first match, querySelectorAll returns a static NodeList. Unlike the live collection from the class name method, a static NodeList does not update when elements are added or removed from the document after the search is performed.


2/ How do you create and insert a new element into the DOM?

Ans- Use document.createElement() to generate the node in memory. At this stage, the element exists but is not yet visible on the page.


we must attach the created element to a parent node already present in the DOM using one of the following methods:

appendChild(): Adds the element as the last child of the parent.

prepend(): Adds the element as the first child of the parent.

before() / after(): Inserts the element relative to a specific sibling element.

insertAdjacentElement(): Offers precise control ('afterbegin', 'beforeend').


