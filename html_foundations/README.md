# HTML vs CSS vs Javascript
- HTML (Hypertext Markup Language) is what contains all the information in a webpage. All the text, links, buttons. Hypertext means text that can link to other things like different parts in the same page.

- CSS (Cascading Style Sheets) is what gives _style_ to those elements. It positions them, gives them colour, changes font, etc. 

**Note:** CSS is mainly used to create _static_ visual effects.

- Javascript brings in interactivity in a webpage. It allows you to change HTML and CSS elements to match your specifications.
#
# Elements and Tags
Most elements are wrapped in opening and closing HTML tags. For example, a paragraph is enclosed in `<p>` `</p>` tags. So, the three parts of an HTML element are the opening tag, the actual content inside it and the closing tag. 

Some elements that don't have closing tags are called **Void Elements**. Examples include `<br>` and `<img>`. They're void elements because they don't have any content inside them. 
#
# HTML Boilerplate
**Note:** We should always name our file containing the homepage of our website as `index.html` as web servers by default look for an `index.html` page for when users land on our websites.

A _doctype's_ purpose is to tell the browser which version of HTML it should use to render the document. The doctype for HTML 5 (the latest version) is `<!DOCTYPE html>`.

After declaring the doctype, we have to provide an `<html>` element that everything else in the document will be enclosed in. `lang` specifies the language of the text content which is useful for assistive technologies like screen readers to adapt to the correct language and invoke correct pronunciation.

The `<head>` element is where we put metadata about our webpages. We should **not** put any element that displays content on the webpage. The `<meta>` tag is always within the `<head>` element and is used to set the charset encoding of the webpage which ensures that special symbols are displayed properly in the webpage.

The `<title>` tag is what is displayed for the users as the name of the webpage when we see it in the tabs list.

The `<body>` tag is where the all the content displayed on a webpage goes. 

In summary, the complete boilerplate has the DOCTYPE element, `<html>` element in which everything is enclosed, `<head>` element that contains metadata about the webpage, `<title>` element inside `<head>` and finally the `<body>` element where all the content goes.
#
# Working With Text
- Headings range from `<h1>` to `<h6>` in terms of size and boldness.

The `<strong>` element makes text bold alongside semantically marking the text as important. The difference between simply bold and strong element is that bold only makes the text thicker and strong makes the text thicker _and_ tells the browser that the text inside it is important.

The `<em>` element makes text italic.
# 
# Lists
`<ul>` is used to make an unordered list (with bullet points). 

`<ol>` is used to make a ordered (numbered) list. 

Each item of a list is enclosed in `<li>` and `</li>` tags.
#
# Links and Images
To link something, we first use an anchor element that contains some text that the link would be anchored to. This is done using the `<a>, </a>` tags. Then, to include the link of we can do `<a href="https://some-link.com"> My anchor </a>`. 

Here, `href` stands for Hypertext Reference and is an _HTML attribute_. An HTML attritbute gives additional information to an HTML element and always goes in the element's opening tag. It's usually made up of two parts - a name and a value. In the example above, the value of `href` is the destination we want our link to go to.

A link by default would open in the same tab as the webpage containing it. To change that, we can add a `target` attribute to the anchor element. If we set the value of target as "_blank" then it would open in a new tab or window. Ex: `<a href="https://some-link.com" target="_blank" rel="noopener noreferrer"> My anchor </a>`. The `noopener` and `noreferrer` values for the `rel` attribute mean that the opened link cannot gain access to the webpage from which it was opened and it cannot know which webpage has linked it respectively.

**Absolute links** are links to other websites on the internet. It has to have the protocol and domain of the destination. 

**Relative links** are links to other pages in our website. It does not include the domain name, only the file path to the other page relative to the page the link is in.

For inserting an image, the `<img>` element is used with the src attribute to show the browser where the image is located.

The alt attribute is used to describe an image and is used in place of the image if it fails to load. It also tells visually impaired users what the image is supposed to be when used with screen readers. 

The height and width of the image can be defined using the same attributes. If we specify just one then it'll scale proportionally while defining both will stretch the image.
#