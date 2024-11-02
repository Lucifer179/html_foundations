# Basic Syntax
CSS is made of rules. Rules are made up of -> selectors + property + value.
#
# Selectors
**Universal Selector** will select elements of any type and the syntax for it is an asterisk. By using a universal selector, every element would have the property specified with it.

```
* {
    color: green;
}
```

**Type Selector** selects all elements of the given element type and the syntax for it is the name of the element.

```
div {
    color: yellow;
}
```

**Class Selector** selects all elements with the given class. Class is just an attribute placed in an html element. It's prepended with a period and is case sensitive.

```
<div class="alert-text">Insert message here</div>

.alert-text {
    color: white;
}
```
