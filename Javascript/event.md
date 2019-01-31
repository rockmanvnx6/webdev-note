# Event

### Browser level event

`Load` - when the page finished loading

`Error` - when a resource failed to load

`online/offline` - online/offline

`resize` - when a viewport is resized

`scroll` - when a viewport is scrolled up/down/left/right

### DOM level

`Focus` - clicked, tabbed to

`Blur` - when element loses focus (leaving form field, etc)

`resets/submit` - forms button

`click`,`mouseover`,`drag`,`drop` - mouse event



### Other Events

`Media Events` - audio/video playback

`Progress events` - Monitor ongoing browser progress

`CSS transition events` - transition start, run, end





**Example:**

```html
<div class="cta">
    <a href="#" class="hide">Book Now!</a>
    <section id="booking-alert" class="booking-info">
        <div class="centered">
            <h3 class="content-title">Sorry about that!</h3>
            <p class="teaser two-column">By some weird coincidence, all the rooms at Moonwalk Manor are booked out for the date you planned to take your trip. Unfortunately we are unable to provide you with sufficient lodging for your party at this time. Moonwalk Manor is very busy and your satisfaction is our top priority. When you take your first steps in the moon dust, your life will change. We are always at your service. Your satisfaction matters to us.</p>
        </div>
    </section><!-- .booking-info -->
</div>
```

###### Object: click a, display `#booking-alert` 

>  First, we need to target `.cta a` & `#bookingalert`

```javascript
const BTN = document.querySelector(".cta a");
const ALR = document.querySelector("#booking-alert");
```

> Now, notice that `.cta a` is hide, we want to show it and hide `booking-alert`

```javascript
BTN.classList.remove("hide");
ALR.classList.add("hide");
```

> Next, we need a function so when we click `.cta a` we will trigger the function and display the `#bookingalert`

```javascript
function toggleAlert(a) {
    a.preventDefault(); // to prevent href="#"
    BTN.classList.toggle("hide");
    ALR.classList.toggle("hide");
}

BTN.onclick = toggleAlert;
```

We need to assign  the function **without the parenthesis in the end.** By removing the **parenthesis**, we can make sure that **the browser only run the script when it's clicked. **

The line `a.preventDefault()` prevent the default behavior of the href.

If we put in the parameter `a` acts as the `event object` and use `preventDefault()` to stop the page from jumping to `#`.

```javascript
console.log(a)
```

```console
MouseEvent {isTrusted: true, screenX: 1190, screenY: 362, clientX: 350, clientY: 266, …}
```

# Event listener

The problem with `event handler` is it only accepts one argument.

What do i mean by that?

What if you want to add another `BTN.onlick = console.log("Clicked")` ?

If you add it after the original code:

```javascript
BTN.onclick = toggleAlert; // this won't work
BTN.onlick = console.log("Clicked");
```

and if you add it before the original:

```javascript
BTN.onlick = console.log("Clicked"); // this won't work
BTN.onclick = toggleAlert;
```





**Event listener will help to solve this problem**

it will listen to every event that occured by the object.

`element.addEventListener("type",function,optional)`

For `type`: https://developer.mozilla.org/en-US/docs/Web/Events

`optional` :  A Boolean value that specifies whether the event should be executed in the capturing or in the bubbling phase. 

 Possible values:

- true - The event handler is executed in the capturing phase
- false- Default. The event handler is executed in the bubbling phase

normally it's **false**.



So in this case, it will be:

```javascript
BTN.addEventListener("click",toggleAlert,false);
BTN.addEventListener("click",function(){console.log("clicked")},false);
```



### Passing parameter into EventListener

As you can see, in the `EventListener` we can't use parenthesis. So how do we pass in parameter?

you need to use anonymous function.

```javascript
element.addEventListener("type",function(e){toggleAlert(e,parameter)},false);
function toggleAlert(event,item) {
    e.preventDefault()
    item.innerHTML == "Book Now!" ? item.innerHTML = "Oooooops!" : item.innerHTML = "Book Now!";
     ALR.classList.toggle("hide");
}
```



### For Touch

```javascript
window.addEventListener("touchmove",function(e){
    console.log(e.touches[0].clientX,e.touches[0].clientY);
})
```

