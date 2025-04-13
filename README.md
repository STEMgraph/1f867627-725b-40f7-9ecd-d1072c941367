<!---
{
  "id": "1f867627-725b-40f7-9ecd-d1072c941367",
  "depends_on": ["3ee0acd9-0f99-4423-b4f3-a0ca84a16422"],
  "author": "Stephan Bökelmann",
  "first_used": "2025-04-13",
  "keywords": ["HTML", "anchor", "a element", "hyperlink", "navigation"]
}
--->

# Introduction to HTML Anchor Elements

> In this exercise you will learn how to create and use anchor (`<a>`) elements in plain HTML. Furthermore we will explore different types of links and understand how navigation works inside a browser.

### Introduction

Anchor tags (`<a>`) are one of the oldest and most essential parts of HTML. They allow us to create hyperlinks—clickable text that leads to other pages, parts of the same page, or even triggers actions like sending an email. Understanding how they work is fundamental to web development.

In this exercise, we’ll use nothing more than `vim` and a web browser. You’ll write HTML files manually, save them, and open them in the browser to see what happens when you click on various kinds of links. You will also observe the browser’s default behaviors: page reloading, internal jumping, and how the address bar changes.

By the end, you’ll understand what `href` really does, what happens when the browser sees a link, and how this relates to more advanced systems like Angular’s routing. This is your first step toward thinking like the browser.

### Further Readings and Other Sources

- [MDN: HTML `<a>` element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a)
- [W3Schools on Links](https://www.w3schools.com/html/html_links.asp)
- [Video: HTML Anchor Tag Explained](https://www.youtube.com/watch?v=W6NZfCO5SIk)

### Tasks

#### Task 1: Create a Basic HTML File with Links

Open `vim` and create a file called `links.html`:

```bash
vim links.html
```

Paste the following HTML:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Anchor Tag Demo</title>
  </head>
  <body>
    <h1>My First Links</h1>
    <p><a href="https://example.com">Go to Example.com</a></p>
    <p><a href="page2.html">Go to Page 2</a></p>
    <p><a href="#section">Jump to Section</a></p>
    <h2 id="section">Target Section</h2>
    <p>This is where the in-page jump takes you.</p>
  </body>
</html>
```

Save and open the file in your browser, according to your platform. 

Try each link:
- The first one opens a new website.
- The second gives a file-not-found unless you create `page2.html`.
- The third scrolls you down to the `id="section"` header.

#### Task 2: Create a Second Page and Link Back

Still in `vim`, create a new file:

```bash
vim page2.html
```

Paste:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page 2</title>
  </head>
  <body>
    <h1>Welcome to Page 2</h1>
    <p><a href="links.html">Back to Main Page</a></p>
  </body>
</html>
```

Now your second link in `links.html` works too. You’ve created a real multi-page mini-site with plain HTML.

#### Task 3: Try an Email and Telephone Link

In `links.html`, add:

```html
<p><a href="mailto:hello@example.com">Email Us</a></p>
<p><a href="tel:+123456789">Call Us</a></p>
```

Test what happens when you click them. The behavior depends on your system setup (email client, phone app, etc.).

#### Task 4: Use an Anchor Without `href`

Add this to `links.html`:

```html
<p><a id="no-link">I'm just styled like a link</a></p>
```

Notice that this doesn’t act like a link — it has no `href`, so clicking it does nothing. But it's still styled as a hyperlink. This is common when JavaScript takes over the click behavior.

### Questions

1. What happens when you click a link with an `href`?
2. What is the difference between a link to a website and a link to another file?
3. What happens when a link uses `#`? Why?
4. What happens if an `<a>` element has no `href`?
5. What does the browser do differently when clicking an anchor with `mailto:` or `tel:`?

### Advice

Anchor tags may seem simple, but they’re incredibly powerful. They tell the browser where to go and when. Understanding how they trigger navigation, reloads, or in-page jumps gives you insight into how web applications work under the hood. This understanding is crucial when you move on to JavaScript-based routers like Angular’s — where the anchor is still present, but its behavior is intercepted and transformed. Practice here makes your understanding of future routing smoother and more intuitive.

