opacity applies to the element as a whole, including its contents, even though the value is not inherited by child elements. Thus, the element and its children all have the same opacity relative to the element's background, even if they have different opacities relative to one another.

If you do not want to apply opacity to child elements, use the background property instead. Ex; background: rgba(0, 0, 0, 0.4);
