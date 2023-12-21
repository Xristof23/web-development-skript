# Table of contents

## Week 1

- Github and Markdown
- HTML and the Web
- CSS Basics
- CSS Flexbox

---

---

# GitHub and Markdown

## Learning Objectives

- learning what version control is and why it is useful / important
- creating repositories on GitHub
- creating / editing files on GitHub
- creating commits on GitHub
- learning what Markdown is
- writing Markdown

---

## Markdown

The Markdown syntax allows writing formatted text (headlines, blockquotes, lists, etc.) that can be
stored in plain text. It is used by tools and websites like GitHub or Slack. It uses specific
characters to format parts of the text in a certain way.

### Markdown Examples

| Element                         | Markdown Syntax                         |
| ------------------------------- | --------------------------------------- |
| Level 1 headline                | `# Level 1 headline`                    |
| Level 2 headline                | `## Level 2 headline`                   |
| Level 5 headline                | `##### Level 5 headline`                |
| list item                       | `- list item`                           |
| [ ] done                        | `[ ] checkbox`                          |
| [x] done                        | `[x] checkbox`                          |
| **bold text**                   | `**bold text**`                         |
| _italicized text_               | `_italicized text_`                     |
| [link](https://www.example.com) | `[link text](https://www.example.com)`  |
| image                           | `![description of image](url to image)` |
| block quote                     | `> block quote`                         |
| divider                         | `---`                                   |
| `inline code block`             | `` `inline code block` ``               |
| `code block`                    | ` ``` code block ``` `                  |

See this [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) for
more Markdown Syntax.

---

## Git & Commits

Git is an open source version control system that:

- keeps track of all changes made to the source code
- enables developers to easily collaborate on the same project and exchange updates
- enables developers to go back to earlier versions of the source code

### Git Repositories

A Git repository is a place where a project is being saved. It keeps track of all versions of the
project files. Many people can have access to (and work on) the same repository.

### Commits

A commit is a **snapshot of your repository** at a specific point in time. Creating a commit in your
project is similar to hitting the **save** button in a video game.

You can always **go back to any prior commit** and will have all the project files as they were when
you made the commit.

Each commit has a message which should include a descriptive text, so that you and other developers
will know what changes the commit includes.

### Good commit messages

Writing good commit message is an art form in itself. Try to stick to the following rules:

- Be short and descriptive
- Always use english
- The first word should be a verb: "add", "fix", "remove", etc.
- Use imperative and present tense: "add shop page" instead of "added shop page"
- Do not end your commit message with a period
- When in doubt, describe **why** you did something instead of **how**: "fix typo" instead of
  "replaced the letter a with an e in the second word"

Your commit messages are a protocol of all changes made to the code base. Other developers should be
able to understand what happened by reading the commit messages.

---

## GitHub

GitHub is an online platform where you can store, share and collaborate on **remote** git
repositories. With GitHub, the same codebase can be shared and edited across many collaborators.
Many repositories are open source, so you can view the code, create a copy, modify it or use it in
your own projects.

> 💡 Hint: Check out this huge
> [list of GitHub repositories](https://github.com/pawelborkar/awesome-repos) and see what you can
> find there.

At the same time GitHub is a social network for developers and companies. Your GitHub profile will
be a valuable public asset for your future career. You can get in contact with many open source
projects, developers and even companies via GitHub.

> 💡 Even though GitHub is the most popular online git platform, it is by far not the only one.
> There are several alternatives to GitHub, i.e Gitlab or Bitbucket.

<br>
<br>

---

## Resources

- [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- [GitHub Profile Readme](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)
- [List of awesome GitHub profile readmes](https://github.com/abhisheknaiidu/awesome-github-profile-readme)

---

---

# HTML and the web

## Learning Objectives

- understanding client/server communication
- writing HTML code
- knowing about the importance of semantic HTML

---

## How the web works

The world wide web is a network of computers that can exchange information with each other. There
are many different protocols that define the rules on how machines communicate. Browsers use HTTP
(Hypertext Transfer Protocol) to communicate with web servers.

- The URL (Uniform Resource Locator) is the unique address of a resource on the web contains a human
  readable domain name, that needs to be resolved to the technical IP (Internet Protocol) address of
  the web server via a DNS (Domain Name Server)
- The browser sends a **GET** (that's an HTTP method) **request** to load a HTML (Hyper Text Markup
  Language) document from a web server
- The web server sends a **response** containing the document
- Often the HTML code contains references to additional resources (CSS (Cascading Style Sheet)
  files, images, etc.), which the browser then also requests from the server
- The browser **renders** the received content to the screen and makes it interactive
- Browsers might also request additional data from servers later via subsequent **GET** or **POST**
  requests

<img src="./assets/request-response.png" width=600 />

---

## HTML basics

HTML (Hyper Text Markup Language) is used to express text in a structured way. HTML tags indicate
what kind of element is displayed on the website. For example, a headline is written like this:

```html
<h1>I am a headline!</h1>
```

The content considered as headline is wrapped within an **opening tag** and a **closing tag**. The
whole thing is called an **element**.

Elements are nested into each other to create structure and hierarchy.

```html
<h1>I am a <em>headline!</em></h1>
```

Some elements can't contain any other elements and therefore don't have a closing tag. They are
self-closing and called
[_empty elements_](https://developer.mozilla.org/en-US/docs/Glossary/Empty_element).

```html
<hr />
or
<br />
```

### HTML tag attributes

Some elements require some more information in order to work properly. This information is
specified via attributes, for example:

- the source of an image
  ```html
  <img src="logo.png" alt="The logo of the company." />
  ```
- the destination of an anchor element
  ```html
  <a href="https://example.com"> click me </a>
  ```
- the type of an input element
  ```html
  <input type="date" />
  ```

> 💡 The [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes) contain
> detailed information about elements and corresponding attributes.

### Layout of an HTML file

Every HTML document starts with a
[doctype](https://developer.mozilla.org/en-US/docs/Glossary/Doctype) followed by the `<html>`
element, which consists of two main parts:

- The `<head>` contains important meta information for the browser like
  - the charset (utf-8)
  - the favicon displayed in the tab
  - the title of the website
  - CSS and JavaScript files needed for the website
- The `<body>` contains the visible content of the website structured by html elements

```html
<!DOCTYPE html>
<html>
  <head>
    … meta information, additional links to CSS / JavaScript files …
  </head>
  <body>
    … elements displayed on the web page …
  </body>
</html>
```

### List of common HTML elements

| element             | meaning                                                      |
| ------------------- | ------------------------------------------------------------ |
| `<head></head>`     | only once per website, includes meta data and linked files   |
| `<body></body>`     | only once per website, includes the html website content     |
| `<h1></h1>`         | only once per website, a level one heading                   |
| `<h2></h2>`         | a level two heading                                          |
| `<p></p>`           | a paragraph                                                  |
| `<a></a>`           | an anchor (link)                                             |
| `<img>`             | an image (self-closing / empty)                              |
| `<form></form>`     | a form element                                               |
| `<input>`           | an input field (self-closing / empty)                        |
| `<button></button>` | a clickable element equipped with some kind of functionality |

> 💡 A comprehensive [list of all html elements can be found at the MDN web docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element#inline_text_semantics).

---

## Structuring a Website

Developers have two main tools to express a meaningful structure in a website:

1.  Using semantic HTML elements
2.  Nesting / grouping of HTML elements

### Semantic HTML

Semantic HTML elements not only divide the content of the web page into distinct parts, but also
describe the function or purpose of the elements. This has two major benefits:

- The HTML becomes more understandable for other developers
- Accessibility tools and search engines can interpret the website

Therefore, one should use semantic HTML elements whenever possible.

### List of Semantic HTML elements

| element                 | meaning                                                                                                             |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `<main></main>`         | only once per website, includes the main content of the page                                                        |
| `<section></section>`   | a generic standalone section of a document                                                                          |
| `<ul></ul>`/`<ol></ol>` | a list of elements with the same structure, only has `<li>` elements as direct children                             |
| `<nav></nav>`           | a navigation bar                                                                                                    |
| `<aside></aside>`       | element representing a portion of a document whose content is only indirectly related to the main content           |
| `<article></article>`   | representing a self-containing part of the website, which is intended to be independently distributable or reusable |
| `<header></header>`     | representing introductory content, typically a group of introductory or navigational aids                           |
| `<footer></footer>`     | typically contains information about the author of the section, copyright data or links to related documents        |

> 💡 You can find a comprehensive [list of semantic html elements in the MDN web docs](https://developer.mozilla.org/en-US/docs/Glossary/Semantics).

### Nesting HTML elements

Nesting groups elements together in a meaningful way. The element containing the other elements is
called the **parent element**, which contains one or more **child elements**.

The following cases are typical examples of nested elements:

- ```html
  <ul>
    <li>first item</li>
    <li>second item</li>
    <li>third item</li>
  </ul>
  ```
- ```html
  <article>
    <h2>Some headline</h2>
    <p>I am a paragraph…</p>
    <a href="https://www.github.com">a link to another website</a>
  </article>
  ```
- ```html
  <button>
    <img src="arrow.svg" />
    <span> submit </span>
  </button>
  ```

Below is a sketch of how semantic elements can be nested in a web page.<br><br>
<img src="./assets/sectioning-elements.png" width=700 />

## Emmet

Visual Studio Code has a useful tool called Emmet which lets you autocomplete a lot of code by just
typing certain snippets and pressing the <kbd>Tab</kbd> key afterwards. Try these snippets inside an
HTML file and see what happens:

- `!`
- `.highlight`
- `button#red`
- `ul>li.card\*10`

> 💡 You can learn about more Emmet commands in
> [this cheat-sheet](https://docs.emmet.io/cheat-sheet/)

---

## Resources

- [MDN: Introduction to HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML)
- [MDN: Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
- [MDN: HTML Elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [MDN: Semantic elements: Glossary](https://developer.mozilla.org/en-US/docs/Glossary/Semantics)
- [MDN: HTML attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes)

---

---

# CSS Basics

## Learning Objectives

- [ ] having a general understanding of the purpose of CSS
- [ ] knowing what Cascading Style Sheets means
- [ ] understanding the fundamentals of CSS: CSS syntax, selectors, box model,
      inline & block elements
- [ ] linking stylesheets to the HTML document

## What is CSS?

With CSS (_Cascading Stylesheets_) you can add styling to your HTML elements.

![Comparison of HTML, CSS and JavaScript](assets/animated-gif-for-comparison.gif)

The term _cascading_ in CSS refers to an algorithm that resolves conflicts when multiple styles are defined for a particular element. When deciding which style to apply, CSS takes into account three key factors: specificity, source order, and inheritance.

- Specificity refers to how precisely a selector targets an element. Styles with higher specificity take precedence over those with lower specificity.

- The source order of styles also plays a role in determining which style should be applied. When multiple styles with the same specificity are defined, the style that appears last in the stylesheet will override any previous styles for that element.

- Additionally, CSS allows styles to be inherited from parent elements to their child elements. This means that certain styles can be passed down through the document tree, affecting multiple elements simultaneously.

The term _stylesheet_ refers to a collection of rulesets declared using CSS, usally within a `.css` file.

## Linking Stylesheets

To separate your HTML and CSS code, you can create a new file, like `css/styles.css` and link it to
your HTML file by placing a `<link>` tag in the `<head>` of your HTML document.

```html
<head>
  …
  <link rel="stylesheet" href="css/styles.css" />
</head>
```

## CSS syntax

Any stylesheet consists of a collection of **ruleset**s. A ruleset consists of four parts:

![CSS syntax](assets/css-syntax.png)

|                | Description                                                                                                              |
| -------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Selector       | Selects to which elements the style declarations are applied, followed by curly braces (`{}`) enclosing the declarations |
| Declaration    | A combination of a property and a property value, separated by a colon (`:`) and ending with a semicolon (`;`)           |
| Property       | The property you want to style, e.g. `color`, `font-size`, `text-align`                                                  |
| Property Value | The value assigned to the property, e.g `blue` for the `color` property, `3rem` for the `font-size` property             |

A ruleset can have multiple declarations:

```css
h1 {
  color: blue;
  font-size: 3rem;
  text-align: center;
}
```

## Selectors

There are different CSS selectors you can use to select elements to which you want to apply styles.

### Type selector

The type selector selects all elements of a specific element type.

**Syntax**: `article`, `h1`, `p`, `div`, `a`, `input`, `button`, …

**Example**:

Select all `article` elements.

```css
article {
  color: red;
}
```

```html
<article>…</article>
```

### Class selector

The class selector selects all elements that have the specified class.

**Syntax**: `.superpink` (the user defined class name from the HTML but starting with a dot `.`)

**Example**:

Select all elements with the class `superpink`.

```css
.superpink {
  color: hotpink;
}
```

```html
<aside class="superpink">…</aside>
```

HTML elements can have multiple classes separated by a space. The selector `.superpink` would
also select the following element:

```html
<aside class="broccoli superpink some-other-class">…</aside>
```

The order of the classes in the HTML attribute doesn't matter.

### Pseudo-classes

The pseudo-class selector selects all elements that are in a specific state. It is used in combination with other selectors.

**Syntax**: `:hover`, `:focus`, … (the pseudo-class name starting with a colon `:`)

#### `:hover`

Selects an element when you hover over it with the mouse.

**Example**:

Select all hovered links.

```css
a:hover {
  color: hotpink;
}
```

```html
<a href="https://www.neuefische.de">neuefische</a>
```

#### `:focus`

Selects an element when it is focused. This is usually the case when you click into an input field or select an element with the tab key.

**Example**:

Select all focused input fields.

```css
input:focus {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

#### Other pseudo-classes

There are many more pseudo-classes like `:active`, `:first-child`, `:last-child`, `:first-of-type`, `:last-of-type`, `:nth-child()`, `:nth-of-type()`, `:not()`, …

> 📙 You can find a list of all [**Pseudo-classes** on mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

### Attribute selectors

The attribute selector selects all elements based on the presence or value of a given attribute.

#### Basic attribute selector

Selects all elements with the specified attribute.

**Syntax**: `[attribute]` (attribute name in square brakets `[]`)

**Example**:

Select all elements that have a `type` attribute.

```css
[type] {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

#### Attribute value selector

Selects all elements with the specified attribute and value.

**Syntax**: `[attribute="value"]` (attribute name followed by `=` and the attribute value in quotation marks `""` — all in square brakets `[]`)

**Example**:

Select all elements that have a `type` attribute with the value `text`.

```css
[type="text"] {
  border: 1px solid hotpink;
}
```

```html
<input type="text" />
```

#### Advanced attribute selectors

With advanced attribute selectors you can also select elements that have an attribute with a
specific value at the beginning, end or in the middle of the value.

> 📙 You can find more information about [**Attribute selectors** on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors).

### Universal selector

The universal selector `*` selects all elements in the document.

**Syntax**: `*`

**Example**:

Select all elements.

```css
* {
  border: 1px solid hotpink;
}
```

> ❗️ The universal selector is rarely used for anything but resets. Do not use it unless you know what you are doing.

## Combining Selectors

Combinators are used to combine multiple selectors to create a new selector.

### Combine multiple selectors with a comma

You can combine multiple selectors with a comma to create a new selector that selects all elements that are selected by **any one** of the selectors.

**Syntax**: `selector1, selector2, …`

**Example**:

Select all `h1`, `h2` and `h3` elements.

```css
h1,
h2,
h3 {
  color: hotpink;
}
```

### Descendant combinator

The descendant combinator ` ` (space) selects all elements that are descendants (children) of another selector.

**Syntax**: `selector1 selector2 …`

**Example**:

Select all `.superpink` elements that are descendants of an `article` element.

```css
article .superpink {
  color: hotpink;
}
```

```html
<article>
  <p class="superpink">I am pink</p>
  <p>I am not pink</p>
  <footer>
    <p class="superpink">
      I am pink, even though I am not a direct descendant of the article
    </p>
  </footer>
</article>
<p class="superpink">
  I am not pink because I am not a descendant of an article
</p>
```

### Other combinators

There are many more combinators like the direct descendant combinator `>`, the adjacent sibling combinator `+` and the general sibling combinator `~`. A good general rule is to use combinators (except the comma to combine selectors) very sparingly and only when necessary.

> 📙 You can find more information about [**Combinators** on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors#combinators).

## CSS Properties

There are a lot of CSS properties and you will discover new ones every day. Therefore the following list shows only a few examples:

| Property           | Effect                                         |
| ------------------ | ---------------------------------------------- |
| `color`            | Color of an elements text                      |
| `font-size`        | Defines the size of a font                     |
| `text-align`       | Defines the alignment of text                  |
| `background-color` | Background color of an element                 |
| `border`           | Defines the border of an element.              |
| `padding`          | Defines the padding of an element.             |
| `margin`           | Defines the margin of an element.              |
| `width`            | This property defines the width of an element. |

> 📙 You can find more properties in the [alphabetic list of **Properties** on CSS-Tricks](https://css-tricks.com/almanac/properties/)
> or in the [**Index** of properties, pseudo-classes, pseudo-elements, data types, functional notations and at-rules on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#index).

## Inheritance

Some CSS properties are inherited from the parent element to the child element. This means that the child element inherits the value of the property from the parent element if it is not set explicitly.

**Example**:

```css
body {
  color: hotpink;
}

p {
  /* The color of the paragraph is hotpink because it is inherited from the body */
}
```

```html
<body>
  <p>I am hotpink</p>
</body>
```

This is very useful for properties like `color` or `font-family` because you can set them on any element and all child elements will inherit the value.

> 📙 You can find more information about [**Inheritance** on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/inheritance).

## Box Model

All elements of a website are rectangular boxes described by the **box model**. Each of those boxes has four areas: content, padding, border and margin.

| Box model part | Function                                                               |
| -------------- | ---------------------------------------------------------------------- |
| margin         | The outer space measured from the border to other elements on the page |
| border         | The border of the element                                              |
| padding        | The inner space between the content and the border of the element      |
| content        | The actual content box of the element                                  |

<img src="./assets/box-model.excalidraw.png" width="500" alt="A chart describing the different boxes making up the box model">

The browser knows two ways to calculate the size (`width` and `height`) of an element in this model: `content-box` (the default, old) and `border-box` (the modern variant).

In `content-box` mode, `width` and `height` only describe the size of the content box: The padding and border are added to the size of the element. This can be confusing and lead to unexpected results.

We can set the `box-sizing` property to `border-box` for all elements (using the universal selector) to make the `width` and `height` of an element include the padding and border box.

```css
* {
  box-sizing: border-box;
}
```

Now, the `width` property defines the size of the border box, padding and border width are
subtracted to calculate the available space for the content. This code will be in all used in all future projects to set a sensible default.

<img src="./assets/box-model-border-box-vs-content-box.excalidraw.png" width="768" alt="A chart describing the different boxes making up the box model">

> 💡 The CSS Working Group (which produces the specification for CSS) keeps an [**Incomplete List of Mistakes in the Design of CSS**](https://wiki.csswg.org/ideas/mistakes), saying that `box-sizing: border-box` should have been the default from the start.
>
> It is not possible to change the default behavior of `box-sizing` in the specification and in browsers (or fix any of the other "mistakes"), because it would break many websites that rely on the current behavior.

## Inline and block elements

There are basically two types of elements: inline-level and block-level elements.

### Inline elements

Inline elements **are as wide as their maximum content width** and **flow with the text lines**. They start and end within a line of text. Their box can be cut into multiple parts by line breaks.

Common inline elements include:

- `a`
- `span`
- `strong`
- `em`
- `img`
- `input`
- `button`
- …

### Block elements

Block elements **take up the full width of their parent element** and **always start on a new line**.

Common block elements are:

- `p`
- `h1` - `h6`
- `div`
- `section`
- `article`
- `header`
- `footer`
- `nav`
- …

### Example

In the following example, the `h2` and `p` elements are block-level elements. The `a` element is an inline-level element.

```html
<h2>Coding Bootcamp</h2>
<p>
  If you want to participate in a bootcamp, visit
  <a href="https://www.neuefische.de">neuefische.de</a>
</p>
```

### Display property

You can change the default behavior by using the CSS `display` property.

```css
h2 {
  display: inline;
}
```

This will make all `h2` elements behave like an inline elements. The same works the other way around:

```css
a {
  display: block;
}
```

This will make all `a` elements behave like a block elements.

## Resources

- [CSS on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS first steps on the mdn](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps)
- [Combinators on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors#combinators)
- [Alphabetic List of Properties on CSS-Tricks](https://css-tricks.com/almanac/properties/)
- [Index of properties, pseudo-classes, pseudo-elements, data types, functional notations and at-rules on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#index)
- [Inheritance on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/inheritance)
- [CSS styling text on the mdn](https://developer.mozilla.org/en-US/docs/Learn/CSS/Styling_text)
- [box-sizing on the mdn](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing?retiredLocale=de)
- [Incomplete List of Mistakes in the Design of CSS on the CSS Working Group Wiki](https://wiki.csswg.org/ideas/mistakes)

---

---

# CSS Flexbox

## Learning Objectives

- understanding the purpose of flexbox:
  - letting items fill out the possible space in their container
  - distributing elements for different screen sizes
  - making the website more responsive with flexbox
- understanding the most important flexbox properties
- knowing the difference between **main-axis** and **cross-axis**

---

## Flexbox

Flexbox is a powerful CSS tool to layout your HTML elements, especially when you want to align
elements horizontally. It is defined on a container element, containing multiple elements whose
position will be determined by the flexbox rules. You define it as follows:

```css
.container-element {
  display: flex;
}
```

Flexbox does the following:

- All child elements will be displayed next to each other along the main axis, the horizontal axis
  by default. The perpendicular axis is called cross axis.
- If the width of all child elements exceeds the container's width, the child elements will be
  shrunk such that they all fit into the available space.

This behavior can be modified to achieve some very useful layouts. The most important flex
properties are listed in the following table.

---

## Important Flex Properties

| property                                                                            | effect                                                                                                                                       |
| ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| [justify-content](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) | Defines the positioning of elements along the main axis. Useful values: `flex-start`, `flex-end`, `center` , `space-between`, `space-evenly` |
| [align-items](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)         | Defines the positioning of elements along the cross axis. Useful values: `flex-start`, `flex-end`, `center`                                  |
| [gap](https://developer.mozilla.org/en-US/docs/Web/CSS/gap)                         | Defines the minimum spacing between elements.                                                                                                |
| [flex-direction](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction)   | Sets the direction of the main axis. Useful values: `row`, `column`                                                                          |
| [flex-wrap](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap)             | Modifies how elements can wrap into another row instead of being squashed into one row. Useful values: `wrap`, `no-wrap`                     |

> 💡 [This very detailed cheatsheet](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
> includes everything you will ever need when working with flexbox.

---

## Flex-direction

This very fundamental property lets you define which axis should act as main axis. In this picture
you can see its effect.

![flex-direction](assets/flex-direction.png)

As you can see it changes the layout completely. Also notice, that the property `align-items`, which
defines the positioning on the cross axis, also changes with the definition of the flex-direction.

---

## Flex-wrap

This property is very useful for creating responsive layouts. With the property set to
`flex-wrap: wrap` the elements flow into the next row when they wouldn't fit into the current row.
Depending on the screen width, the content can align itself, as shown in the following example.

![flex-wrap](assets/flex-wrap.png)

---

### CSS Grid Layout

CSS Grid is another powerful tool to layout your HTML elements. While flexbox excels at laying out
elements in one dimension (if you ignore wrapped items), CSS Grid is used to layout elements in two dimensions.

> 📑 Learn more about [**CSS Grid Layout** in the document we prepared](./assets/css-grid.md).

---

## Resources

- [Flexbox Cheat Sheet](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [MDN web docs: Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
- [CSS Battle](https://cssbattle.dev/)
- [📑 CSS Grid Layout document](./assets/css-grid.md)
- [Flexbox playground](https://the-echoplex.net/flexyboxes/)
