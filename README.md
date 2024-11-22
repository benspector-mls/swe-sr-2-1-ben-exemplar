# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Do some research on semantic and non-semantic elements and share your findings. Your response should include:
* Examples of semantic and non-semantic tags
* The differences between semantic and non-semantic tags
* The benefits of using semantic tags (when possible)

### Response 1

Semantic tags have names that describe the content they contain. Tags like `<header>`, `<main>` and `<footer>` make it clear what role they play on a page and what content they contain. Meanwhile, tags like `<div>` and `<span>` are generic and could contain anything!

Semantic tags provide the benefit of readability since it is immediately obvious what the purpose of a semantic tag is. In addition, and perhaps more importantly, semantic tags help with accessibility because they help screen readers understand the structure of the web page, allowing them to provide shortcuts for users to navigate directly to the desired content.

## Prompt 2

Do some research on accessibility. What are some ways to make your website more accessible? Explain why it is important for developers to create websites that meet accessibility standards.

### Response 2

As mentioned above, using semantic tags is a great way to improve a page's accessibility. For users with poor vision, using highly readable fonts and color schemes that provide good contrast and that avoid common issues related to color blindness can be a great help. Lastly, adding `alt` text to images and adding `aria-label` attributes to elements will help blind users who require a screen reader to easily navigate your page.

It is essential that websites meet accessibility standards so that they can be accessed by users of all abilities.

## Prompt 3

It is possible to add "inline" CSS styles to our html elements using the `style` attribute like so:

```html
<p style="color: red;" >hello world</p>
```

While this is possible, it is a best practice to instead write styles in a separate CSS file. Provide at least one argument for why it _might_ be considered useful to write inline styles, and then provide a more compelling argument for writing styles in a separate CSS file.

### Response 3

Writing inline CSS styles may be quicker in the short term since you won't have to create a separate CSS file. You can also control how every single element is styled. 

However, it can quickly become highly repetitive and disorganized if you only use inline CSS styles. Instead, it is better to write CSS in a separate CSS file. By separating these concerns, it will be easier to focus on the content and structure of your page in your HTML files and on styling in the CSS page. In addition, with CSS, we can target entire groups of elements by their tag name or class to provide styles in a non-repetitive manner. 

## Prompt 4

Imagine you are teaching a brand new programmer a brief lesson about the `class` and `id` attributes in HTML as well as how to use them to style elements using CSS. Your lesson should have the following components:

* An explanation of the concept of "classes" and "ids" with an analogy.
* An example of the usage using an HTML code block and a CSS code block.
* An explanation of the syntax using the terms: **attribute**, **selector** 

### Response 4

In HTML and CSS, `class` and `id` are attributes that can be added to an HTML element to label that element. The `id` attribute labels a single element with a unique name while the the same `class` attribute can be given to many elements to label them as a part of the same group of elements.

For example, the `ul` below is given the unique `id` of `"posts-list"` while each `li` in the list is a part of the `post` class.

```html
<ul id="posts-list">
  <li class="post">I like coding!</li>
  <li class="post">Check out my coding blog</li>
  <li class="post">Tell me your favorite coding fact</li>
</ul>
```

In CSS, we can apply styles to elements with a particular `id` or `class` using the syntax `#id` and `.class`:

```css
#posts-list {
  list-style: none;
}

.post {
  padding: 1rem;
  font-style: italic;
}
```

In this example, the `#posts-list` selector targets the element with the attribute `id="posts-list"` while the `.post` selector targets all of the elements with the attribute `class="post"`.

## Prompt 5

The Document Object Model (DOM) API provides functions for manipulating HTML documents. It is possible to build an entire website using only JavaScript and the DOM API, however is that the best practice?

When building a website, how can I decide which content I should write using HTML/CSS and which content I should create using the JavaScript and the DOM API?

### Response 5

When building a website, it is a best practice to start by building the hard-coded structure and appearance of the website using HTML and CSS. Then, you can use the DOM API functions to insert content that needs to be generated programmatically. For example, you can use the DOM API to create a list of posts based on a dataset of posts or to modify the content of the page in response to a user event.
