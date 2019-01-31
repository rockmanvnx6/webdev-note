# Things that I forgot

if parent has `relative` . its child will be positioned relative to the parent.

`background-size:contain` rescale the background to fit the div.



## transition:

`transition: [what] [time] [type]`

example:

```css
transition: background-color .5s;
transition: all 1s ease;
```

> Sometime you don't want to transition all because of the zoom-in-out effect when you reload the page.



## Selection

target a double class element

```html
<div class = "class1 class2">
    
</div>
```

```css
.class1.class2 {
    
}
```

## Float

whenever we float; the parent item will not extend to the high/width of the children inside.

mostly sometimes you see `height: 0` is because of this problem. And thus sometimes it makes `margin` does not work.

```html
<div id="parent">
    <div class="child1" style="float:left">
        hahah
    </div>
    <div class="child2" style="float:left">
        hii
    </div>
</div>
```



Now parents will have height 0

To fix:

**1. #parent { float:left;} or #parent{float:right}**

**2. #parent {overflow:hidden}**

**3. #parent::after{content: "";display:block;clear:both;}**

## display: block

`display: block` by default will take full width;

**Inline elements:**

1. respect **left & right margins** and padding, but **not** <u>top & bottom</u>
2. **cannot** have a width and height set
3. **allow other elements to sit to their left and right. // sit on the same line**
4. see very important side notes on this [here](https://hacks.mozilla.org/2015/03/understanding-inline-box-model/).

**Block elements:**

1. respect all of those
2. force a line break after the block element
3. acquires full-width if width not defined

**Inline-block elements:**

1. allow other elements to sit to their left and right.
2. respect top & bottom margins and padding
3. respect height and width



## position: absolute

if position absolute; it means the width only fits the content inside it.

**position absolute display block doesn't fill the width**





## nav > ul 

this means it's only target the **unordered list** which is **immediately** **below** the **nav** element





# If some CSS properties don't work and get crossed out

It's likely because you didn't select it specificly.

When select `div class` use `div.class`.





## nth-child(n)

To select the child. Starting from 1.

**Example**:

```html
<div class="list">
    <div>
        child1
    </div>
    <div>
        child2
    </div>
    <div>
        child3
    </div>
</div>
```

```css
div.list:nth-child(1) {
    css for child 1;
}
div.list:nth-child(2) {
    css for child 2;
}
div.list:nth-child(3) {
    css for child 3;
}
```

