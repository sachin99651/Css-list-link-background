````markdown
# Lists, Links, Backgrounds, and Borders Review

---

## Styling Lists

### `line-height` Property

The `line-height` property is used to create space between lines of text.  
Accepted values include:
- `normal`
- Numbers (e.g., `1.5`)
- Percentages
- Length units like `em`

---

### `list-style-type` Property

The `list-style-type` property specifies the marker style for list items.  
Common values include:
- `disc`
- `circle`
- `square`
- `decimal`

#### Example

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
````

```css
ul {
  list-style-type: square;
}
```

---

### `list-style-position` Property

This property sets the position of the list marker relative to the content.

Accepted values:

* `inside`
* `outside`

#### Example

```html
<ul class="inside-list">
  <li>Item with inside position</li>
  <li>Item with inside position</li>
</ul>

<ul class="outside-list">
  <li>Item with outside position</li>
  <li>Item with outside position</li>
</ul>
```

```css
.inside-list {
  list-style-position: inside;
}

.outside-list {
  list-style-position: outside;
}
```

---

### `list-style-image` Property

This property replaces the list marker with an image.
It commonly uses the `url()` function.

```css
ul {
  list-style-image: url("marker.png");
}
```

---

### Spacing List Items Using Margin

Margins create space **outside** list items and improve readability.

* `margin-bottom` is commonly used to add space below list items.

#### Example

```html
<ul class="list">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

```css
.list li {
  margin-bottom: 20px;
}
```

---

## Styling Links

### Pseudo-Classes

A **pseudo-class** is a keyword added to a selector to style elements based on a specific state.

Common link-related pseudo-classes:

* `:link`
* `:visited`
* `:hover`
* `:focus`
* `:active`

---

### `:link` Pseudo-Class

Styles links that have **not yet been visited**.

```html
<a href="/">Example link</a>
```

```css
a:link {
  color: red;
}
```

---

### `:visited` Pseudo-Class

Styles links that the user has already visited.

---

### `:hover` Pseudo-Class

Styles elements when the user hovers over them.

```html
<a href="/">Hover over me!</a>
```

```css
a:hover {
  color: green;
  text-decoration: underline;
}
```

---

### `:focus` Pseudo-Class

Styles elements when they receive focus (via keyboard or mouse).

```html
<a href="/">Example link</a>
```

```css
a:focus {
  outline: 2px solid orange;
}
```

---

### `:active` Pseudo-Class

Styles elements while they are being activated (clicked).

```html
<a href="/">Click me!</a>
```

```css
a:active {
  color: pink;
}
```

---

## Working with Backgrounds

### `background-size` Property

Controls the size of the background image.

Common values:

* `cover`
* `contain`

```css
body {
  background-image: url("image.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}
```

---

### `background-repeat` Property

Controls how background images repeat.

Common values:

* `repeat` (default)
* `no-repeat`

```css
body {
  background-repeat: no-repeat;
}
```

---

### `background-position` Property

Specifies the position of the background image.

Values can include:

* Keywords (`top`, `center`, `bottom`, `left`, `right`)
* Percentages
* Length units

```css
body {
  background-position: center top;
}
```

---

### `background-attachment` Property

Controls whether the background scrolls with the page.

Values:

* `scroll` (default)
* `fixed`

---

### `background-image` Property

Sets the background image of an element.
Supports:

* `url()`
* `linear-gradient()`
* `radial-gradient()`

```css
body {
  background-image: url("image.jpg");
}
```

---

### `background` Shorthand Property

Allows multiple background properties to be set in one declaration.

```css
body {
  background: center top no-repeat url("image.jpg");
}
```

---

### Accessibility: Color Contrast

Good contrast between background and foreground colors is essential for readability.

**WCAG recommendations:**

* Normal text: **4.5:1**
* Large text: **3:1**

---

## Borders

### Individual Border Properties

* `border-top`
* `border-right`
* `border-bottom`
* `border-left`

```css
.bordered-box {
  border-top: 3px solid blue;
  border-right: 2px solid red;
  border-bottom: 1px dashed green;
  border-left: 4px dotted orange;
  padding: 20px;
}
```

---

### `border` Shorthand Property

Sets width, style, and color in one line.

```css
img {
  border: 2px solid red;
}
```

---

### `border-radius` Property

Creates rounded corners.

```css
img {
  border: 2px solid black;
  border-radius: 10px;
}
```

---

### `border-style` Property

Defines the style of the border.

Common values:

* `solid`
* `dashed`
* `dotted`
* `double`

```css
.solid-border {
  border: 3px solid blue;
}

.dashed-border {
  border: 3px dashed red;
}

.dotted-border {
  border: 3px dotted green;
}
```

---

## Gradients

### `linear-gradient()` Function

Creates a gradient along a straight line.

```css
.linear-gradient {
  background: linear-gradient(to right, red, blue);
  height: 40vh;
}
```

---

### `radial-gradient()` Function

Creates a gradient that radiates from a central point.

```css
.radial-gradient {
  background: radial-gradient(circle, red, blue);
  height: 40vh;
}
```

---

```

If you want, I can next:
- Merge this with your **CSS Basics** into a single `README.md`
- Add **exam-focused summaries**
- Create **separate chapters** (Lists.md, Links.md, Backgrounds.md, Borders.md) for a clean GitHub structure
```
