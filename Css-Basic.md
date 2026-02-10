````markdown
# CSS Basics

## What is CSS?

**Cascading Style Sheets (CSS)** is a styling language used to apply styles to HTML elements.  
CSS is used to control:
- Colors  
- Background images  
- Layouts  
- Spacing  
- Overall visual presentation of web pages  

---

## Basic Anatomy of a CSS Rule

A CSS rule is made up of two main parts:

- **Selector**: A pattern used to identify and target specific HTML elements for styling.
- **Declaration Block**: A block that applies a set of styles to the selected elements.

### General Syntax

```css
selector {
    property: value;
}
````

---

## `<meta name="viewport">` Element

The `<meta name="viewport">` element gives the browser instructions on how to control a page’s dimensions and scaling on different devices, especially mobile phones and tablets.
It is essential for responsive web design.

---

## Default Browser Styles

Each HTML element has **default browser styles** (also known as *User Agent Styles*).
These usually include default values for:

* Margins
* Padding
* Font sizes

These defaults can be overridden using CSS.

---

## Inline, Internal, and External CSS

### Inline CSS

Inline styles are written directly inside an HTML element using the `style` attribute.

> Inline CSS is generally avoided due to poor maintainability and violation of separation of concerns.

#### Example

```html
<p style="color: red;">This is a red paragraph.</p>
```

---

### Internal CSS

Internal CSS is written inside `<style>` tags within the `<head>` section of an HTML document.
This approach is useful for small projects or quick demonstrations.

```html
<style>
  p {
    color: red;
  }
</style>
```

---

### External CSS

External CSS is written in a separate `.css` file and linked to the HTML document using the `<link>` element.
This is the **recommended approach** for most projects.

```html
<link rel="stylesheet" href="styles.css">
```

---

## Working With the `width` and `height` Properties

### Width Properties

* **`width`**: Specifies the width of an element.

  * Default value: `auto`
* **`min-width`**: Specifies the minimum width an element can have.
* **`max-width`**: Specifies the maximum width an element can have.

### Height Properties

* **`height`**: Specifies the height of an element.

  * Default value: `auto`
* **`min-height`**: Specifies the minimum height an element can have.
* **`max-height`**: Specifies the maximum height an element can have.

---

## Different Types of CSS Combinators

### Descendant Combinator

Targets elements that are descendants of a specified parent.

```css
ul li {
    background-color: yellow;
}
```

Targets all `li` elements inside `ul` elements.

---

### Child Combinator (`>`)

Targets elements that are **direct children** of a parent.

```css
.container > p {
    background-color: black;
    color: white;
}
```

Only `p` elements that are direct children of `.container` will be styled.

---

### Next-Sibling Combinator (`+`)

Targets an element that immediately follows another element.

```css
h2 + p {
    background-color: red;
}
```

Styles the first `p` element immediately after an `h2`.

---

### Subsequent-Sibling Combinator (`~`)

Targets all sibling elements that come after a specified element.

```css
ul ~ p {
    background-color: green;
}
```

Styles all `p` elements that are siblings of `ul` and come after it.

---

## Inline, Block, and Inline-Block Level Elements

### Inline-Level Elements

* Take up only as much width as needed
* Do not start on a new line
* Flow within text

**Examples:** `span`, `a`, `img`

---

### Block-Level Elements

* Start on a new line
* Take up full available width by default

**Examples:** `div`, `p`, `section`

---

### Inline-Block Elements

* Behave like inline elements
* Allow `width` and `height` to be set like block elements

```css
display: inline-block;
```

---

## Margin and Padding

### `margin` Property

Used to apply space **outside** an element, between its border and surrounding elements.

### `padding` Property

Used to apply space **inside** an element, between its content and border.

---

### Margin Shorthand

You can use 1–4 values:

* **1 value** → all sides
* **2 values** → top/bottom, left/right
* **3 values** → top, left/right, bottom
* **4 values** → top, right, bottom, left

```css
margin: 10px 20px 5px 15px;
```

---

### Padding Shorthand

Follows the same rules as margin shorthand.

```css
padding: 10px 20px;
```

---

## CSS Specificity

### Inline CSS Specificity

* Highest specificity
* Overrides all other styles
* Specificity value: **(1, 0, 0, 0)**

---

### Internal CSS Specificity

* Written inside `<style>` tags
* Lower priority than inline styles
* Can override external CSS

---

### External CSS Specificity

* Lowest priority
* Best for maintainability and scalability

---

### Universal Selector (`*`)

* Targets every element on the page
* Lowest specificity: **(0, 0, 0, 0)**
* Commonly used for resets

```css
* {
    margin: 0;
    padding: 0;
}
```

---

### Type Selectors

* Target elements by tag name
* Specificity: **(0, 0, 0, 1)**

```css
p {
    color: blue;
}
```

---

### Class Selectors

* Defined using a dot (`.`)
* Specificity: **(0, 0, 1, 0)**

```css
.button {
    background-color: green;
}
```

---

### ID Selectors

* Defined using a hash (`#`)
* High specificity: **(0, 1, 0, 0)**

```css
#header {
    background-color: black;
}
```

---

### `!important` Keyword

* Forces a style to override all others
* Should be used sparingly
* Makes CSS harder to debug and maintain

```css
p {
    color: red !important;
}
```

---

## Cascade Algorithm

The **Cascade Algorithm** determines which CSS rule is applied when multiple rules target the same element.
It considers:

1. Importance (`!important`)
2. Specificity
3. Source order (last rule wins)

---

## CSS Inheritance

CSS Inheritance allows child elements to receive styles from their parent elements automatically.
Common inheritable properties include:

* `color`
* `font-family`
* `font-size`

This reduces repetition and improves maintainability.

---

```

If you want, I can:
- Split this into **chapter-wise markdown files**
- Add **diagrams and visuals**
- Optimize it for **exam revision or GitHub documentation style**
- Convert it into **PDF or README.md format**
```
