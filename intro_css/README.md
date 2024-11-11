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

**Grouping Selector** - if two groups of elements have some of the same style declarations then they can just be declared together with a comma to separate them instead of declaring them separately and declare the rest as usual.

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

# Some Basic Properties

### Colour
Colour simply be the name of the actual colour, or it can be a HEX, RGB or HSL value - each of which can be implemented in the following ways:

**Name**
```
p {
    color: red;
}
```

**HEX**
```
p {
    color: #1100ff;
}
```

**RGB**
```
p {
    color: rgb(0, 10, 123);
}
```

**HSL**
```
p { 
    color: hsl(15, 23%, 64%);
}
```
#
### Typography and text-align
`font-family` - for specifying font. Generally, provide a fallback font to the one you want in case the browser can't support it like so: `font-family: "Times New Roman", serif;`.

`font-size` will specify the size of the font. It should be of the format `font-size 142px`, where "px" and the size doesn't have any space between it. 

`font-weight` affects boldness of the text. It can be just a keyword like "bold" or a number ranging from 1-1000. For reference, 700 is the equivalent of bold.

`text-align` aligns the text horizontally within an element. Common keywords like "center" work here.
#

### Image Height and Width
By default, the image's dimensions will be of the original. But if we wanted to change it without stretching it then we can specify one dimension and put the other as "auto".
```
img {
    height: 250px;
    width: auto;
}
```
It's best to specify the height and width even if we don't plan on changing it since it'd take longer to load otherwise.
#
# Adding CSS to HTML
### External CSS
The most common way to do it is just to create a separate CSS file and linking it in the head tag with the link element.
```
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```
Here, the `rel` attribute species the relationship between the HTML file and the linked file.
### Internal CSS
Adding CSS elements in the HTML file itself. Here, you place all CSS elements within `<style>` tags, which are then placed in `<head>` tags.
### Inline CSS
CSS elements are placed inside the opening tag of the element itself. It generally works if you wanna add a unique style for a _single_ element. 

It generally isn't preferred though because it can get quite messy quite quickly and any inline CSS will override the other two methods which can cause unexpected results.
#