# Building the Header and Navbar

In this section, we’ll create the header for our website, which includes the main title (`h1`) and the navigation bar (`nav`).

---

## Step 1: Create the Header Structure

Start by creating the **header** section that will hold your page title and navigation links.

- The header typically includes your **website name or logo** (represented by an `<h1>` tag) and the **navigation menu**.
- The `<header>` element helps browsers and assistive technologies understand that this part of your page contains introductory or navigational content.

---

## Step 2: Use the Semantic `<header>` Element

It’s best practice to wrap your header content inside a **semantic** `<header>` tag instead of placing elements directly in the body.

> 🔗 Learn more about the `<header>` element on [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/header)

Replace your existing `<h1>` in `index.html` with this structure:

```html
<header>
  <h1>OptiFoodPhotography</h1>
</header>
```

### Why This Matters

- The `<h1>` tag represents the **main topic** of the page.
- There should be **only one `<h1>` element per page**, as it defines the central focus of your content.
- This practice improves **semantic structure**, **accessibility**, and **SEO (Search Engine Optimization)**.

---

## Step 3: Add the Navigation Links

Next, we’ll create navigation links that allow users to move through different sections of the page.

- We use the `<nav>` element to wrap our navigation links.  
  This is another **semantic element** that tells browsers and assistive technologies that this section is for page navigation.

You can place the `<nav>` element inside the `<header>` — a common layout convention:

```html
<header>
  <h1>OptiFoodPhotography</h1>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#portfolio">Portfolio</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
```

### Notes

- `<ul>` creates an unordered list that holds each navigation item (`<li>`).
- Each `<a>` (anchor) tag represents a clickable link that directs to a specific section of the page.
- The `#` symbol in the `href` attribute references a section ID within the same page.

---

## Step 4: Prepare for Styling

Now that your markup structure is complete, your header and navigation are semantically correct and ready to be styled.

In the **next steps**, we’ll focus on:

- Adding CSS styles to position and format the navbar.
- Making it visually appealing

---

✅ **Summary**

- Use `<header>` to group your site’s introductory or navigational content.
- Always include one `<h1>` per page for clarity and SEO.
- Use `<nav>` inside `<header>` for structured, semantic navigation.
