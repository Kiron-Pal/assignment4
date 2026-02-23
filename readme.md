What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?

Ans - The primary difference lies in the specificity and the type of object returned. getElementById is the most restrictive but fastest, targeting a unique ID and returning a single Element. while, getElementsByClassName searches for all elements with a specific class and returns a live HTMLCollection, which automatically updates if the DOM changes.

QuerySelector and QuerySelectorAll are the "Swiss Army Knives" of the group; they use CSS selector syntax (e.g., .class, #id, div > p), making them the most versatile. While
QuerySelector returns only the first match, querySelectorAll returns a static NodeList. Unlike the live collection from the class name method, a static NodeList does not update when elements are added or removed from the document after the search is performed.