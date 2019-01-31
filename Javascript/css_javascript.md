# CSS

> Javascript will add in-line CSS straight to HTML DOM

`element.style`

```javascript
document.querySelector(".class a").style
```

We can change css style by changing its properties:

`element.style.color` `element.style.backgroundColor`

```css
document.querySelector(".class a").style.color = "green";
document.querySelector(".class a").style.backgroundColor = "blue";
```

> Advantage: only modify a style properties.
>
> Disadvantage: if you want to add multiple style properties, it becomes cumbersome.



**Another way**

Another way is to use `.cssText` we can add `css` straight to the element.

```javascript
document.querySelector(".class a").style.cssText = "padding: 1em; color: white; background-color: red;"
```



**Another way**

If you look at the css attribute

```html
<div style="color:white; background-color: #000; font-weight:bold">
    
</div>
```

This is just the attribute `style` with it's own `values`. That means we can use `hasAttribute`, `setAttribute` and `removeAttribute` method.

```javascript
document.querySelector(".class a").setAttribute("style", "adding: 1em; color: white; background-color: red;");
```



