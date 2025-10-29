# Building the Photo Grid Section

In this section, we'll build the next part of our webpage — the photo grid section — and style it step by step.

## Step 1: Getting the Images

We'll be sourcing our images from [Unsplash](https://unsplash.com), a site that offers free, high-quality photos.

For this tutorial, the images have already been collected in a file called `assets.txt` to save time during the webinar.

##  Step 2: Adding the Images to the HTML

1. Open the `assets.txt` file.
2. Copy the image links found in the "image only" section.
3. Go to your `index.html` file and, right after the header section, paste the links.

###  Quick Tip: Selecting Multiple Cursors in VS Code

To quickly add `<img>` tags before each URL:

- Hold **ALT + Click** (Windows/Linux) or **Option + Click** (Mac) to create multiple cursors.
- Type: `<img src="`
- Move to the end of each URL using **Ctrl + ↓** (Windows) or **Cmd + ↓** (Mac).
- Then close the tag with `">`.

Now when you open your browser, you should see all images — though not neatly aligned yet.

## 📏 Step 3: Setting Equal Image Height

To give all images a consistent height, add this CSS:

```css
img {
  height: 800px;
}
```

> **⚠️ Note:** Using the global `img` selector isn't best practice since other images might need different styles. For now, we'll keep it simple, but later we'll learn about targeted selectors.

##  Step 4: Adding Image Captions

Each image needs a caption to attribute the photographer. We'll use the `<figcaption>` element:

```html
<figcaption>
  Photo by
  <a href="https://unsplash.com/@moniqa">Monika Grabkowska</a>
  on
  <a href="https://unsplash.com/photos/pancake-with-orange-and-blueberries-beside-scattered-chocolate-and-coffee-beans-P1aohbiT-EY">Unsplash</a>
</figcaption>
```

You'll notice that the captions push the images down — this is because `<figcaption>` is a block-level element.

##  Step 5: Grouping Each Image and Caption Together

We'll group each image and its caption using a `div` element and give it a class called `card`.

```html
<div class="card">
  <img src="image-link-here" />
  <figcaption>
    Photo by <a href="#">Photographer</a> on <a href="#">Unsplash</a>
  </figcaption>
</div>
```

This allows us to style each photo-card pair as one block.

##  Step 6: Styling the Card Grid

Now, in your `styles.css`, remove any old `img` or `figcaption` selectors and add:

### a) Make Each Card Inline and Control Its Width

```css
.card {
  width: 40%;
  display: inline-block;
}
```

### b) Ensure the Image Scales with the Card

```css
.card img {
  height: 800px;
  width: 100%;
}
```

This ensures the image fills its parent container without being squashed.

### c) Target Only Captions Inside Cards

```css
.card figcaption {
  display: inline-block;
}
```

##  Step 7: Adjusting the Grid Layout

If you try to make each card 50% wide, you'll notice that items drop to the next line. This happens because `inline-block` elements respect the whitespace between them — that extra space pushes the layout down.

To fix it:

```css
.card {
  width: 49.75%;
  display: inline-block;
}
```

This slight reduction removes overflow caused by whitespace.

## 🧩 Step 8: Fixing Image Stretching

If the images appear stretched, use the `object-fit` property:

```css
.card img {
  object-fit: cover;
}
```

This ensures images maintain their aspect ratio while filling their containers.

##  Step 9: Adding Spacing and Layout Padding

We'll use padding (not margin) because margins between inline-blocks can add unwanted gaps.

```css
.card {
  width: 49.75%;
  display: inline-block;
  box-sizing: border-box;
  padding: 25px;
}
```

##  Step 10: Grouping All Cards in a Gallery Section

Finally, wrap all the `.card` elements inside a `<figure>` element (or `<section>`) with a class name of `gallery`.

```html
<figure class="gallery">
  <!-- all .card divs here -->
</figure>
```

Then add this CSS:

```css
.gallery {
  padding: 15px;
}
```

This groups your photo cards into one clean, well-structured gallery section — ready for more advanced layout techniques like Flexbox or CSS Grid later.

## ✅ Summary

You've just:

- Created a responsive photo gallery layout.
- Grouped images and captions using semantic HTML.
- Styled cards to display neatly using `inline-block` and `object-fit`.
- Learned why whitespace and `box-sizing` matter in layout design.

**Next up** — During our cohort session, we'll learn and refine this gallery using Flexbox for even more control. 🚀