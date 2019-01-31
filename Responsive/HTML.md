# Important HTML tags

```html
<meta name="viewport" content ="width = device-width, initial-scale = 1">
```

This will prevent the device from automatically scale the website and keep the page originally as it is. **Without this, the device will scale automatically**. 

```html
<link rel="stylesheet" type="text/css" media="screen" href="css/screen.css">
```

`media="screen"` will tell the websites that this css files for screen.



## New semantic elements in HTML5

![image-20180630215551223](/var/folders/wl/5zc4m5n90d194b1zbgxxtsb00000gn/T/abnerworks.Typora/image-20180630215551223.png)

[link](https://www.w3schools.com/html/html5_semantic_elements.asp)

`<nav>` for navbar

`<section>` defines a section in a document.

> a section normally comes with a header.

`<article>` is indipendent on its own. like post, newspaper article.

`<aside>` side content. should be related to the surrounding content.

`<figure>` & `<figcaption>` to represent explaination to an image.

```html
<figure>
	<img src="" alt="something">
    <figcaption> What does this mean ? </figcaption>
</figure>
```

**Why semantic elements ?**

It's easier for the search engine to find the content.

**More information:**

https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting

https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure

```html
<header>
  <h1>Site Title</h1>
  <nav>
    <ul>
      <li>Link 1</li>
      <li>Link 2</li>
      <li>Link 3</li>
    </ul>
  </nav>
</header>

<main>
  <section>
    <article>
      <header>
        <h2>Some Article Title Here</h2>
        <p>by Brian Haferkamp</p>
      </header>
      <article>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
      </article>
    </article>
    <article>
      <header>
        <h2>Some Article Title Here</h2>
        <p>by Brian Haferkamp</p>
      </header>
      <article>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut voluptates, assumenda illum id, eum quaerat? Numquam, et odit illo nobis.</p>
      </article>
    </article>
  </section>

  <aside>
    <header>
      <h3>Sidebar</h3>
    </header>
    <nav>
      <ul>
        <li>Link 1</li>
        <li>Link 2</li>
        <li>Link 3</li>
      </ul>
    </nav>
  </aside>
</main>

<footer>

  <small>&copy; 2017 Highway Web Consulting</small>

</footer>
```

