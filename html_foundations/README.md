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