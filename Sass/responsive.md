# responsive

> Using mixin to make a clean code.

```scss
$desktop: 840px;
@mixin desktop {
    @media (min-width: #{$desktop}) {
        @content; // define content
    }
}

body{
    #randomdiv{
        //normal css
        color: white;
        @include desktop {
            // css for desktop view
            color: black;
        }
    }
}
```

