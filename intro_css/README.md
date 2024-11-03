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

**ID Selector** is similar to class selectors with the major difference being that an element can have only **one** ID whereas it can have multiple classes. Here, instead of a period, we prepend it with a hashtag. Generally, classes should be preferred over IDs.

```
<div id="alert">Some text</div>

#alert {
    background-color: blue;
}
```

**Grouping Selector** - if two grouups of elements have some of the same style declarations then they can just be declared together with a comma to separate them instead of declaring them separately and declare the rest as usual.

```
.read,
.unread {
    color: white;
    background-color: green;
}
```

**Chaining Selectors** is used if we want to set styles to elements that have the same set of classes/ID's. For example, if we want the element with both the subheading and title classes only to have a certain style then we can chain them as shown in the example provided below.

```
.subheading.title {
    color: red;
}
```

It can be used for chaining any combination of selectors except for chaining more than one type selectors.

**Descendant combinator** is used when you want to select elements belonging to a certain class only if they have a common ancestor. For example, if we want to select elements that have a class "child" nested in "ancestor", then only elements with the `child` class nested in `ancestor` class would be selected.

```
<div class="ancestor">
    <div class="son">
        <div class="child"><!-- some element --></div> 
    </div>
</div>
```

```
.ancestor .child {
    <!-- some declaration -->
}
```

Generally it's best to avoid selecting elements that need a lot of nesting since it can get confusing.
#