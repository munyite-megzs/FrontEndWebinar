In this section, we shall finish up styling our header items. This is by changing the h1 font-weight and text size. Note that any h1 element has a default weight of 700

2. Move the h1 element a bit inside from the left. There is also a bit more spacing at the top and bottom of the h1 element. Note that h1 elements do have a default margin assigned to it, hence the additional space. We need to figure out on whether to apply the margin to the header or to the h1 element alone. I will go with the header

<header class="navbar">
  <h1>OptiFoodPhotography</h1>
  <nav class="nav-links">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    
  </nav>
</header>

3. Give the haeder element a class called navbar. In css, give that class a margin of 32px. Also remove the default h1 margin. set it to 0.
   .navbar{
   margin: 32px;
   }

h1 {
display: inline-block;
margin: 0;
}

4. Note that the ul element too has a default browser padding setting. When one inspects it, it is colored green. A lot of things have margin and padding by default. This is something we shall deal with a lot in the course. We shall learn on how to reset that all at once. For now we will just work around it by setting padding to 0; The reason why ul elements have padding is because typically they are ususlly indented. Like in a word document for example.

.nav-links ul {
padding: 0;
}

5. Add space between the h1 element and start of the ul elements. I had already figured out tat 32px is the right spacing. Ideally one would play around with the spacing to get the ideal one if you did not have a designer do that for you. In large companies, the designer will already have come up with the right dimensions for you.

h1 {
display: inline-block;
margin: 0 32px;
}

6. Add an underline at the bottom of the link to indicate that this is the page we currently are in. We need to target just that one link. Apply a class to that link and give it a text-decoration of underline. The class name is active-navlink . Note that using the text decoration will work but it is not the most ideal in this case. Note that also doing active-navlink {
  text-decoration: underline;
} will not work because it is being overriden by this property , .nav-links a {
  color: black;
  text-decoration: none;
  font-size: 20px;
  margin: 0 15px;
}. The cause of this is because of something called specificity in css. It is something that we shall also talk and see how to ensure you have the right specificity set in your css. for now, to avoid it being overidden, we shall go with a.active-navlink {
  text-decoration: underline;
}

7. Using a border bottom on the element would be ideal for purpose of styling. It will create some breathing room between the two elements. It will also control the thickness of the line which can't be done by using the text-decoration property. 




