**Combinators and multiple selectors**

Using one selector at a time is useful, but can be inefficient in some situations. CSS selectors become even more useful when you start combining them to perform fine-grained selections. CSS has several ways to select elements based on how they are related to one another. Those relationships are expressed with combinators

Two ways of combining multiple selectors together for further useful selection capabilities.

**Combinators**
1. Descendant combinator - A descendant combinator is whitespace that separates two compound selectors. A selector of the form "A B" represents an element B that is an arbitrary descendant of some ancestor element A.

2. Child combinator - A child combinator describes a childhood relationship between two elements. A child combinator is made of the "greater-than sign" (U+003E, >) character and separates two compound selectors. Ex: body > p, where p is the immediate child of body. Other p element which do not comply this rule will be ignored. 

3. Next-sibling combinator - The next-sibling combinator is made of the "plus sign" (U+002B, +) character that separates two compound selectors. The elements represented by the two compound selectors share the same parent in the document tree and the element represented by the first compound selector immediately precedes the element represented by the second one. Non-element nodes (e.g. text between elements) are ignored when considering the adjacency of elements.

4. Following-sibling combinator - The following-sibling combinator is made of the "tilde" (U+007E, ~) character that separates two compound selectors. The elements represented by the two compound selectors share the same parent in the document tree and the element represented by the first compound selector precedes (not necessarily immediately) the element represented by the second one.

5. Reference combinators - The reference combinator consists of two slashes with an intervening CSS qualified name, and separates two compound selectors, e.g. A /attr/ B. The element represented by the first compound selector explicitly references the element represented by the second compound selector. Unless the host language defines a different syntax for expressing this relationship, this relationship is considered to exist if the value of the specified attribute on the first element is an IDREF or an ID selector referencing the second element. Attribute matching for reference combinators follow the same rules as for attribute selectors.                       
The following example highlights an <input> element when its <label> is focused or hovered-over:
`label:matches(:hover, :focus) /for/ input,       /* association by "for" attribute */
label:matches(:hover, :focus):not([for]) input { /* association by containment */
    box-shadow: yellow 0 0 10px; `
}`