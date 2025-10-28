# Styling the Header and Navigation Bar

In this section, we’ll work on positioning and styling our website’s header and navigation so that the **page title** and **navigation links** sit neatly side by side — similar to the layout in the original website.

---

## Step 1: Understanding Block vs Inline Elements

By default, HTML elements have different display behaviors.

### Block Elements

The following elements in our header are **block-level elements**:

- `<h1>`
- `<nav>`
- `<ul>`
- `<li>`

> Block elements automatically take up the **entire width** of the screen.

### Inline Elements

- The `<a>` (anchor) tag is an **inline element**, meaning it **only takes up as much width** as its content (e.g., the link text).

You can confirm this behavior by inspecting the elements using **DevTools** — you’ll notice that block elements span the full width.

---

## Step 2: Making Header Elements Inline

Since we want the `<h1>` (page title) and `<nav>` (navigation) to appear on the **same line**, we’ll need to make them behave more like inline elements.

We do this using the CSS `display` property:

```css
h1 {
  display: inline-block;
}

nav {
  display: inline-block;
}

li {
  display: inline-block;
}
```

This ensures that the `<h1>`, `<nav>`, and each `<li>` (list item) appear side by side rather than stacking vertically.

---

### Note: About Repetition and the DRY Principle

You’ll notice we’re repeating `display: inline-block;` several times.

In **software engineering**, repetition like this breaks the **DRY principle** — _Don’t Repeat Yourself_.  
We aim to **avoid repetitive values** and keep our code clean and efficient.

We’ll explore **best practices in CSS organization**, including:

- Grouping selectors efficiently.
- Naming conventions for classes and IDs.
- When and how to use reusable utility classes.

For now, we’ll keep the code as is to maintain clarity.

---

## Step 3: Using Classes for Better Structure

Instead of styling all `<li>` elements globally, it’s better practice to **scope** your styles by wrapping them in a specific class.

In your HTML, add a class to the navigation:

```html
<nav class="nav-links">
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>
```

Then update your CSS to target that class:

```css
.nav-links {
  display: inline-block;
}

.nav-links li {
  display: inline-block;
}
```

This approach:

- Makes your code easier to **maintain**.
- Prevents unintentional styling of other `<li>` elements elsewhere on the page.
- Follows better **CSS scoping and naming practices**, which we’ll explore in depth next week.

---

## Step 4: Styling the Links

Now, let’s refine how the navigation links look.

We’ll:

- Remove underlines (`text-decoration`).
- Adjust spacing.
- Change the color.
- Tweak the font size.

Here’s the CSS for the links inside `.nav-links`:

```css
.nav-links a {
  color: black;
  text-decoration: none;
  font-size: 20px;
}
```

You can experiment with different values for `font-size` and `color` until you find what matches your design best.

---

## Step 5: Adding Spacing Between Links

We’ll space out the navigation links to make them more readable.  
For now, we’ll use simple margins:

```css
.nav-links li {
  display: inline-block;
  margin-right: 20px;
}
```

> ⚠️ In later sessions, we’ll explore **Flexbox** — a more powerful and modern way to align and distribute space between elements.

---

## ✅ Summary

| Concept                   | Description                                                                                       |
| ------------------------- | ------------------------------------------------------------------------------------------------- |
| **Block elements**        | Take full width by default (`h1`, `nav`, `ul`, `li`).                                             |
| **Inline elements**       | Only take as much width as their content (`a`).                                                   |
| **display: inline-block** | Allows elements to sit side-by-side while retaining block-like properties.                        |
| **DRY Principle**         | Avoid repeating CSS rules unnecessarily.                                                          |
| **Scoped styling**        | Use classes (like `.nav-links`) to keep styles organized.                                         |
| **Next up**               | We’ll explore **Flexbox** for layout control and learn best practices for CSS naming conventions. |
