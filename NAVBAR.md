1. Create the header with its content, i.e. navbar items(h1 and the navigation links)
2. Use the industry standard where we use the header element to wrap our navbar items and header contnet. Read kore about the header element at https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/header
   In index.html, remove the h1 element and make a header element and inside of it put h1 element like below. h1 is the most important and central topic of the page. In web develpment standards, ensure that you have only one h1 element per page. This will help in terms of making your page semantically correct, accessible and SEO friendly.
   <header>
   <h1>OptiFoodPhotography</h1>
   </header>
3. Work on the page navigation links. We shall wrap them in a nav element. It is also one of the semantic elements. We will get to dive deeper into semantic elements during class. The nav element can be placed on the header, on the side of the page or even the footer section of the page.
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

4. In the next steps, we will begin to style our navbar. 